# Release a new version of Jupyter_Video_Widget:

PyPi Instructions: https://packaging.python.org/distributing/#uploading-your-project-to-pypi

Twin command-line tool for registering and uploading packages: https://github.com/pypa/twine

## Version Numbers

Version number for this project are defined once for Python and again for Javascript:
- jpy_video/version.py
- js/package.json


Commit code edits to GitHub after making all your awesome changes.  Update version
number in the file version.py, making sure to also remove 'dev' descriptor.

```bash
git add <any new stuff>
git commit -a
git push
```

Create source and binary distribution files.  Twine will handle registering the project the
first time uploading a distribution for a new project.  Install twine via pip if necessary.

```bash
rm -rf dist

python setup.py sdist bdist_wheel

twine upload dist/*
```


Once the above is done its time to go back to developing the next great release.  Update current
version number inside version.py by adding 'dev' and increment the minor number. Commit this change
and go to work.

```bash
git commit -a
```
