Steps to quickly demonstrate SDLC

First create some modules

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
```
Then it's time to pull / merge this modules in a separate branch

```
git checkout master

git checkout -b sprint/uat-127
git add -A
git commit -m update
git push --set-upstream origin sprint/uat-127
```

Now we can test these modules on our UAT environment

Let's suppose module-x was the only approved module we create a new prd branch for this sprint

```
git checkout master

git checkout -b sprint/prd-127
git add -A
git commit -m update
git push --set-upstream origin sprint/prd-127
```

We can pull / merge module-x with this new branch
Deploy it again on uat and once approved deploy it to production.

Then we can pull / merge sprint/prd-127 with master so master is up to the current production deployment.
