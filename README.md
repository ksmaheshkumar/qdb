# qdb

A fast, high availability, fully Redis compatible store.

## Redis Command Support

### Keys Command

    +-------------------+-----------+-------------------------------------------------------------------+
    |      Command      | Twemproxy | redis-binlog                                                      |
    +-------------------+-----------+-------------------------------------------------------------------+
    |        DEL        |    Yes    | Yes                                                               |
    +-------------------+-----------+-------------------------------------------------------------------+
    |       DUMP        |    Yes    | Yes                                                               |
    +-------------------+-----------+-------------------------------------------------------------------+
    |      EXISTS       |    Yes    | Yes                                                               |
    +-------------------+-----------+-------------------------------------------------------------------+
    |      EXPIRE       |    Yes    | Yes                                                               |
    +-------------------+-----------+-------------------------------------------------------------------+
    |     EXPIREAT      |    Yes    | Yes                                                               |
    +-------------------+-----------+-------------------------------------------------------------------+
    |       KEYS        |    No     |                                                                   |
    +-------------------+-----------+-------------------------------------------------------------------+
    |      MIGRATE      |    No     |                                                                   |
    +-------------------+-----------+-------------------------------------------------------------------+
    |       MOVE        |    No     |                                                                   |
    +-------------------+-----------+-------------------------------------------------------------------+
    |      OBJECT       |    No     |                                                                   |
    +-------------------+-----------+-------------------------------------------------------------------+
    |      PERSIST      |    Yes    | Yes                                                               |
    +-------------------+-----------+-------------------------------------------------------------------+
    |      PEXPIRE      |    Yes    | Yes                                                               |
    +-------------------+-----------+-------------------------------------------------------------------+
    |     PEXPIREAT     |    Yes    | Yes                                                               |
    +-------------------+-----------+-------------------------------------------------------------------+
    |      PTTL         |    Yes    | Yes                                                               |
    +-------------------+-----------+-------------------------------------------------------------------+
    |     RANDOMKEY     |    No     |                                                                   |
    +-------------------+-----------+-------------------------------------------------------------------+
    |      RENAME       |    No     |                                                                   |
    +-------------------+-----------+-------------------------------------------------------------------+
    |     RENAMENX      |    No     |                                                                   |
    +-------------------+-----------+-------------------------------------------------------------------+
    |      RESTORE      |    Yes    | Yes                                                               |
    +-------------------+-----------+-------------------------------------------------------------------+
    |      SORT         |    Yes*   |                                                                   |
    +-------------------+-----------+-------------------------------------------------------------------+
    |       TTL         |    Yes    | Yes                                                               |
    +-------------------+-----------+-------------------------------------------------------------------+
    |      TYPE         |    Yes    | Yes                                                               |
    +-------------------+-----------+-------------------------------------------------------------------+
    |      SCAN         |    No     |                                                                   |
    +-------------------+-----------+-------------------------------------------------------------------+

### Strings Command

    +-------------------+-----------+------------------------------------------------------------------+
    |      Command      | Twemproxy | redis-binlog                                                     |
    +-------------------+-----------+------------------------------------------------------------------+
    |       APPEND      |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      BITCOUNT     |    Yes    |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |       BITOP       |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |       DECR        |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      DECRBY       |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |       GET         |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      GETBIT       |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |     GETRANGE      |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      GETSET       |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      INCR         |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      INCRBY       |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |     INCRBYFLOAT   |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      MGET         |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      MSET         |    Yes*   | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      MSETNX       |    No     | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      PSETEX       |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      SET          |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      SETBIT       |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      SETEX        |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      SETNX        |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      SETRANGE     |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      STRLEN       |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+

### Hashes

    +-------------------+-----------+------------------------------------------------------------------+
    |      Command      | Twemproxy | redis-binlog                                                     |
    +-------------------+-----------+------------------------------------------------------------------+
    |       HDEL        |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      HEXISTS      |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |       HGET        |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      HGETALL      |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      HINCRBY      |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |    HINCRBYFLOAT   |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      HKEYS        |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      HLEN         |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      HMGET        |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      HMSET        |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      HSET         |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      HSETNX       |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      HVALS        |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      HSCAN        |    Yes    |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+

### Lists

    +-------------------+-----------+------------------------------------------------------------------+
    |      Command      | Twemproxy | redis-binlog                                                     |
    +-------------------+-----------+------------------------------------------------------------------+
    |       BLPOP       |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |       BRPOP       |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |     BRPOPLPUSH    |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |      LINDEX       |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      LINSERT      |    Yes    |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |      LLEN         |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      LPOP         |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      LPUSH        |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      LPUSHX       |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      LRANGE       |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      LREM         |    Yes    |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |      LSET         |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      LTRIM        |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      RPOP         |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |     RPOPLPUSH     |    Yes*   |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |      RPUSH        |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      RPUSHX       |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+

### Sets

    +-------------------+-----------+------------------------------------------------------------------+
    |      Command      | Twemproxy | redis-binlog                                                     |
    +-------------------+-----------+------------------------------------------------------------------+
    |      SADD         |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      SCARD        |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      SDIFF        |    Yes*   |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |     SDIFFSTORE    |    Yes*   |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |      SINTER       |    Yes*   |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |    SINTERSTORE    |    Yes*   |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |     SISMEMBER     |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |     SMEMBERS      |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      SMOVE        |    Yes*   |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |      SPOP         |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |    SRANDMEMBER    |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      SREM         |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |     SUNION        |    Yes*   |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |   SUNIONSTORE     |    Yes*   |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |      SSCAN        |    Yes    |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+

### Sorted Sets

    +-------------------+-----------+------------------------------------------------------------------+
    |      Command      | Twemproxy | redis-binlog                                                     |
    +-------------------+-----------+------------------------------------------------------------------+
    |      ZADD         |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      ZCARD        |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |      ZCOUNT       |    Yes    |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |      ZINCRBY      |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |     ZINTERSTORE   |    Yes*   |                                                                  |
    +--------------------------------------------------------------------------------------------------+
    |      ZLEXCOUNT    |    Yes    |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |      ZRANGE       |    Yes    |                                                                  |
    +--------------------------------------------------------------------------------------------------+
    |    ZRANGEBYLEX    |    Yes    |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |    ZRANGEBYSCORE  |    Yes    |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |      ZRANK        |    Yes    |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |       ZREM        |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |   ZREMRANGEBYLEX  |    Yes    |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |   ZREMRANGEBYRANK |    Yes    |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |  ZREMRANGEBYSCORE |    Yes    |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |    ZREVRANGE      |    Yes    |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |  ZREVRANGEBYSCORE |    Yes    |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |     ZREVRANK      |    Yes    |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |     ZSCORE        |    Yes    | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |    ZUNIONSTORE    |    Yes*   |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |      ZSCAN        |    Yes    |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+

### HyperLogLog

    +-------------------+-----------+------------------------------------------------------------------+
    |      Command      | Twemproxy |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |       PFADD       |    Yes    |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |      PFCOUNT      |    Yes    |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |      PFMERGE      |    Yes*   |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+


### Pub/Sub

    +-------------------+-----------+------------------------------------------------------------------+
    |      Command      | Twemproxy |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |     PSUBSCRIBE    |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |     PUBLISH       |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |    PUNSUBSCRIBE   |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |     SUBSCRIBE     |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |     UNSUBSCRIBE   |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+

### Transactions

    +-------------------+-----------+------------------------------------------------------------------+
    |      Command      | Twemproxy |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |      DISCARD      |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |       EXEC        |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |       MULTI       |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |      UNWATCH      |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |       WATCH       |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+

### Scripting

    +-------------------+-----------+------------------------------------------------------------------+
    |      Command      | Twemproxy |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |       EVAL        |    Yes*   |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |     EVALSHA       |    Yes*   |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |    SCRIPT EXISTS  |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |    SCRIPT FLUSH   |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |    SCRIPT KILL    |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |    SCRIPT LOAD    |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+

### Connection

    +-------------------+-----------+------------------------------------------------------------------+
    |      Command      | Twemproxy |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |       AUTH        |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |       ECHO        |    No     | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |       PING        |    No     | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |       QUIT        |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |      SELECT       |    No     | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+

### Server

    +-------------------+-----------+------------------------------------------------------------------+
    |      Command      | Twemproxy |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |    BGREWRITEAOF   |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |      BGSAVE       |    No     | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |    CLIENT KILL    |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |    CLIENT LIST    |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |    CONFIG GET     |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |    CONFIG SET     |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |  CONFIG RESETSTAT |    No     |                                                                  |
    +-------------------+------------------------------------------------------------------------------+
    |     DBSIZE        |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |    DEBUG OBJECT   |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |    DEBUG SEGFAULT |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |     FLUSHALL      |    No     | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |     FLUSHDB       |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |      INFO         |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |     LASTSAVE      |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |     MONITOR       |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |      SAVE         |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |     SHUTDOWN      |    No     | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |     SLAVEOF       |    No     | Yes                                                              |
    +-------------------+-----------+------------------------------------------------------------------+
    |     SLOWLOG       |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |      SYNC         |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+
    |      TIME         |    No     |                                                                  |
    +-------------------+-----------+------------------------------------------------------------------+

### Codis-Slots Command

    +-------------------+-------------------------------------------------------------------------------+
    |      Command      | redis-binlog                                                                  |
    +-------------------+-------------------------------------------------------------------------------+
    |   SlotsInfo       | Yes*                                                                          |
    +-------------------+-------------------------------------------------------------------------------+
    |   SlotsMgrtSlot   | Yes*                                                                          |
    +-------------------+-------------------------------------------------------------------------------+
    |  SlotsMgrtTagSlot | Yes*                                                                          |
    +-------------------+-------------------------------------------------------------------------------+
    |   SlotsMgrtOne    | Yes                                                                           |
    +-------------------+-------------------------------------------------------------------------------+
    |  SlotsMgrtTagOne  | Yes                                                                           |
    +-------------------+-------------------------------------------------------------------------------+
    |    SlotsDel       |                                                                               |
    +-------------------+-------------------------------------------------------------------------------+
    |    SlotsHashKey   | Yes                                                                           |
    +-------------------+-------------------------------------------------------------------------------+
    |    SlotsCheck     |                                                                               |
    +-------------------+-------------------------------------------------------------------------------+

    * slotsinfo, slotsmgrtslot and slotsmgrttagslot cannot get the exact value of slot's size, but return 1 if it's not empty

## Performance

### Setup

    1. install gorocks.a & levigo.a to GOPATH
    $ cd redis-binlog/extern && bash setup.sh

    2. run redis-binlog with specifed config file
    $ redis-binlog -c conf/config.toml -n 4 --create

### redis-benchmark against redis-binlog (default config, see conf/config.toml)

    $ ./redis-benchmark -q -t set,get,incr,lpush,lpop,sadd,spop,lpush,lrange -c 100 -p 6380 -r 1000 -n 100000
    SET: 31094.53 requests per second
    GET: 53361.79 requests per second
    INCR: 36049.03 requests per second
    LPUSH: 43346.34 requests per second
    LPOP: 37965.07 requests per second
    SADD: 40899.80 requests per second
    SPOP: 53333.33 requests per second
    LPUSH (needed to benchmark LRANGE): 40567.95 requests per second
    LRANGE_100 (first 100 elements): 3395.12 requests per second
    LRANGE_300 (first 300 elements): 1202.59 requests per second
    LRANGE_500 (first 450 elements): 849.21 requests per second
    LRANGE_600 (first 600 elements): 640.11 requests per second
