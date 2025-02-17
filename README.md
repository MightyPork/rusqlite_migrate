<div align="center">
  
# Rusqlite Migrate

[![docs.rs](https://img.shields.io/docsrs/rusqlite_migration?style=flat-square)](https://docs.rs/rusqlite_migration) [![Crates.io](https://img.shields.io/crates/v/rusqlite_migration?style=flat-square)](https://crates.io/crates/rusqlite_migration)

</div>

Simple schema migration tool for [rusqlite](https://lib.rs/crates/rusqlite) using [user_version](https://sqlite.org/pragma.html#pragma_user_version) instead of an SQL table to maintain the current schema version.

## Benefit

### Simplicity 

There is a set of SQL statements and you just append to it to change the schema.

### Speed

No need to add a table to be parsed, the `user_version` field is at a fixed offset in the sqlite file format.

## Example

Please see `examples/quick_start.rs`.
