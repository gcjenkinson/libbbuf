# libbbuf

Dynamic binary buffer modelled on `sbuf`s.

## API

### Constructor/Destructor

A binary buffer construct `bbuf_new_auto()` as follows:

```
struct bbuf *buf;
int rc;

rc = bbuf_new_auto();
```

