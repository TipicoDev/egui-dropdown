# egui-dropdown
Dropdown list for egui.

![](media/showcase1.png)

# Installation
```toml
[dependencies]
egui-dropdown = "0.11"
```

# Usage
```rust
// Working example can be found in `examples/dropdown.rs`

ui.add(DropDownBox::from_iter(
    &self.items,
    "test_dropbox",
    &mut self.buf,
    |ui, text| ui.selectable_label(false, text)
));
```

# Naming
Although it's called `DropDownBox`, technically speaking it should be called `ComboBox`.
But this is what egui uses for its version of the widget so yeah.

# Features
There is an `unidecode` feature that uses the crate [rust-unidecode](https://github.com/chowdhurya/rust-unidecode).
It allows the usage of `.ignore_accent_marks(bool)` which ignores accent marks in the filtering.