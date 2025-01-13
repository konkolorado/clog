# Keep a personal changelog

When you want to document an acheivement:

```bash
scriv create
```

Fill out the newly created `.md` document in the `changelog.d` directory. Make
sure to uncomment only the sections that are going to have contents added to
them. 

A Github Action will periodically run, collecting changelog fragments in the
`changelog.d` directoy and compiling them into the completed `CHANGELOG.md`. 


## Versions

Changelog fragments are compiled to a version following the CalVer scheme
`YYYY.0W`. An easy way to associate week number with week dates is to use the
`ncal` command, such as below.

```bash
ncal -w  [YYYY]
```