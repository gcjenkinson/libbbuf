# libbbuf

Dynamic binary buffer modelled on `sbuf`s.

## Build

```
$ ./autogensh
$make
$make install
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
