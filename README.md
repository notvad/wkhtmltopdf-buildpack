# wkhtmltopdf buildpack

This is a [Heroku buildpack][0] for bundling a compatible [wkhtmltopdf][1] binary with your environment.
`wkhtmltoimage` binary is not included in this buildpack.

## Supported stacks:
* heroku-18
* heroku-20
* heroku-22


## Usage

This buildpack only installs wkhtmltopdf, it isn't very useful by itself. You'll probably want to use add it to you current buildpacks config.

```bash
$ heroku buildpacks:add https://github.com/notvad/wkhtmltopdf-buildpack
```

### Clearing Repo Cache

Remember to clean your repository cache if you are updating the version of buildpack. To do that, run:

```bash
$ heroku plugins:install https://github.com/heroku/heroku-repo.git
$ heroku repo:purge_cache -a appname
```

[0]: http://devcenter.heroku.com/articles/buildpacks
[1]: http://wkhtmltopdf.org/
