# ember-data-docs

API documentation for Ember Data 1.0.0-beta.12.

Documentation is available online [here](https://ember-data-docs-isazazenwa.now.sh).

## Pushing updates

```sh
# clone the repo down from github
git clone git@github.com:emberjs/data.git

# checkout the needed version
cd data && git checkout v1.0.0-beta.12

# use a really really old version of node.js, 0.12
nvm use 0.12

# build the project
npm run dist

# documentation will be generated under `dist/docs`
# copy the content of `dist/docs` into the repo
```

## Deployment

Deployment is done via [now.sh](https://zeit.co/now). You would need push rights
and an account in order to update the deployed documentation.
