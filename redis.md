REDIS COMMANDS
============

SORTED SETS
-----------

### ZADD
- Lưu data theo `key-value`, tự động sắp xếp các value theo giá trị của key
```
redis> ZADD myzset 1 "one"
(integer) 1
redis> ZADD myzset 1 "uno"
(integer) 1
redis> ZADD myzset 2 "two" 3 "three"
(integer) 2
//xuất sets
redis> ZRANGE myzset 0 -1 WITHSCORES
1) "one"
2) "1"
3) "uno"
4) "1"
5) "two"
6) "2"
7) "three"
8) "3"
redis> 
```

### ZCARD
- Đếm số lượng data được lưu vào 
```
 ZCARD myzset
 (integer) 6
```