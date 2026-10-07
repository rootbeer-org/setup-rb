# setup-rb

Installs `rb` and `rb-helper` from a rootbeer commit. Both binaries must carry
the attestation rootbeer's CI made on `main` for that exact commit, or the step
fails.

```yaml
- uses: actions/checkout@v7
- uses: rootbeer-org/setup-rb@<sha>
```

The commit comes from `.github/rb-engine-revision` in the checked-out
repository, a full lowercase SHA. Pass `revision-file` to read another file.
