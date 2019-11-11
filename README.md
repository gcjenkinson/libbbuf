# libbbuf

Dynamic binary buffer modelled on FreeBSD's `sbuf`. 

## Build

```
$ ./autogensh
$ make
$ make install
```

## API

### Constructor/Destructor

A binary buffer with the default options can be constructed using the `bbuf_new_auto()` function as follows, the call to `bbuf_new_auto` returns `0` on success:

```
struct bbuf *buf;
int rc;

rc = bbuf_new_auto();
```

The binary buffer constructed by the call to `bbuf_new_auto()` should be deleted by calling `bbuf_delete` as follows, this frees up all allocated memory: 

```
bbuf_delete(buf);
```
### Get/Put

To write a primive value into the binary buffer:

```
int8_t value;

value = 0;
bbuf_put_int8(bbuf, value);
```

### Misc

The `bbuf_data()` function returns the memory backing the binary buffer:

`bbuf_data()`

The `bbuf_pos()` function returns the current offset into memory backing the binary buffer:

`bbuf_pos()`
