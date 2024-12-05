### Ref

- [How to Host any Website using AWS Amplify Hosting | Amazon Web Services - YouTube](https://www.youtube.com/watch?v=iOlIrU3bhSE)
- [Deploying an Express server using the deployment manifest - AWS Amplify Hosting](https://docs.aws.amazon.com/en_us/amplify/latest/userguide/deploy-express-server.html)

### Getting started

```ruby
mkdir express-app
cd express-app
npm init
```

### Install express, typescript and types
```ruby
npm install express
npm install typescript ts-node @types/node @types/express --D
```

### Generate tsconfig.json

```ruby
npx tsc --init
```

### Update main file

```ruby
curl -O https://raw.githubusercontent.com/tseijp/amplify-express-server-test/refs/heads/main/index.ts
curl -O https://raw.githubusercontent.com/tseijp/amplify-express-server-test/refs/heads/main/deploy-manifest.json
curl -O https://raw.githubusercontent.com/tseijp/amplify-express-server-test/refs/heads/main/amplify.yml
```

### Test start, build, serve

```ruby
# start
tsx watch index.ts
# build
tsc --outDir dist
# serve
node dist/index.js
```

### Push to Github

```tsx
npx gitignore node
echo ".amplify-hosting" >> .gitignore
git add .
git commit -m ":tada: init commit"
git branch -M main
git remote add origin https://github.com/tseijp/amplify-express-server-test.git
git push -u origin main
```
