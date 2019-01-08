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

## Testing Package
You can tell pip to install a package from TestPyPi with this:
```sh
pip install --index-url https://test.pypi.org/simple/ --extra-index-url https://pypi.org/simple your-package-name
```
Virtualenv setup:
```sh
virtualenv -p python3 my-environment-name
```