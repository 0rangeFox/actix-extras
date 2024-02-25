# Changes

## Unreleased

- Use new feature named `tls` for TLS settings. [#380]
- Add new function `settings::tls::Tls::get_ssl_acceptor_builder()` to build `openssl::ssl::SslAcceptorBuilder`. [#380]
- Implement TLS logic for `ApplySettings<S>::try_apply_settings()`. [#380]
- Add `openssl` dependency;
- Minimum supported Rust version (MSRV) is now 1.75.
- `ApplySettings<S>::apply_settings()` is deprecated; `ApplySettings<S>::try_apply_settings()` should be preferred. [#380]

[#380]: https://github.com/actix/actix-extras/pull/380

## 0.7.1

- Fix doc examples.

## 0.7.0

- The `ApplySettings` trait now includes a type parameter, allowing multiple types to be implemented per configuration target.
- Implement `ApplySettings` for `ActixSettings`.
- `BasicSettings::from_default_template()` is now infallible.
- Rename `AtError => Error`.
- Remove `AtResult` type alias.
- Update `toml` dependency to `0.8`.
- Remove `ioe` dependency; `std::io::Error` is now used directly.
- Remove `Clone` implementation for `Error`.
- Implement `Display` for `Error`.
- Implement std's `Error` for `Error`.
- Minimum supported Rust version (MSRV) is now 1.68.

## 0.6.0

- Update Actix Web dependencies to v4 ecosystem.
- Rename `actix.ssl` settings object to `actix.tls`.
- `NoSettings` is now marked `#[non_exhaustive]`.

## 0.5.2

- Adopted into @actix org from <https://github.com/jjpe/actix-settings>.
