# appsignal-transmitter (Deprecated)

**This crate is deprecated.** It is a thin re-export of `reqwest` and provides no additional functionality. Please use `reqwest` directly instead.

## Migrating

### 1. Update your dependency

Replace:

```toml
appsignal-transmitter = { git = "https://github.com/appsignal/appsignal-transmitter.git" }
```

With:

```toml
reqwest = { version = "0.12", default-features = false, features = ["rustls-tls"] }
```

### 2. Update your imports

Replace any `appsignal_transmitter::reqwest` paths with `reqwest` directly.

Before:

```rust
use appsignal_transmitter::reqwest::{Client, Response, Url};
```

After:

```rust
use reqwest::{Client, Response, Url};
```
