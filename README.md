# PyPi Test 
Link to instructions: https://realpython.com/pypi-publish-python-package/

## Building package
Build the package using the setup.py manifest
```sh
python setup.py sdist bdist_wheel
```

## Upload
Upload to TestPyPi with this:
```sh
twine upload --repository-url https://test.pypi.org/legacy/ dist/*
```
Upload to main PyPi with this:
```sh
twine upload dist/*
```