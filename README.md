# tui-realm-treeview

<p align="center">
  <img src="docs/images/tui-realm-treeview.svg" width="256" height="256" />
</p>

[![License: MIT](https://img.shields.io/badge/License-MIT-teal.svg)](https://opensource.org/licenses/MIT) [![Stars](https://img.shields.io/github/stars/veeso/tui-realm-treeview.svg)](https://github.com/veeso/tui-realm-treeview) [![Downloads](https://img.shields.io/crates/d/tui-realm-treeview.svg)](https://crates.io/crates/tui-realm-treeview) [![Crates.io](https://img.shields.io/badge/crates.io-v0.1.0-orange.svg)](https://crates.io/crates/tui-realm-treeview) [![Docs](https://docs.rs/tui-realm-treeview/badge.svg)](https://docs.rs/tui-realm-treeview)  

[![Build](https://github.com/veeso/tui-realm-treeview/workflows/Linux/badge.svg)](https://github.com/veeso/tui-realm-treeview/actions) [![Build](https://github.com/veeso/tui-realm-treeview/workflows/MacOS/badge.svg)](https://github.com/veeso/tui-realm-treeview/actions) [![Build](https://github.com/veeso/tui-realm-treeview/workflows/Windows/badge.svg)](https://github.com/veeso/tui-realm-treeview/actions) [![Coverage Status](https://coveralls.io/repos/github/veeso/tui-realm-treeview/badge.svg?branch=main)](https://coveralls.io/github/veeso/tui-realm-treeview?branch=main)

Developed by Christian Visintin  
Current version: 0.1.0 (06/06/2021)

---

- [tui-realm-treeview](#tui-realm-treeview)
  - [About tui-realm-treeview 🌲](#about-tui-realm-treeview-)
  - [Get started 🏁](#get-started-)
    - [Add tui-realm-treeview to your Cargo.toml 🦀](#add-tui-realm-treeview-to-your-cargotoml-)
    - [Use the treeview component](#use-the-treeview-component)
    - [About performance](#about-performance)
  - [Documentation 📚](#documentation-)
  - [Contributing and issues 🤝🏻](#contributing-and-issues-)
  - [Changelog ⏳](#changelog-)
  - [Buy me a coffee ☕](#buy-me-a-coffee-)
  - [License 📃](#license-)

---

## About tui-realm-treeview 🌲

tui-realm-treeview is an implementation of a **treeview component** for [tui-realm](https://github.com/veeso/tui-realm), it is implemented wrapping the [tui-tree-widget](https://crates.io/crates/tui-tree-widget)

---

## Get started 🏁

### Add tui-realm-treeview to your Cargo.toml 🦀

```toml
tui-realm-treeview = "0.1.0"
```

### Use the treeview component

View how to use the treeview-component following the [example](examples/demo.rs). The example contains a simple file explorer using a tree view, the depth is set to 3.

```sh
cargo run --example demo
```

- Press `ENTER` to change directory
- Press `BACKSPACE` to go to upper directory
- Move up and down with `UP/DOWN` arrow keys
- Open directories with `RIGHT`
- Close directories with `LEFT`
- Change window between input field and treeview with `TAB`
- Press `ESC` to quit

### About performance

In this library there is a consistent use of recursion, and since rust is not functional, this might lead to stack overflows when dealing with huge trees. In addition consider that each level of depth added, will slow down the application exponentially.

Best practices:

- Except when dealing with small trees, always set a depth for the tree
- For file systems, depth 3 should be fine

---

## Documentation 📚

The developer documentation can be found on Rust Docs at <https://docs.rs/tui-realm-treeview>

---

## Contributing and issues 🤝🏻

Contributions, bug reports, new features and questions are welcome! 😉
If you have any question or concern, or you want to suggest a new feature, or you want just want to improve tui-realm, feel free to open an issue or a PR.

Please follow [our contributing guidelines](CONTRIBUTING.md)

---

## Changelog ⏳

View tui-realm-treeview's changelog [HERE](CHANGELOG.md)

---

## Buy me a coffee ☕

If you like tui-realm-treeview and you're grateful for the work I've done, please consider a little donation 🥳

[![Buy-me-a-coffee](https://img.buymeacoffee.com/button-api/?text=Buy%20me%20a%20coffee&emoji=&slug=veeso&button_colour=404040&font_colour=ffffff&font_family=Comic&outline_colour=ffffff&coffee_colour=FFDD00)](https://www.buymeacoffee.com/veeso)

---

## License 📃

tui-realm is licensed under the MIT license.

You can read the entire license [HERE](LICENSE)
