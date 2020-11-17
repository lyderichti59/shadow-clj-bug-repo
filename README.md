# This repository aims at reproducing bugs 

## Project architecture

This project has been created with `npx create-shadow-cljs-app cljs-app`.

## Currently repoducible bugs

* No error/warning when an `:after-load` hook is unresolvable.
    - Reproduce : Watch build `:undefined-reload-hook`
        + Affect a wrong reference to the shadow-cljs build's `[:devtools :after-load]`
        + Try to watch the build and modify `*.cljs` sources.
    - Expected : a warning/error message in the console saying that the hook   `undefined.ns/hook` could not be resolved
    - Error : Nothing gets logged thus the problem is hard to detect.
