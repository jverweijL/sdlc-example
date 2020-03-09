Steps to quickly demonstrate SDLC

```
git clone git@github.com:jverweijL/sdlc-example.git
cd sdlc-example

git checkout -b feature/module-x
echo update > module-x.md
git add -A
git commit -m update
git push --set-upstream origin feature/module-x

git checkout master

git checkout -b feature/module-y
echo update > module-y.md
git add -A
git commit -m update
git push --set-upstream origin feature/module-y

git checkout master

git checkout -b sprint/uat-127
git add -A
git commit -m update
git push --set-upstream origin sprint/uat-127

git checkout master

git checkout -b sprint/prd-127
git add -A
git commit -m update
git push --set-upstream origin sprint/prd-127
```
