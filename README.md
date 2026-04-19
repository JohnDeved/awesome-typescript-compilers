# Awesome TypeScript Compilers, Transpilers and Runtimes
A curated list of TypeScript compilers, transpilers and runtimes targeting various languages and platforms.

## JavaScript Targets
| Project | Description |
|-|-|
| [tsc](https://github.com/microsoft/TypeScript) | Official TypeScript compiler by Microsoft. ([playground](https://www.typescriptlang.org/play)) |
| [tsgo](https://github.com/microsoft/typescript-go) | Go-based TypeScript compiler by Microsoft targeting 10x performance. |
| [swc](https://github.com/swc-project/swc) | Rust-based platform for fast TypeScript/JavaScript compilation. ([playground](https://swc.rs/playground)) |
| [esbuild](https://github.com/evanw/esbuild) | Extremely fast TypeScript/JavaScript bundler written in Go. ([playground](https://esbuild.github.io/try/)) |
| [vite](https://github.com/vitejs/vite) | Next generation frontend tooling with TypeScript support. ([playground](https://vite.new)) |
| [rspack](https://github.com/web-infra-dev/rspack) | Rust-based Webpack-compatible bundler with TypeScript support. |
| [Turbopack](https://github.com/vercel/turbo) | Rust-based incremental bundler with zero-config TypeScript support in Next.js. |
| [Rsbuild](https://github.com/web-infra-dev/rsbuild) | Fast build tool that integrates Rspack, SWC, and Lightning CSS. |
| [Rslib](https://github.com/web-infra-dev/rslib) | Library development tool built on top of Rsbuild/Rspack. |
| [biome](https://github.com/biomejs/biome) | Successor to Rome providing a unified TypeScript toolchain. ([playground](https://biomejs.dev/playground/)) |
| [rolldown](https://github.com/rolldown/rolldown) | Fast Rust bundler for JavaScript/TypeScript with Rollup-compatible API. ([repl](https://repl.rolldown.rs/)) |
| [tsdown](https://github.com/rolldown/tsdown) | Library bundler powered by Rolldown and Oxc; builds TypeScript and generates declaration files. |
| [farm](https://github.com/farm-fe/farm) | Extremely fast Vite-compatible web build tool written in Rust. |
| [Mako](https://github.com/umijs/mako) | Rust-based web bundler for apps, libraries, and frameworks. ([playground](https://utoo-repl.vercel.app/)) |
| [oxc](https://github.com/oxc-project/oxc) | Rust-based JavaScript/TypeScript toolchain including parser, linter, and compiler. ([playground](https://playground.oxc.rs/)) |
| [swc4j](https://github.com/caoccao/swc4j) | JVM-facing TypeScript/JavaScript compilation and bundling tool built around SWC. |
| [webpack](https://github.com/webpack/webpack) | JavaScript bundler with TypeScript integration. |
| [rollup](https://github.com/rollup/rollup) | JavaScript module bundler with TypeScript support. ([repl](https://rollupjs.org/repl/)) |
| [parcel](https://github.com/parcel-bundler/parcel) | Zero configuration web app bundler with TypeScript support. ([repl](https://repl.parceljs.org/)) |
| [tsup](https://github.com/egoist/tsup) | TypeScript bundler powered by esbuild. |
| [babel](https://github.com/babel/babel) | The compiler for next generation JavaScript with TypeScript support. ([playground](https://babeljs.io/repl)) |
| [sucrase](https://github.com/alangpierce/sucrase) | Super-fast alternative to Babel focusing on modern JS runtimes. ([playground](https://sucrase.io/)) |
| [ezno](https://github.com/kaleidawave/ezno) | JavaScript compiler and TypeScript checker in Rust focusing on static analysis. ([playground](https://kaleidawave.github.io/ezno/playground/)) |
| [stc](https://github.com/dudykr/stc) | Rust-based static type checker for TypeScript focusing on performance. |

## Runtimes
| Project | Description |
|-|-|
| [deno](https://github.com/denoland/deno) | Secure TypeScript runtime & toolkit written in Rust. |
| [bun](https://github.com/oven-sh/bun) | Fast JavaScript and TypeScript runtime & toolkit written in Zig. |
| [node.js 23.6.0+](https://github.com/nodejs/node/pull/56450) | Partial support in 23.6.0 |
| [elsa](https://github.com/elsaland/elsa) | Minimal runtime for JavaScript and TypeScript written in Go. |
| [elide](https://github.com/elide-dev/elide) | Polyglot runtime and toolchain with native TypeScript, JavaScript, Kotlin, and Python support, built on GraalVM. ([playground](https://play.elide.dev/)) |
| [yavascript](https://github.com/suchipi/yavascript) | QuickJS-based scripting runtime with built-in TypeScript transpilation, designed as a bash replacement. |
| [txiki.js](https://github.com/saghul/txiki.js) | Tiny JavaScript runtime built on QuickJS-ng and libuv, with TypeScript type definitions via `@txikijs/types`. |
| [LLRT](https://github.com/awslabs/llrt) | Low Latency Runtime for AWS Lambda by AWS Labs; runs TypeScript when bundled/transpiled ahead of time. |

## Loaders / Execution Tools
| Project | Description |
|-|-|
| [tsx](https://github.com/privatenumber/tsx) | Run TypeScript with an esbuild-powered ESM loader. |
| [ts-node](https://github.com/TypeStrong/ts-node) | TypeScript execution and REPL for Node.js. |
| [ts-blank-space](https://github.com/bloomberg/ts-blank-space) | Small, fast, pure-JS type-stripper that uses the official TypeScript parser. |
| [@swc-node/register / swc-node](https://github.com/swc-project/swc-node) | Fast Node runtime path for TypeScript without typechecking. |
| [esbuild-register](https://github.com/egoist/esbuild-register) | On-the-fly JSX/TypeScript/esnext transpilation with esbuild. |
| [tsm](https://github.com/lukeed/tsm) | TypeScript module loader supporting `node <file>`, `--loader`, and `--require`. |
| [tsimp](https://github.com/tapjs/tsimp) | Node import loader that uses the official TypeScript implementation and aims for `tsc` consistency with typechecking. |
| [Amaro](https://github.com/nodejs/amaro) | Node.js TypeScript wrapper around `@swc/wasm-typescript`, used internally for Node’s type stripping. |
| [vite-node](https://github.com/antfu-collective/vite-node) | Legacy Vite-powered Node runtime with TS support; new projects are now directed to Vite’s built-in Module Runner. |
| [jiti](https://github.com/unjs/jiti) | Runtime TypeScript and ESM support for Node.js. |

## Other Language Targets
| Project | Target | Description |
|-|-|-|
| [AssemblyScript](https://github.com/AssemblyScript/assemblyscript) | `WASM` | TypeScript-like language for WebAssembly. ([playground](https://www.assemblyscript.org/editor.html)) |
| [ts2lua](https://github.com/TypeScriptToLua/TypeScriptToLua) | `Lua` | Feature-complete TypeScript to Lua compiler. ([playground](https://typescripttolua.github.io/play/)) |
| [roblox-ts](https://github.com/roblox-ts/roblox-ts) | `Luau` | TypeScript-to-Luau compiler for Roblox. ([playground](https://roblox-ts.com/playground)) |
| [ts2c](https://github.com/andrei-markeev/ts2c) | `C` | Convert Javascript/TypeScript to C ([online demo](https://andrei-markeev.github.io/ts2c/)) |
| [TypeScript2Cxx](https://github.com/ASDAlexander77/TypeScript2Cxx) | `C++` | TypeScript to C++ transpiler. |
| [ts2gd](https://github.com/johnfn/ts2gd) | `GDScript` | Compile TypeScript to GDScript for Godot. |
| [typesl](https://github.com/SieR-VR/typesl) | `GLSL` | Typescript to GLSL transpiler. |
| [hydro-sdk](https://github.com/hydro-sdk/hydro-sdk) | `Flutter` | No native bridge, no V8. Just Dart. |
| [jsii](https://github.com/aws/jsii) | `Python/Java/C#/.NET/Go/...` | Lets you author libraries in TypeScript and consume them from Python, Java, C#/.NET, Go, and more. |
| [ts2nim](https://github.com/bung87/ts2nim) | `Nim` | Typescript to Nim transpiler. |
| [ts2dart](https://github.com/dart-archive/ts2dart) | `Dart` | TypeScript to Dart transpiler. |
| [SharpTS](https://github.com/nickna/SharpTS) | `.NET IL` | TypeScript interpreter/compiler in C# with ahead-of-time compilation to .NET IL. |
| [speedy.js](https://github.com/MichaReiser/speedy.js) | `WASM` | Compile TypeScript to WebAssembly for accelerated execution. |
| [ts2rust](https://github.com/vedantroy/ts2rust) | `Rust` | Typescript to Rust transpiler. |
| [ts2php](https://github.com/searchfe/ts2php) | `PHP` | Typescript to PHP Transpiler. |
| [ts2py](https://github.com/chayleaf/ts2py) | `Python` | TypeScript to Python converter. |
| [ast-transpiler](https://github.com/carlosmiei/ast-transpiler) | `PHP/Python/C#/Go` | Work-in-progress AST-based transpiler from TypeScript to PHP, Python, C#, and Go. |
| [Karakum](https://github.com/karakum-team/karakum) | `Kotlin` | Converts TypeScript declaration files into Kotlin declarations. |
| [Porffor](https://github.com/CanadaHonk/porffor) | `WASM/Native` | Ahead-of-time JavaScript/TypeScript compiler producing WebAssembly and native binaries. |
| [ts2go](https://github.com/leona/ts2go) | `Go` | Experimental TypeScript to Go transpiler. ([playground](https://ts2go.pages.dev/)) |
| [ts-swift-transpiler](https://github.com/marcelganczak/ts-swift-transpiler) | `Swift` | JavaScript/TypeScript to Swift transpiler built with ANTLR. |

## Experimental/Research Projects
| Project | Type | Description |
|-|-|-|
| [BosqueLang](https://github.com/microsoft/BosqueLanguage) | `Research Language` | A TypeScript-like language created by Microsoft. |
| [TypeRunner](https://github.com/marcj/TypeRunner) | `Native Compiler` | Experimental TypeScript to native code compiler. |
| [StaticScript](https://github.com/StaticScript/StaticScript) | `Research Language` | A new statically typed programming language with native compilation. |
| [tsCompiler](https://github.com/ASDAlexander77/TypeScriptCompiler) | `Native Compiler` | TypeScript to native code compiler using LLVM. |
| [ts-llvm](https://github.com/emillaine/ts-llvm) | `Native Compiler` | TypeScript to LLVM IR compiler enabling AOT native compilation (archived). |
