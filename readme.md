I need to use git in browser to do a shallow clone. Currently using [Wasm-git](https://github.com/petersalomonsen/wasm-git) for this but there is an issue.

[libgit2 does not support shall clones](https://github.com/libgit2/libgit2/issues/3058). [There is PR for it](https://github.com/libgit2/libgit2/pull/6396) though.

This repo is attempt at compiling that PR with wasm-git.

Following [these instructions](https://github.com/petersalomonsen/wasm-git/blob/master/.github/workflows/main.yml#L24). So instead of:

`curl -L https://github.com/libgit2/libgit2/archive/refs/tags/v1.5.0.tar.gz --output libgit2.tar.gz`

I did:

```
git clone https://github.com/libgit2/libgit2
gh pr checkout 6396 # gh is github CLI https://cli.github.com
```

Then moved the `libigt2` output to this folder.

So `libig2` folder is one that should have the sparse clone feature support. And `libgit2-git-wasm-working-version` is version that [wasm-git](https://github.com/petersalomonsen/wasm-git) uses which works.

Will try run the other instructions in setup and build, hopefully the things that will most likely break are fixable.
