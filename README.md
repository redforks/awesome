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

## cint crate

`cint`` - color interop, defines common color types, and a `Spaces` enum for these color spaces. No color space conversion.

## mint crate

`mint` - Math interoperability standard types. Mainly for computer graphics, such as Matrix, Point, Angle, Vector.

## phf

[`phf`](https://crates.io/crates/phf), Perficate Hash Function, is a macro to generate a perfect hash function.
Generate lookup table at compile time. PHF hashtable is a fast and memory efficient alternative to `HashMap`.
`phf` crate is very popular, a good tool to do tiny optimization.

## String Interning, Tiny/Small String

`string-interner`, `string-cache`, `tinystr`, `smartstr`, `kstring` and many other tiny/small strings.

`string-interner` is specifically designed for interning, it's a bit low level and hard to use. Does not support mutable.

`string-cache` has a confusing name, but it's a general purpose tiny string library, support mutable, static, inline storage (upper to 7 bytes).
High efficiency. Use a single u64 as underlying storage, smaller than most tiny/small string crates. It should work on wasm, see: [issue](https://github.com/servo/string-cache/pull/254). Best use case: heavily mix use of predefined static str and ascii str, such as computer language parsing and tokenizing. Drawback: heavily unsafe code.

## Ant Design

[Ant Design](https://ant.design/) Application UI components, React based. Use its own css classes, not based on tailwind. Very popular.

## Shadcn-UI

[Shadcn-UI](https://shadcn-ui.com/) Application UI components, React based and other official bindings such as steve. Use tailwind css classes, 
support many themes.

## Nuxt and Next

Next is React based, Nuxt is Vue based. They are similar, support hyper computation, provides server and client side components,
controller, and BI processing etc. I haven't use it yet, because I don't want js at server side. Static Server side not very useful, because it
is static.