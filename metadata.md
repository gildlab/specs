# Metadata

### Magic numbers

The magic number for the first 8 bytes of offchainAsset vault meta documents is

```
0xff688a46f9cf4594
```

Which was obtained by running

```
openssl rand -hex 8
```

Then manually setting the leading bytes to `0xff`.

Tooling that wishes to read meta MUST discard/ignore all binary data that
does not begin with the magic number.

#### Magic numbers

Here is a table of magic numbers that the tooling maintained by the authors of
this document are already handling.

| Number             | Interpretation             |
| ---                |----------------------------|
| 0xff688a46f9cf4594 | Prefixes oa meta documents |
| 0xffa8e8a9b9cf4a31 | Prefixes oa schemas        |
