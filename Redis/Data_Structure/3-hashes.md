# Redis [HASHES](https://redis.io/docs/latest/develop/data-types/hashes/)

Redis Hashes are a data type that maps fields to values, similar to a dictionary or object. They are ideal for storing and retrieving small collections of key-value pairs.

## Key Features
- A hash is stored as a single Redis key but can hold multiple field-value pairs.
- Suitable for objects like user profiles, configuration settings, etc.
- Hash fields and values are strings.
- Efficient for managing multiple related values under a single key.

## Commands

### Basic Hash Operations
- **HSET `<key>` `<field>` `<value>`**: Sets the value of a field in a hash. If the field already exists, it updates the value.
- **HGET `<key>` `<field>`**: Retrieves the value of a specific field in the hash.
- **HGETALL `<key>`**: Retrieves all fields and values in the hash.
- **HMSET `<key>` `<field1>` `<value1>` `<field2>` `<value2>`**: Sets multiple fields and values in a single command (deprecated in favor of `HSET`).
- **HMGET `<key>` `<field1>` `<field2>`**: Retrieves values of specific fields in the hash.

```shell
# Example Commands
hset user:1 name "Ashish" age 25
hget user:1 name
hmset user:2 name "Sonu" age 30 city "Bangalore"
hmget user:2 name age
hgetall user:1