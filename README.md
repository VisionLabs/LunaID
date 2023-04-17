

### usage

```sh
pipenv install
pipenv shell
mkdocs serve
```


### mkdocs cheats

```sh
mkdocs new [dir-name] - Create a new project.
mkdocs serve - Start the live-reloading docs server.
mkdocs build - Build the documentation site.
mkdocs -h - Print help message and exit.
```


на каждую версию - своя ветка.
чтобы можно было обновлять доки.
потому что не все обновляются сразу.



### how to update docs

```sh
cd mkdocs
git checkout {version}
```

and then use `mike` or `mkdocs`.

```sh
mike serve --dev-addr '127.0.0.1:9876'
mike deploy --update-aliases {version} latest
```


### how to create docs for new version

```sh
cd mkdocs
git checkout {lastest_version}
git checkout -b {next_version}
```

update docs and deploy it.

```sh
mike deploy --push --update-aliases {next_version} latest
```


