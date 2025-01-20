# Redis
- Open source in-memory (RAM: Primary memory) database.
- Redis stands for **Remote Dictionary Server**.
- A single key can have a maximum size of **512 MB**.
- It is known for its high performance, low latency, and versatility as a NoSQL data store.

## Key Features
- **In-memory storage**: Data is stored in RAM for fast read and write operations.
- **Data persistence**: Optional persistence to disk (RDB snapshots and AOF logs).
- **Flexible data structures**: Strings, Lists, Sets, Hashes, Sorted Sets, Streams, Bitmaps, and more.
- **Pub/Sub messaging**: Built-in publish-subscribe functionality for real-time communication.
- **Atomic operations**: All commands are executed as atomic operations.

## Tips
- Redis keys should be designed like **{module}:{unique_id}** for better organization and to avoid collisions.
- Use expiration (`EXPIRE`) on keys to save memory and automatically delete unused data.
- Use `SCAN` for large keyspaces instead of `KEYS` to avoid blocking the server.

## CLI Commands/Operations
```shell
# Delete a key
del {key_name}

# List all keys matching a pattern (not recommended for large datasets)
keys users*

# Set a key-value pair
set {key_name} {value}

# Get the value of a key
get {key_name}

# Set an expiration time for a key (in seconds)
expire {key_name} {seconds}

# Increment a key's value
incr {key_name}

# Check if a key exists
exists {key_name}
```

