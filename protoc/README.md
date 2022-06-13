# Protoc

## --decode_raw

> Read an arbitrary protocol message from standard input and write the raw tag/value pairs in text format to standard output.  No PROTO_FILES should be given when using this flag.

### Example usage

```shell
cat simple.bin | protoc --decode_raw
```

## --decode

> Read a binary message of the given type from standard input and write it in text format to standard output.  The message type must be defined in PROTO_FILES or their imports.

### Example usage

```shell
cat simple.bin | protoc --decode=Simple simple.proto > simple.txt
```

```shell
cat simple.bin | protoc --decode=simple.Simple simple.proto > simple.txt
```

## --encode

> Read a text-format message of the given type from standard input and write it in binary to standard output.  The message type must be defined in PROTO_FILES or their imports.

### Example usage

```shell
cat simple.txt | protoc --encode=Simple simple.proto > simple.pb
```

```shell
cat simple.txt | protoc --encode=simple.Simple simple.proto > simple.pb
```