# zeit-now-nestjs-starter
A Demo for [nextjs-starter](https://github.com/nestjs/typescript-starter) deploy to [zeit/now](https://github.com/zeit/now) in a minute.

### Deployment
```sh
# clone the project
git clone https://github.com/calvinlam0124/zeit-now-nestjs-starter

# update git sub-module
git submodule update --init --recursive

# initial and build your applicatoin - nestjs
cd typescript-starter
npm install && npm test && npm build

# deploy
now
```


### Deploy with your ready made application
just create a now.json and run now
```sh
vim now.json
now
```
