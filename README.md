# Udagram Feed-Api Service

## Coding Style Guide
​
codestyle is defined in the tslint config file [tslint.json](tslint.json)
​
## Build Tool
​
### Prerequisites
​
- nodejs
- docker
​
### Overview
 see all node commands in [package.json](package.json)
 
### Build
```shell script
node run build
```

### Run Dev
```shell script
node run start
```
​
### Dockerize

e.g.
```shell script
docker build -t <image_tag> . && docker run <image_tag> 
```

## Versioning
​
This project uses [SemVer](https://semver.org/) for versioning and [gitflow](https://danielkummer.github.io/git-flow-cheatsheet/) for the git workflow
​
The Version number is defined by Tags in git. The Version-name is based on git-Tags.
​​
## License
​
© 2020 jaschke.it All Rights Reserved.
