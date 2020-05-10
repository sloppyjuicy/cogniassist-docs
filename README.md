## After changes
```
git add .
git commit -m "change description"
git push origin master
```

## To deploy a version
```
git chekc
yarn run build
git add -f build/cogniassist-docs/
git commit -m "initial build"
git subtree push --prefix build/cogniassist-docs origin gh-pages
```