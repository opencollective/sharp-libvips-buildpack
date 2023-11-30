This repository attempts to reproduce that `sharp` is not building when using the `heroku-buildpack-vips` heroku buildpack.

## Buildpacks

Make sure to have Heroku configured with those buildpacks:

- https://github.com/heroku/heroku-buildpack-apt
- https://github.com/brandoncc/heroku-buildpack-vips
- heroku/nodejs

## Deployment

```
git remote add heroku https://git.heroku.com/sharp-libvips-buildpack.git
git push heroku
```

## Notes

At this moment, the latest version of `sharp` requires `"libvips": ">=8.15.0"`.

The current `heroku-buildpack-vips` only has `8.14.5`, use the opencollective fork to reproduce properly:

- https://github.com/opencollective/heroku-buildpack-vips
