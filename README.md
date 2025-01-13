# Keep a personal changelog

A template repo that can be used to maintain a personal changelog. Powered by
`scriv` and Github Actions.

## Setup 

1. Create a new repository from this template
    ```bash
    gh repo create my-clog --template konkolorado/clog --private --clone
    ```
2. [Optional] Install `poetry`
3. Install `scriv`
    
    **NOTE** This repo lists `scriv` as a dependency for convenience. You can use an
    externally installed version of `scriv` (from `pipx`, for example) to create new
    changelog fragments. Or you can install using `poetry install`. If installed
    using `poetry`, prepend `poetry` to all commands that use `scriv` below.

## Usage 

When you want to document an achievement:

```bash
scriv create
```

Fill out the newly created `.md` document in the `changelog.d` directory. Make
sure to uncomment only the sections that are going to have contents added to
them. Git add and push the file. 

A Github Action will periodically run (by default on Sunday evenings),
collecting changelog fragments in the `changelog.d` directoy and compiling them
into the completed `CHANGELOG.md`. 

## Versions

Changelog fragments are compiled to a version following the CalVer scheme
`YYYY.0W`. An easy way to associate week number with week dates is to use the
`ncal` command, such as below.

```bash
ncal -w  [YYYY]
```