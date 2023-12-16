To reproduce run:
```
yarn
yarn run lint1 # This prints out an error:
yarn run lint2 # This does not print out an error
```

Sample output:
```
> yarn run lint1
yarn run v1.22.21
$ npx unimported@1.31.0

       summary               unimported v1.31.0 (node)
───────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────
       entry file          : main.ts

       unresolved imports  : 1
       unused dependencies : 0
       unimported files    : 0


─────┬─────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────
     │ 1 unresolved imports
─────┼─────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────
   1 │ geojson at types.ts
─────┴─────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────────


       Inspect the results and run npx unimported -u to update ignore lists
error Command failed with exit code 1.
info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.
[08:59:53] jason@linux-mint-desktop /home/jason/dev/tmp/unimported-repro [1]
> yarn run lint2
yarn run v1.22.21
$ npx unimported@1.30.0
✓ There don't seem to be any unimported files.
Done in 1.88s.
```
