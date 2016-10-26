System wide ld config
=====================

This may be common knowledge, but I discovered it recently.
`/etc/ld.so.conf{,.d/}` have paths, one per line, absolute,
that will be used globally.

`LD_LIBRARY_PATH` adds to these when it is set. these paths are
searched for shared objects (`.so`) to be loaded.

`RPATH`s in executables (baked in at compile time), which can be
overridden by setting `LD_RUN_PATH` are always searched in addition
to these.
