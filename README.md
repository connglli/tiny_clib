# tiny_clib - tiny library for c

This is a tiny lib for c, implemented easily, which you can ***care nothing about type casting***.

## Content

This lib includes some data structures as well as some easy but often used functions.

+ [x] [dynamic array - array](array)
+ [x] [linked list   - list](list)
+ [x] [pool          - pool](pool)
+ [x] [hash          - hash](hash)
+ [ ] [tree map      - tree_map](.)
+ [x] [hash map      - hash_map](map/hash-map)
+ [x] [bitmap        - bitmap](bitmap)
+ [x] [bloom filter  - bloom_filter](bloom-filter)
+ [x] [generator     - gent](gent)
+ [x] [coroutine     - coro](coro)
+ [x] [string utils  - strutil](strutil)
+ [x] [logger utils  - logger](logger)
+ [x] [debug utils   - debug](debug)

## API Intro

The api of tlfc is all the same among these data structures:

+ `make_xxx`: create/alloc and then initialize a data structure, e.g. `make_array`, usually used as `array_int_t a = make_array()`, but some may not have `make` method, e.g. `pool_t`
+ `xxx_init`: initialize a data structure, e.g. `list_init`, usually used as `array_int_t a; array_init(&a)`
+ `xxx_get`: get data/nodes of a data structure, e.g. `array_get`
+ `xxx_set`: set data/nodes of a data structure, e.g. `array_set`
+ `xxx_insert`: insert data/nodes of a data structure, e.g. `list_insert`
+ `xxx_remove`: remove data/nodes of a data structure, e.g. `list_remove`
+ `xxx_deinit`: destroy a data structure, e.g. `list_deinit`

In almost all api, if your access is invalid, the program will crash.

## Examples

You can check source code of coro, it uses pool and list.

## Thanks

+ [rxi/vec](https://github.com/rxi/vec)
+ [clibs/list](https://github.com/clibs/list)
+ [petewarden/c_hashmap](https://github.com/petewarden/c_hashmap)
+ [libtask](https://swtch.com/libtask/)
+ [Coroutines in C](https://www.chiark.greenend.org.uk/~sgtatham/coroutines.html)
+ [字符串Hash函数评估](http://blog.csdn.net/liuaigui/article/details/5050697)
