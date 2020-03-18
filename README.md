# zeit-now-nestjs-starter
A Demo for [nextjs-starter](https://github.com/nestjs/typescript-starter) deploy to [zeit/now](https://github.com/zeit/now) in a minute.

### Deploy
1. update git sub-model
```sh
git submodule update --init --recursive
```

2. initial and build sub-model
```sh
cd typescript-starter
npm install
npm run test
npm run build
```

3. setup zeit-now, create `now.json`
```json
{
  "version": 2,
  "builds": [
    {
      "src": "typescript-starter/dist/main.js",
      "use": "@now/node"
    }
  ],
  "routes": [
    {
      "src": "/(.*)",
      "dest": "typescript-starter/dist/main.js"
    }
  ]
}
```

4. deploy to zeit-now
```sh
now
```


### Deploy with your ready made application
just create a now.json and run now
```sh
vim now.json
now
```
