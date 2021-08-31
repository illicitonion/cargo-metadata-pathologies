# binary-deps

When a crate has a dependency on a bin-only crate, the bin crate has the following deficiencies:
1. It doesn't appear in the `packages` key.
2. Its dependencies don't appear in the `packages` key.
3. It and its dependencies don't appear in the `resolve` key.
4. Its dependencies list in the `resolve` key doesn't contain the bin crate.
