# uluru

A simple, fast, least-recently-used (LRU) cache implementation used for
Servo's style system.

`LRUCache` uses a fixed-capacity array for storage. It provides `O(1)`
insertion, and `O(n)` lookup.  It does not require an allocator and can be
used in `no_std` crates.  It is implemented in 100% safe Rust.

## Cargo Features

By default, this crate won't need the standard library. However, if the `std` cargo feature is enabled, `insert()` will
return a replaced value which allows to reuse memory it may have contained.

* [Documentation](https://docs.rs/uluru)
* [crates.io](https://crates.io/crates/uluru)
* [Release notes](https://github.com/servo/uluru/releases)
