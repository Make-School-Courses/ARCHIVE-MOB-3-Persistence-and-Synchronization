# UserDefaults and Keychain

## Objectives


## UserDefaults

UserDefaults allows to store Strings, Numbers, Dates, NSData and
Arrays or Dictionaries

Usually should be used to store user preferences, can be used to store small amount of persistent information

Should never be used for sensitive data

```swift
// Set
UserDefaults.standard.set(false, forKey: "FirstTimeUser")

// Get
let value = UserDefaults.standard.bool(forKey: "FirstTimeUser")
```

## Keychain

Is used to store sensitive information, such as passwords

All information is stored encrypted

Apple’s API is arcane - Open Source Libraries such as
KeychainSwift will make your life easier!


## Encoding/Decoding

Encoding: Creating a binary/textual representation (that can
be stored on disk, transferred via network) from an object
graph

Decoding: Creating an object graph from a binary/textual
representation

### Step 1: Implement NSCoding

```swift
class Movie: NSObject, NSCoding {
    var title: String
    var duration: Int

    init(title: String, duration: Int) {
        self.title = title
        self.duration = duration
    }

    required convenience init?(coder aDecoder: NSCoder) {
        guard let title = aDecoder.decodeObject(forKey: "title") as? String
            else { return nil }
        let duration = aDecoder.decodeInteger(forKey: "duration")

        self.init(title: title, duration: duration)
    }

    func encode(with aCoder: NSCoder) {
        aCoder.encode(self.title, forKey: "title")
        aCoder.encode(self.duration, forKey: "duration")
    }
}

```

### Step 2: User Archiver

Archive

```swift
NSKeyedArchiver.archiveRootObject(movies, toFile: "/path/to/archive")
```

Unarchive

```
let unarchivedMovies = NSKeyedUnarchiver.unarchiveObjectWithFile(
"/path/to/archive") as? [Movie]
```

### When to use NSCoding
Use NSCoding when main goal of persistence in your App is
to store the current state of the application
If you additionally want to create queries, need migrations,
etc, there are better solutions (e.g., CoreData)
