# Awesome TypeScript Compilers, Transpilers and Runtimes

A list of TypeScript compilers, runtimes, and related tools.

[esbuild](https://esbuild.github.io/content-types/#typescript) and
[Node.js type stripping](https://nodejs.org/api/typescript.html#type-stripping)
don't check types. Use a separate checker such as `tsc --noEmit`.

## Contents

- [JavaScript toolchain](#javascript-toolchain)
- [Runtimes](#runtimes)
- [Loaders and type stripping](#loaders-and-type-stripping)
- [Language and platform targets](#language-and-platform-targets)
- [Research and education](#research-and-education)
- [Related tooling](#related-tooling)
- [Contributing](#contributing)

<a name="javascript-targets"></a>

## JavaScript toolchain

### Compilers and type checkers

- [ezno](https://github.com/kaleidawave/ezno): JavaScript compiler and TypeScript checker written in Rust, focused on static analysis. [Playground](https://kaleidawave.github.io/ezno/playground/).
- [stc](https://github.com/dudykr/stc): TypeScript type checker written in Rust. Archived.
- [tsc](https://github.com/microsoft/TypeScript): The official TypeScript compiler from Microsoft. [Playground](https://www.typescriptlang.org/play).
- [tsgo](https://github.com/microsoft/typescript-go): Microsoft's Go-based TypeScript compiler.

### Transpilers and compiler toolkits

- [babel](https://github.com/babel/babel): JavaScript compiler that also transpiles TypeScript. [Playground](https://babeljs.io/repl).
- [oxc](https://github.com/oxc-project/oxc): JavaScript and TypeScript parser, linter, and compiler written in Rust. [Playground](https://playground.oxc.rs/).
- [sucrase](https://github.com/alangpierce/sucrase): Babel alternative for projects targeting modern JavaScript runtimes. [Playground](https://sucrase.io/).
- [swc](https://github.com/swc-project/swc): JavaScript and TypeScript compiler written in Rust. [Playground](https://swc.rs/playground).
- [swc4j](https://github.com/caoccao/swc4j): SWC compilation and bundling for JavaScript and TypeScript on the JVM.

### Bundlers and build tools

- [esbuild](https://github.com/evanw/esbuild): JavaScript and TypeScript bundler written in Go. [Playground](https://esbuild.github.io/try/).
- [farm](https://github.com/farm-fe/farm): Vite-compatible web build tool written in Rust.
- [Mako](https://github.com/umijs/mako): Web bundler written in Rust for apps, libraries, and frameworks. [Playground](https://utoo-repl.vercel.app/).
- [parcel](https://github.com/parcel-bundler/parcel): Zero-configuration web app bundler with TypeScript support. [REPL](https://repl.parceljs.org/).
- [rolldown](https://github.com/rolldown/rolldown): JavaScript and TypeScript bundler written in Rust, with a Rollup-compatible API. [REPL](https://repl.rolldown.rs/).
- [rollup](https://github.com/rollup/rollup): JavaScript module bundler with TypeScript support. [REPL](https://rollupjs.org/repl/).
- [Rsbuild](https://github.com/web-infra-dev/rsbuild): Build tool using Rspack, SWC, and Lightning CSS.
- [Rslib](https://github.com/web-infra-dev/rslib): Library build tool based on Rsbuild and Rspack.
- [rspack](https://github.com/web-infra-dev/rspack): Webpack-compatible bundler written in Rust, with TypeScript support. [Playground](https://playground.rspack.rs/).
- [tsdown](https://github.com/rolldown/tsdown): TypeScript library bundler using Rolldown and Oxc. Also generates declaration files.
- [tsup](https://github.com/egoist/tsup): TypeScript library bundler using esbuild. No longer actively maintained; the maintainers recommend [tsdown](https://github.com/rolldown/tsdown).
- [Turbopack](https://github.com/vercel/next.js): Next.js's incremental bundler, written in Rust. Uses SWC to transpile TypeScript without checking types. [Docs](https://nextjs.org/docs/app/api-reference/turbopack).
- [vite](https://github.com/vitejs/vite): Frontend build tool with TypeScript support. [Playground](https://vite.new).
- [webpack](https://github.com/webpack/webpack): JavaScript bundler with TypeScript integration.

## Runtimes

- [Andromeda](https://github.com/tryandromeda/andromeda): JavaScript and TypeScript runtime written in Rust using the Nova engine. Runs TypeScript without configuration.
- [azle](https://github.com/demergent-labs/azle): Runs JavaScript and TypeScript in WebAssembly on the Internet Computer (ICP).
- [bun](https://github.com/oven-sh/bun): JavaScript and TypeScript runtime and toolkit written in Zig.
- [deno](https://github.com/denoland/deno): TypeScript runtime and toolkit written in Rust.
- [DeviceScript](https://github.com/microsoft/devicescript): Compiles a TypeScript subset to custom VM bytecode for IoT devices such as ESP32 and RP2040. Microsoft project; archived.
- [dune](https://github.com/aalykiot/dune): Hobby JavaScript and TypeScript runtime written in Rust using V8.
- [elide](https://github.com/elide-dev/elide): GraalVM-based runtime and toolchain with native support for TypeScript, JavaScript, Kotlin, and Python. [Playground](https://play.elide.dev/).
- [elsa](https://github.com/elsaland/elsa): Minimal JavaScript and TypeScript runtime written in Go.
- [LLRT](https://github.com/awslabs/llrt): AWS Labs' Low Latency Runtime for AWS Lambda. TypeScript must be bundled or transpiled ahead of time.
- [Node.js](https://github.com/nodejs/node): JavaScript runtime that strips erasable TypeScript syntax. Does not check types, read `tsconfig.json`, or support TSX. [Docs](https://nodejs.org/api/typescript.html).
- [txiki.js](https://github.com/saghul/txiki.js): Small JavaScript runtime built on QuickJS-ng and libuv. Provides TypeScript definitions through `@txikijs/types`.
- [yavascript](https://github.com/suchipi/yavascript): QuickJS-based scripting runtime with built-in TypeScript transpilation. Intended as a bash replacement.

<a name="loaders--execution-tools"></a>

## Loaders and type stripping

### Execution tools

- [esbuild-register](https://github.com/egoist/esbuild-register): Transpiles JSX, TypeScript, and ESNext on the fly using esbuild.
- [jiti](https://github.com/unjs/jiti): Runtime TypeScript and ESM support for Node.js.
- [swc-node](https://github.com/swc-project/swc-node): Runs TypeScript in Node.js without checking types.
- [ts-node](https://github.com/TypeStrong/ts-node): Runs TypeScript in Node.js and provides a REPL.
- [tsimp](https://github.com/tapjs/tsimp): Node.js import loader with type checking. Uses the official TypeScript implementation and aims to match `tsc`.
- [tsm](https://github.com/lukeed/tsm): TypeScript loader for `node <file>`, `--loader`, and `--require`.
- [tsx](https://github.com/privatenumber/tsx): Runs TypeScript through an esbuild-based ESM loader.
- [vite-node](https://github.com/antfu-collective/vite-node): Legacy Vite-based Node.js runtime with TypeScript support. The project recommends Vite's built-in Module Runner for new projects.

### Type strippers

- [Amaro](https://github.com/nodejs/amaro): Wrapper around `@swc/wasm-typescript`, used by Node.js to strip TypeScript types.
- [ts-blank-space](https://github.com/bloomberg/ts-blank-space): Type stripper written in JavaScript using the official TypeScript parser.

<a name="other-language-targets"></a>

## Language and platform targets

Some of these projects support only a TypeScript subset or a TypeScript-like language.

### WebAssembly and bytecode

- [AssemblyScript](https://github.com/AssemblyScript/assemblyscript): TypeScript-like language that compiles to WebAssembly. [Playground](https://www.assemblyscript.org/editor.html).
- [Porffor](https://github.com/CanadaHonk/porffor): Ahead-of-time compiler from JavaScript and TypeScript to WebAssembly and native binaries.
- [SharpTS](https://github.com/nickna/SharpTS): TypeScript interpreter and compiler written in C#. Supports ahead-of-time compilation to .NET IL.
- [speedy.js](https://github.com/MichaReiser/speedy.js): Compiles TypeScript to WebAssembly.
- [Wasmnizer-ts](https://github.com/web-devkits/Wasmnizer-ts): Compiles TypeScript to WebAssembly with garbage collection (WasmGC).

### Source-to-source transpilers

- [ast-transpiler](https://github.com/carlosmiei/ast-transpiler): AST-based transpiler from TypeScript to PHP, Python, C#, and Go. Work in progress.
- [poseidon](https://github.com/Turbin3/poseidon): Converts TypeScript Solana programs to Anchor programs in Rust.
- [roblox-ts](https://github.com/roblox-ts/roblox-ts): TypeScript-to-Luau compiler for Roblox. [Playground](https://roblox-ts.com/playground).
- [ts-swift-transpiler](https://github.com/marcelganczak/ts-swift-transpiler): Converts JavaScript and TypeScript to Swift using ANTLR.
- [ts2c](https://github.com/andrei-markeev/ts2c): Converts JavaScript and TypeScript to C. [Demo](https://andrei-markeev.github.io/ts2c/).
- [ts2dart](https://github.com/dart-archive/ts2dart): TypeScript-to-Dart transpiler.
- [ts2gd](https://github.com/johnfn/ts2gd): Compiles TypeScript to GDScript for Godot.
- [ts2go](https://github.com/leona/ts2go): Experimental TypeScript-to-Go transpiler. [Playground](https://ts2go.pages.dev/).
- [ts2haxe](https://github.com/Ezelia/ts2haxe): Converts TypeScript to Haxe.
- [ts2lua](https://github.com/TypeScriptToLua/TypeScriptToLua): Compiles TypeScript to Lua. [Playground](https://typescripttolua.github.io/play/).
- [ts2nim](https://github.com/bung87/ts2nim): TypeScript-to-Nim transpiler.
- [ts2php](https://github.com/searchfe/ts2php): TypeScript-to-PHP transpiler.
- [ts2py](https://github.com/chayleaf/ts2py): TypeScript-to-Python converter.
- [ts2rust](https://github.com/vedantroy/ts2rust): TypeScript-to-Rust transpiler.
- [TypeScript2Cxx](https://github.com/ASDAlexander77/TypeScript2Cxx): TypeScript-to-C++ transpiler.

### Shader generation

- [TypeGPU](https://github.com/software-mansion/TypeGPU): Turns GPU-targeted TypeScript functions into WGSL shaders for WebGPU. [Docs](https://docs.swmansion.com/TypeGPU/).
- [typesl](https://github.com/SieR-VR/typesl): TypeScript-to-GLSL transpiler.

### Bindings and framework integrations

- [hydro-sdk](https://github.com/hydro-sdk/hydro-sdk): Dart-based toolkit for Flutter, without a native bridge or V8.
- [jsii](https://github.com/aws/jsii): Makes TypeScript libraries usable from Python, Java, C#/.NET, Go, and other languages.
- [Karakum](https://github.com/karakum-team/karakum): Converts TypeScript declaration files to Kotlin declarations.

<a name="experimentalresearch-projects"></a>

## Research and education

### Native compiler experiments

- [muta-minits](https://github.com/nervosnetwork/muta-minits): TypeScript-to-LLVM compiler from Nervos Network for the Muta blockchain framework. Archived.
- [scriptc](https://github.com/vercel-labs/scriptc): Experimental JavaScript and TypeScript compiler that emits LLVM IR for native executables and WebAssembly modules.
- [ts-llvm](https://github.com/emillaine/ts-llvm): Compiles TypeScript to LLVM IR for ahead-of-time native compilation. Archived.
- [tsCompiler](https://github.com/ASDAlexander77/TypeScriptCompiler): Compiles TypeScript to native code using LLVM.
- [TypeRunner](https://github.com/marcj/TypeRunner): Experimental compiler from TypeScript to native code.

### Research languages

- [BosqueLang](https://github.com/microsoft/BosqueLanguage): TypeScript-like research language from Microsoft.
- [StaticScript](https://github.com/StaticScript/StaticScript): Statically typed research language with native compilation.

### Educational and type-level projects

- [mini-typescript](https://github.com/sandersn/mini-typescript): Small model of the TypeScript compiler for learning how the real compiler works.
- [typescript-types-only-wasm-runtime](https://github.com/MichiganTypeScript/typescript-types-only-wasm-runtime): WebAssembly runtime implemented entirely in TypeScript types.
- [tyvm](https://github.com/zackradisic/tyvm): Experimental bytecode interpreter and type checker for type-level TypeScript, written in Zig.

## Related tooling

- [biome](https://github.com/biomejs/biome): JavaScript and TypeScript formatter and linter written in Rust. [Playground](https://biomejs.dev/playground/).

## Contributing

Open a pull request to add a project or fix an entry. Include the repository link
and a sentence about what it does. Keep each group alphabetical, and mention any
known compatibility limits or maintenance issues.
