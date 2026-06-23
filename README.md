## Install
```
npm i @ecubelabs/tsconfig
```

## Usage

### Modern Resolution presets (CommonJS runtime)

These presets keep the **CommonJS** emit/runtime exactly as the legacy presets, but
modernize only the module resolution (`module: "node20"`, no `moduleResolution` → auto
`node16`). This honors the `exports`/`imports` fields in dependencies' `package.json`,
fixing resolution failures with modern packages — **without** any source/ESM migration.

> Do **not** add `"type": "module"` to your `package.json`; that keeps the emit as CommonJS.
>
> Switching to modern resolution also implicitly enables `esModuleInterop`,
> `allowSyntheticDefaultImports`, and `moduleDetection: "force"`. This is non-breaking
> (emit stays CJS) but changes resolution/interop behavior, so run `tsc --noEmit` once
> to verify after switching. Requires `typescript>=5.9`.

#### Node 22 (Modern) <kbd><a href="./node22-modern.json">tsconfig.json</a></kbd>
```
"extends": "@ecubelabs/tsconfig/node22-modern.json"
```

#### Node 20 (Modern) <kbd><a href="./node20-modern.json">tsconfig.json</a></kbd>
```
"extends": "@ecubelabs/tsconfig/node20-modern.json"
```

### Node 22 <kbd><a href="./node22.json">tsconfig.json</a></kbd>
Add to your `tsconfig.json`
This tsconfig requires typescript>=5.7
```
"extends": "@ecubelabs/tsconfig/node22.json"
```

### Node 20 <kbd><a href="./node20.json">tsconfig.json</a></kbd>
Add to your `tsconfig.json`
This tsconfig requires typescript>=5
```
"extends": "@ecubelabs/tsconfig/node20.json"
```

### Node 18 <kbd><a href="./node18.json">tsconfig.json</a></kbd>
Add to your `tsconfig.json`
```
"extends": "@ecubelabs/tsconfig/node18.json"
```

### Node 16 <kbd><a href="./node16.json">tsconfig.json</a></kbd>
Add to your `tsconfig.json`
```
"extends": "@ecubelabs/tsconfig/node16.json"
```

### Node 14 <kbd><a href="./node14.json">tsconfig.json</a></kbd>
Add to your `tsconfig.json`
```
"extends": "@ecubelabs/tsconfig/node14.json"
```

### Node 12 <kbd><a href="./node12.json">tsconfig.json</a></kbd>
Add to your `tsconfig.json`
```
"extends": "@ecubelabs/tsconfig/node12.json"
```

### Node 10 <kbd><a href="./node10.json">tsconfig.json</a></kbd>
Add to your `tsconfig.json`
```
"extends": "@ecubelabs/tsconfig/node10.json"
```
