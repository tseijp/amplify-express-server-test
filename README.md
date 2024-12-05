### Ref

- [How to Host any Website using AWS Amplify Hosting | Amazon Web Services - YouTube](https://www.youtube.com/watch?v=iOlIrU3bhSE)
- [Deploying an Express server using the deployment manifest - AWS Amplify Hosting](https://docs.aws.amazon.com/en_us/amplify/latest/userguide/deploy-express-server.html)

### Getting started

```ruby
mkdir express-app
cd express-app

# The following command will prompt you for information about your project
npm init

# Install express, typescript and types
npm install express --save
npm install typescript ts-node @types/node @types/express --save-dev

# Generate tsconfig.json
npx tsc --init

# start, build, serve
ts-node src
tsc --outDir dist

# Push to Github
npx gitignore node
echo ".amplify-hosting" >> .gitignore
git add .
git commit -m ":tada: init commit"
git branch -M main
git remote add origin https://github.com/tseijp/amplify-express-server-test.git
git push -u origin main
```
