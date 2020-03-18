# zeit-now-nestjs-starter


### Deploy
1. update git sub-model
```sh
git submodule update --init --recursive
```

1. initial and build sub-model
```sh
cd typescript-starter
npm install
npm run test
npm run build
```

1. setup zeit-now, create `now.json`
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

1. deploy to zeit-now
```sh
now
```
