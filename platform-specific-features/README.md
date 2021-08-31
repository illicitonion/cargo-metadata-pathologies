# platform-specific-features

When a feature of a dependency is enabled, which enables optional transitive dependencies, those transitive dependencies are not marked as conditional in any way. One cannot work out "On Linux this dependency wouldn't be present". This remains the case even when `--filter-platform` is used.

Ideally, either via `--filter-platform` or via metadata in the returned data structure, it should be clear that on a particular platform the dependency does not exist.

Note that the fact that the feature is conditiona _is_ present in the `package` element for the root package, just the transitive dependency isn't marked as conditional.
