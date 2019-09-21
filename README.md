# meka-passport

## Purpose

Meka-passport is to bind the user's substrate based address and the social media account. It's a srml that based on substrate.

The name passport is from the passport.js which is a very popular authentication for Node.js. 

Meka-passport is included in the [meka-node](https://github.com/projectmeka/meka-node) project.

## Dependencies

### Traits

This module does not depend on any externally defined traits.

### Modules

This module does not depend on any other SRML or externally developed modules.

## Installation

### Runtime `Cargo.toml`

To add this module to your runtime, simply include the following to your runtime's `Cargo.toml` file:

```rust
[dependencies.meka-passport]
default_features = false
git = 'https://github.com/projectmeka/meka-passport'
```

and update your runtime's `std` feature to include this module:

```rust
std = [
    ...
    'meka-passport/std',
]
```

### Runtime `lib.rs`

You should implement it's trait like so:

```rust
/// Used for the module test_module
impl meka_passport::Trait for Runtime {
	type Event = Event;
}
```

and include it in your `construct_runtime!` macro:

```rust
ExampleModule: meka_passport::{Module, Call, Storage, Event<T>},
```

### Genesis Configuration

This template module does not have any genesis configuration.

## Reference Docs

You can view the reference docs for this module by running:

```
cargo doc --open
```

or by visiting this site: <Add Your Link>
