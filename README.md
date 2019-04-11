# Rust Pros Bindgen
Generate PROS bindings to rust
### Requirements
- The latest stable version of rust
- gcc 
- PROS
- some random header modifications 

### Useage
In `build.rs`
```rust
use pros_bindgen::bindgen;

fn main(){
    bindgen();
}
 ```
 
 In some file to import the bindings
```rust 
#![allow(non_upper_case_globals)]
#![allow(non_camel_case_types)]
#![allow(non_snake_case)]
#![allow(dead_code)]
include!(concat!(env!("OUT_DIR"), "/bindings.rs"));
```

### What header modifications
If you want to use it, make an issue and I'll document it.
