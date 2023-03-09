I need to use git in browser to do a shallow clone.

Read [here](https://github.com/nikitavoloboev/wasm-git) for why this repo exists.

To get `libgit2` repo I did:

```
git clone https://github.com/libgit2/libgit2
gh pr checkout 6396 # gh is github CLI https://cli.github.com
```

It has the sparse clone feature support.

`libgit2-git-wasm-working-version` is version that [wasm-git](https://github.com/petersalomonsen/wasm-git) uses which works. Can get it via

```
curl -L https://github.com/libgit2/libgit2/archive/refs/tags/v1.5.0.tar.gz --output libgit2.tar.gz
tar -xzf libgit2.tar.gz
```
