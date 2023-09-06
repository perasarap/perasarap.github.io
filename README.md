# Test Locally:

```
git switch main
git submodule update
hugo server -D
```


# Optional: to test locally static files:

```
cd public
python3 -m http.server 8000
cd ..
```

# Commit Changes 

```
git status
git add .
git commit -m "Describe the change"
git push
```


# Make it Live in Github Pages!

```
git switch hugopublic
rm -rf themes
git restore --source main -- public
cp -R public/* .
rm -rf public
git status
git add .
git commit -m "Add changes to static"

git push origin hugopublic
```
