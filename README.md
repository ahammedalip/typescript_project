# typescript_project
A step by step procedure for installing typescript with node.js and express

This is a simple guide to set up a TypeScript project with Express.

## Step 1: Initialize npm


``` bash
 npm init -y
```

## 2. Create a 'src' folder and 'server.ts' file
```bash
mkdir src
```
Inside src, create a file named server.ts and add your Express server code.
```
import express from 'express'

const app = express()

app.listen(3000,()=>{console.log("Server running");})
```

## Step 3: Install Express
```
npm install express
```
## Step 4: Install TypeScript
```
npm install typescript --save-dev
```
## Step 5: Install TypeScript types for Express

```
npm install @types/express --save-dev
```
## Step 6: Install TypeScript and Node types
```
npm install typescript ts-node @types/node --save-dev
```
## Step 7: Create tsconfig.json
```
npx tsc --init
```

## Step 8: Update package.json scripts
Add the following line to your package.json under the "scripts" section:
```
"start": "ts-node-dev --respawn --transpile-only ./src/server.ts"
```
Replace server.ts with the actual name of your server file.
Now, you can start your TypeScript Express server with:
```
npm start
```
