To compile:

```console
$ GOPATH="$PWD" go build ./src/cmd && ./cmd
main
$ GOPATH="$PWD" go build -tags a ./src/cmd && ./cmd
main
a
$ GOPATH="$PWD" go build -tags 'a b' ./src/cmd && ./cmd
main
a
b
$ GOPATH="$PWD" go build -tags 'b a' ./src/cmd && ./cmd
main
a
b
$ GOPATH="$PWD" go build -tags a -tags b ./src/cmd && ./cmd
main
b
```
