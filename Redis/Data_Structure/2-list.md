# List
- 👉🏻 We can use the list to have a data structure like queue, stack ... by organizing the push and pop in particular order

- LPUSH : Add a element to the head of the list
- RPUSH : Add a new element to the tail of the list
- LPOP : Remove a element from the head of the list
- PROP : Remove a element from the tail of the list
- LLEN : Return the length of the list
- LMOVE : Automatically moves element from one list to another
- LTRIM : Reduces the list to the specified range of element

``` shell
lpush messages "HI"
rpush messages "Hello"
lpop
```

## Blocking commands
- BLPOP : Removes and returns the element from the head of a list. If the list is empty the command will block untill an element became available or untill the specified timeout is reached.

- BLMOVE : Automatically moves element from a source list to a target list. If the source list is empty, the command will block until a new element becomes available.

- 👉🏻 : Similarly BRPOP and BRMOVE commands are also there.

``` shell
blpop messages 10
```

## Fetching elements
- LRANGE : Return the elements of the list
``` shell
lrange messages 0 -1 # Returns all the elements
lrange messages 0 1 # Returns all the elements including 0 & 1 indexes
```