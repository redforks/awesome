# README

1. [Cue Language](https://cuelang.org/) Data validation and template language, support for JSON Schema, OpenAPI, Protobuf, and more.
   Bindings for Go, Python, Java, and JavaScript.

1. [AsciiDoc](https://asciidoc-py.github.io/) Markdown alternative. Shorter and cleaner and more formatting options.
   [Other alternatives](https://github.com/mundimark/awesome-markdown-alternatives), and also [here](https://en.wikipedia.org/wiki/Comparison_of_documentation_generators)

## Rust

1. [vector](https://github.com/vectordotdev/vector) Application log gather and transform tool, [Docs](https://vector.dev/docs/)
1. [predicates](https://docs.rs/predicates/2.1.1/predicates/) Functional programming style predicates for filtering and matching.
   Drawback: compile time is slow. I don't actually use it, that should be interesting to try.
   My another concern is that using closure, sometimes triggers hard to fix lifetime problems.

## Algebra

1. [nalgebra](https://nalgebra.org/) Linear algebra library for Rust.
1. [euclid](https://docs.rs/euclid/latest) 2D and 3D geometry library for Rust.
1. [glam](https://crates.io/crates/glam) A simple and fast linear algebra library for games and graphics.

`nalgebra` optionally depends on `glam`. `glam` a bit low level.
`euclid` and `glam` are similar.
`nalgebra` much popular than `euclid`.
`euclid` add Unit generic type argument, cleaning to map coordinate spaces and length units.

## num crate

`num` crate is a meta crate, if only use a few features, such as `ToPrimitimive`, import the specific crates
to save compile time, such as `num-traits`.

## phf

[`phf`](https://crates.io/crates/phf), Perficate Hash Function, is a macro to generate a perfect hash function.
Generate lookup table at compile time. PHF hashtable is a fast and memory efficient alternative to `HashMap`.
`phf` crate is very popular, a good tool to do tiny optimization.