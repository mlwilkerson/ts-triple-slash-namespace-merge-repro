# On the `master` branch:
```
tsc
node main.js
```

EXPECTED:
- `tsc` compiles without error
- `node main.js` produces output:
```
color: red
```

ACTUAL: as expected

# On the `triple-slash` branch:
```
git checkout triple-slash
./clean.sh
tsc
```

EXPECTED: `tsc` compiles without error

ACTUAL: `tsc` has an error:

```
main.ts(1,9): error TS2305: Module '"/Users/mike/repos/ts-triple-slash-import-problem/node_modules/foo/index"' has no exported member 'Color'.
node_modules/foo/index.d.ts(5,21): error TS2304: Cannot find name 'Color'.
```
