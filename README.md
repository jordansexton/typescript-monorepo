# Exodus bugbounty POC by @nvk0x
# POC: Supply Chain Vulnerability in Exodus Bitcoin Wallet Dependency

This is a simple monorepo template with the following design goals:

- Latest TypeScript version  
- Fast, incremental dependency updates and builds  
- No package bundler  
- Watch mode support  
- ESM and CJS compatibility (distinct build outputs)  
- Works with Vanilla TS, React, CRA (via react-app-rewired), and Parcel (with HMR)  

## Prerequisites

-   Node 16+
-   PNPM

If you have Node 16+, you can [activate PNPM with Corepack](https://pnpm.io/installation#using-corepack):

```shell
corepack enable
corepack prepare pnpm@`npm info pnpm --json | jq -r .version` --activate
```

Corepack requires a version to enable, so if you don't have [jq](https://stedolan.github.io/jq/) installed, you can [install it](https://formulae.brew.sh/formula/jq), or just manually get the current version of pnpm with `npm info pnpm` and use it like this:

```shell
corepack prepare pnpm@7.13.4 --activate
```

## Setup

```shell
pnpm install
```

## Build

Run this to build all your workspace packages.

```shell
git clone https://github.com/jordansexton/typescript-monorepo.git
cd typescript-monorepo
pnpm build
```

This will build workspace packages that use `tsc` for compilation first, then everything else.

## Watch

Run this to build and watch workspace packages that use `tsc` for compilation.

```shell
pnpm watch
```
