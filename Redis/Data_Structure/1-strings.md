# [String](https://redis.io/docs/latest/commands/?group=string)

- SET : stores a single value
- SETNX : Stores the value only of the specified key doesn't exists
- GET : Retrives a single value
- MGET : Retrives multiple string values in a single operation
- MSET : Stores multiple key valur pairs
``` shell
    set name Ashish
    get name
    setnx name Sonu
    mget name age 
    mset name "Ashish" age 25 
```
---
---

- INCR <{key}> : Increases the value by 1
- INCRBY <{key}> <{value}>: Increases the value by <{value}>
- DECR <{key}>: Decreases the value by 1
- DECRBY <{key}> <{value}>: Decreases the value by <{value}>
``` shell 
    set count 0
    incr count
    incrby count 2
```

---
---
## OTHERS COMMAND
- GETSET
