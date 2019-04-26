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

## Mixed Content Issue

When opening the deployed documentation in modern browsers, you will see errors about [Mixed Content](https://developers.google.com/web/fundamentals/security/prevent-mixed-content/what-is-mixed-content):

<details>
  
  <summary>Screenshot from Chrome</summary>
  
  <img width="342" alt="Screen Shot 2019-04-26 at 09 52 46" src="https://user-images.githubusercontent.com/1131196/56812549-2407dc00-6809-11e9-97b9-d5ed3be067d8.png">

</details>

This happens because [`YUIDoc`]() assets aren't served via HTTPS. On top of that it dynamically adds scripts that aren't served as HTTPS either. At this point, it is safe to click "Load Unsafe Scripts".
