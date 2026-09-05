# Awesome TypeScript Compilers, Transpilers and Runtimes

A curated guide to the TypeScript toolchain: type checkers, transpilers, bundlers,
runtimes, and projects targeting other languages and platforms.

## Contents

- [JavaScript toolchain](#javascript-toolchain)
  - [Compilers and type checkers](#compilers-and-type-checkers)
  - [Transpilers and compiler toolkits](#transpilers-and-compiler-toolkits)
  - [Bundlers and build tools](#bundlers-and-build-tools)
- [Runtimes](#runtimes)
- [Loaders and type stripping](#loaders-and-type-stripping)
  - [Execution tools](#execution-tools)
  - [Type strippers](#type-strippers)
- [Language and platform targets](#language-and-platform-targets)
  - [WebAssembly and bytecode](#webassembly-and-bytecode)
  - [Source-to-source transpilers](#source-to-source-transpilers)
  - [Shader generation](#shader-generation)
  - [Bindings and framework integrations](#bindings-and-framework-integrations)
- [Research and education](#research-and-education)
  - [Native compiler experiments](#native-compiler-experiments)
  - [Research languages](#research-languages)
  - [Educational and type-level projects](#educational-and-type-level-projects)
- [Related tooling](#related-tooling)
- [Contributing](#contributing)

## How to read this list

Projects appear once, grouped by their primary role and sorted alphabetically by
name within each group (case-insensitive). Target languages and platforms appear
in parentheses where relevant. **Archived**, **Not actively maintained**, and
**Legacy** labels retain known caveats; an unlabeled entry is not a maintenance
guarantee.

> **Type checking is not transpilation.** Running or transpiling TypeScript does
> not necessarily check types. For example, [esbuild](https://esbuild.github.io/content-types/#typescript)
> and [Node.js type stripping](https://nodejs.org/api/typescript.html#type-stripping)
> do not perform type checking; use a separate checker such as `tsc --noEmit`.

<a name="javascript-targets"></a>

## JavaScript toolchain

Tools for checking TypeScript or producing JavaScript. Projects with overlapping
capabilities are listed under their primary role.

### Compilers and type checkers

- **[ezno](https://github.com/kaleidawave/ezno)** — JavaScript compiler and TypeScript checker in Rust focusing on static analysis. [Playground](https://kaleidawave.github.io/ezno/playground/).
- **[stc](https://github.com/dudykr/stc)** — **Archived.** Rust-based static type checker for TypeScript focusing on performance.
- **[tsc](https://github.com/microsoft/TypeScript)** — Official TypeScript compiler by Microsoft. [Playground](https://www.typescriptlang.org/play).
- **[tsgo](https://github.com/microsoft/typescript-go)** — Go-based TypeScript compiler by Microsoft targeting 10x performance.

### Transpilers and compiler toolkits

- **[babel](https://github.com/babel/babel)** — JavaScript compiler with TypeScript support. [Playground](https://babeljs.io/repl).
- **[oxc](https://github.com/oxc-project/oxc)** — Rust-based JavaScript/TypeScript toolchain including parser, linter, and compiler. [Playground](https://playground.oxc.rs/).
- **[sucrase](https://github.com/alangpierce/sucrase)** — Babel alternative focused on modern JavaScript runtimes. [Playground](https://sucrase.io/).
- **[swc](https://github.com/swc-project/swc)** — Rust-based platform for fast TypeScript/JavaScript compilation. [Playground](https://swc.rs/playground).
- **[swc4j](https://github.com/caoccao/swc4j)** — JVM-facing TypeScript/JavaScript compilation and bundling tool built around SWC.

### Bundlers and build tools

- **[esbuild](https://github.com/evanw/esbuild)** — Go-based JavaScript/TypeScript bundler. [Playground](https://esbuild.github.io/try/).
- **[farm](https://github.com/farm-fe/farm)** — Rust-based, Vite-compatible web build tool.
- **[Mako](https://github.com/umijs/mako)** — Rust-based web bundler for apps, libraries, and frameworks. [Playground](https://utoo-repl.vercel.app/).
- **[parcel](https://github.com/parcel-bundler/parcel)** — Zero-configuration web app bundler with TypeScript support. [REPL](https://repl.parceljs.org/).
- **[rolldown](https://github.com/rolldown/rolldown)** — Fast Rust bundler for JavaScript/TypeScript with Rollup-compatible API. [REPL](https://repl.rolldown.rs/).
- **[rollup](https://github.com/rollup/rollup)** — JavaScript module bundler with TypeScript support. [REPL](https://rollupjs.org/repl/).
- **[Rsbuild](https://github.com/web-infra-dev/rsbuild)** — Fast build tool that integrates Rspack, SWC, and Lightning CSS.
- **[Rslib](https://github.com/web-infra-dev/rslib)** — Library development tool built on top of Rsbuild/Rspack.
- **[rspack](https://github.com/web-infra-dev/rspack)** — Rust-based Webpack-compatible bundler with TypeScript support. [Playground](https://playground.rspack.rs/).
- **[tsdown](https://github.com/rolldown/tsdown)** — Library bundler powered by Rolldown and Oxc; builds TypeScript and generates declaration files.
- **[tsup](https://github.com/egoist/tsup)** — **Not actively maintained.** TypeScript library bundler powered by esbuild. The project recommends [tsdown](https://github.com/rolldown/tsdown).
- **[Turbopack](https://github.com/vercel/next.js)** — Rust-based incremental bundler integrated into Next.js; transpiles TypeScript with SWC without type checking. [Docs](https://nextjs.org/docs/app/api-reference/turbopack).
- **[vite](https://github.com/vitejs/vite)** — Frontend tooling with TypeScript support. [Playground](https://vite.new).
- **[webpack](https://github.com/webpack/webpack)** — JavaScript bundler with TypeScript integration.

## Runtimes

Standalone and platform-specific execution environments. TypeScript support
varies: some run it directly, while others require precompiled JavaScript or
provide type definitions rather than native TypeScript execution.

- **[Andromeda](https://github.com/tryandromeda/andromeda)** — JavaScript and TypeScript runtime in Rust built on the Nova engine, with zero-config TypeScript support.
- **[azle](https://github.com/demergent-labs/azle)** — WebAssembly runtime for TypeScript and JavaScript on the Internet Computer (ICP).
- **[bun](https://github.com/oven-sh/bun)** — Fast JavaScript and TypeScript runtime and toolkit written in Zig.
- **[deno](https://github.com/denoland/deno)** — Secure TypeScript runtime and toolkit written in Rust.
- **[DeviceScript](https://github.com/microsoft/devicescript)** — **Archived.** Microsoft project that compiles a subset of TypeScript to custom VM bytecode for small IoT devices, including ESP32 and RP2040.
- **[dune](https://github.com/aalykiot/dune)** — Hobby JavaScript and TypeScript runtime built on V8 in Rust.
- **[elide](https://github.com/elide-dev/elide)** — Polyglot runtime and toolchain with native TypeScript, JavaScript, Kotlin, and Python support, built on GraalVM. [Playground](https://play.elide.dev/).
- **[elsa](https://github.com/elsaland/elsa)** — Minimal runtime for JavaScript and TypeScript written in Go.
- **[LLRT](https://github.com/awslabs/llrt)** — Low Latency Runtime for AWS Lambda by AWS Labs; runs TypeScript when bundled/transpiled ahead of time.
- **[Node.js](https://github.com/nodejs/node)** — JavaScript runtime with built-in TypeScript type stripping for erasable syntax; does not type-check, read `tsconfig.json`, or support TSX. [Docs](https://nodejs.org/api/typescript.html).
- **[txiki.js](https://github.com/saghul/txiki.js)** — Tiny JavaScript runtime built on QuickJS-ng and libuv, with TypeScript type definitions via `@txikijs/types`.
- **[yavascript](https://github.com/suchipi/yavascript)** — QuickJS-based scripting runtime with built-in TypeScript transpilation, designed as a bash replacement.

<a name="loaders--execution-tools"></a>

## Loaders and type stripping

Tools for executing TypeScript in Node.js, plus libraries that remove type syntax.

### Execution tools

- **[esbuild-register](https://github.com/egoist/esbuild-register)** — On-the-fly JSX/TypeScript/esnext transpilation with esbuild.
- **[jiti](https://github.com/unjs/jiti)** — Runtime TypeScript and ESM support for Node.js.
- **[swc-node](https://github.com/swc-project/swc-node)** — Node.js execution tool for TypeScript without type checking.
- **[ts-node](https://github.com/TypeStrong/ts-node)** — TypeScript execution and REPL for Node.js.
- **[tsimp](https://github.com/tapjs/tsimp)** — Node.js import loader using the official TypeScript implementation, with type checking and a focus on `tsc` consistency.
- **[tsm](https://github.com/lukeed/tsm)** — TypeScript module loader supporting `node <file>`, `--loader`, and `--require`.
- **[tsx](https://github.com/privatenumber/tsx)** — Run TypeScript with an esbuild-powered ESM loader.
- **[vite-node](https://github.com/antfu-collective/vite-node)** — **Legacy.** Vite-powered Node.js runtime with TypeScript support; new projects are directed to Vite’s built-in Module Runner.

### Type strippers

- **[Amaro](https://github.com/nodejs/amaro)** — Node.js TypeScript wrapper around `@swc/wasm-typescript`, used internally for Node’s type stripping.
- **[ts-blank-space](https://github.com/bloomberg/ts-blank-space)** — Small, fast, pure-JavaScript type stripper that uses the official TypeScript parser.

<a name="other-language-targets"></a>

## Language and platform targets

Projects targeting other languages, virtual machines, and frameworks. Scope
varies from TypeScript-like languages and supported subsets to declaration
conversion and cross-language library access; inclusion does not imply full
TypeScript compatibility.

### WebAssembly and bytecode

- **[AssemblyScript](https://github.com/AssemblyScript/assemblyscript)** (WebAssembly) — TypeScript-like language for WebAssembly. [Playground](https://www.assemblyscript.org/editor.html).
- **[Porffor](https://github.com/CanadaHonk/porffor)** (WebAssembly / native) — Ahead-of-time JavaScript/TypeScript compiler producing WebAssembly and native binaries.
- **[SharpTS](https://github.com/nickna/SharpTS)** (.NET IL) — TypeScript interpreter/compiler in C# with ahead-of-time compilation to .NET IL.
- **[speedy.js](https://github.com/MichaReiser/speedy.js)** (WebAssembly) — Compile TypeScript to WebAssembly for accelerated execution.
- **[Wasmnizer-ts](https://github.com/web-devkits/Wasmnizer-ts)** (WasmGC) — Toolchain for compiling TypeScript to WebAssembly with GC support.

### Source-to-source transpilers

- **[ast-transpiler](https://github.com/carlosmiei/ast-transpiler)** (PHP / Python / C# / Go) — Work-in-progress AST-based transpiler from TypeScript to PHP, Python, C#, and Go.
- **[poseidon](https://github.com/Turbin3/poseidon)** (Rust / Anchor) — Transpiler that converts TypeScript Solana programs into Anchor (Rust).
- **[roblox-ts](https://github.com/roblox-ts/roblox-ts)** (Luau) — TypeScript-to-Luau compiler for Roblox. [Playground](https://roblox-ts.com/playground).
- **[ts-swift-transpiler](https://github.com/marcelganczak/ts-swift-transpiler)** (Swift) — JavaScript/TypeScript to Swift transpiler built with ANTLR.
- **[ts2c](https://github.com/andrei-markeev/ts2c)** (C) — JavaScript/TypeScript to C converter. [Demo](https://andrei-markeev.github.io/ts2c/).
- **[ts2dart](https://github.com/dart-archive/ts2dart)** (Dart) — TypeScript to Dart transpiler.
- **[ts2gd](https://github.com/johnfn/ts2gd)** (GDScript) — Compile TypeScript to GDScript for Godot.
- **[ts2go](https://github.com/leona/ts2go)** (Go) — Experimental TypeScript to Go transpiler. [Playground](https://ts2go.pages.dev/).
- **[ts2haxe](https://github.com/Ezelia/ts2haxe)** (Haxe) — TypeScript to Haxe converter that automates common conversion tasks.
- **[ts2lua](https://github.com/TypeScriptToLua/TypeScriptToLua)** (Lua) — Feature-complete TypeScript to Lua compiler. [Playground](https://typescripttolua.github.io/play/).
- **[ts2nim](https://github.com/bung87/ts2nim)** (Nim) — TypeScript to Nim transpiler.
- **[ts2php](https://github.com/searchfe/ts2php)** (PHP) — TypeScript to PHP transpiler.
- **[ts2py](https://github.com/chayleaf/ts2py)** (Python) — TypeScript to Python converter.
- **[ts2rust](https://github.com/vedantroy/ts2rust)** (Rust) — TypeScript to Rust transpiler.
- **[TypeScript2Cxx](https://github.com/ASDAlexander77/TypeScript2Cxx)** (C++) — TypeScript to C++ transpiler.

### Shader generation

- **[TypeGPU](https://github.com/software-mansion/TypeGPU)** (WGSL) — Generates WGSL shaders from GPU-targeted TypeScript functions for WebGPU. [Docs](https://docs.swmansion.com/TypeGPU/).
- **[typesl](https://github.com/SieR-VR/typesl)** (GLSL) — TypeScript to GLSL transpiler.

### Bindings and framework integrations

- **[hydro-sdk](https://github.com/hydro-sdk/hydro-sdk)** (Flutter) — Dart-based toolkit for Flutter without a native bridge or V8.
- **[jsii](https://github.com/aws/jsii)** (Python / Java / C# / .NET / Go / more) — Lets you author libraries in TypeScript and consume them from Python, Java, C#/.NET, Go, and more.
- **[Karakum](https://github.com/karakum-team/karakum)** (Kotlin) — Converts TypeScript declaration files into Kotlin declarations.

<a name="experimentalresearch-projects"></a>

## Research and education

Native compiler experiments, research languages, and projects exploring compiler
internals or type-level execution.

### Native compiler experiments

- **[muta-minits](https://github.com/nervosnetwork/muta-minits)** — **Archived.** TypeScript to LLVM compiler from Nervos Network for the Muta blockchain framework.
- **[scriptc](https://github.com/vercel-labs/scriptc)** — Experimental TypeScript/JavaScript compiler that emits LLVM IR for native executables and WebAssembly modules.
- **[ts-llvm](https://github.com/emillaine/ts-llvm)** — **Archived.** TypeScript to LLVM IR compiler enabling AOT native compilation.
- **[tsCompiler](https://github.com/ASDAlexander77/TypeScriptCompiler)** — TypeScript to native code compiler using LLVM.
- **[TypeRunner](https://github.com/marcj/TypeRunner)** — Experimental TypeScript to native code compiler.

### Research languages

- **[BosqueLang](https://github.com/microsoft/BosqueLanguage)** — A TypeScript-like language created by Microsoft.
- **[StaticScript](https://github.com/StaticScript/StaticScript)** — Statically typed research language with native compilation.

### Educational and type-level projects

- **[mini-typescript](https://github.com/sandersn/mini-typescript)** — A miniature model of the TypeScript compiler intended to teach the structure of the real one.
- **[typescript-types-only-wasm-runtime](https://github.com/MichiganTypeScript/typescript-types-only-wasm-runtime)** — A WebAssembly runtime implemented entirely in TypeScript types.
- **[tyvm](https://github.com/zackradisic/tyvm)** — Experimental bytecode interpreter / type-checker for type-level TypeScript, written in Zig.

## Related tooling

Complementary tools rather than compilers or runtimes.

- **[biome](https://github.com/biomejs/biome)** — Rust-based formatter and linter for JavaScript/TypeScript, complementary to compilers and runtimes. [Playground](https://biomejs.dev/playground/).

## Contributing

Suggest an addition or correction with a pull request. Choose the best-fitting
category, keep entries alphabetized by project name, and include a repository
link with a concise description. Preserve relevant target, compatibility, and
maintenance notes; include a playground, REPL, demo, or documentation link when
useful.
