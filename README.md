# Stack - missing debug symbols

Proof of missing debug symbols when building with cabal.

## How to build
```
docker-compose run --rm build
```

## How to test
```
gdb --args out/nodebug-exe +RTS -V0
```

GDB prints `(no debugging symbols found)`, where the executable should contain them, because it is built with the `-g` option (vide: https://downloads.haskell.org/~ghc/master/users-guide/debug-info.html)
