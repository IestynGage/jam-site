# Website

This website is built using [Docusaurus 2](https://docusaurus.io/), a modern static website generator. This project is used to build simple site about jam.


## Local Dev

```
$ yarn
$ yarn start
$ yarn build
```

## S3

The purpose of this project is to generate webpages so that they could be deployed as a S3 static site. This was done by:
1. Creating a s3 bucket
2. Adding a new bucket policy that includes the action `s3:GetObject`
3. Running `yarn build`
4. Dump all content of `./build` into S3
5. On properties tab enable Static website hosting
6. Set up index document and error document.

**Notes**: The resource URL is different to the bucket website url, the resource URL won't have the re-directing.