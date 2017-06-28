# Intro to Persistence Technologies

### Objectives

- NSUserDefaults
- Keychain
- Filesystem
- Encoding/Decoding
- Advanced Persistence Technologies - CoreData, Realm etc.

## NSUserDefaults
## Keychain
## Filesystem
## NSCoding

## Advanced Persistence Technologies


##### Core Data, Realm, SQLite
- Querying / selecting a subset of object graph
- Saving individual objects independent of entire graph
- Simple versioning of data model


## Summary
- UserDefaults is the easiest way to persist a small amount of
information in an application
- Security relevant information should be stored in the Keychain
- Apps run in a sandbox where they have access to their bundle and
different types of directories
- The entire object graph of an application can be persisted using
- NSCoding and NSArchiver; good solution if you merely need to store
the state of your app and don’t need queries or migrations

## Resources
