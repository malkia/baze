# Experiment with source and bazel files at sibling folders

This is mainly in case we want to start using bazel without introducing bazel files yet.

## Windows

Have this in your %ProgramData%\bazel.bazelrc

```cmd
build --disk_cache=f:/bazel.cache/disk
build --repository_cache=f:/bazel.cache/repo
startup --output_user_root=f:/bazel.cache/user
build --experimental_repository_cache_hardlinks
startup --windows_enable_symlinks
startup --host_jvm_args=-Xmx8192m
startup --host_jvm_args=-Xms2048m
```
