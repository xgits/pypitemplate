pypi template

https://packaging.python.org/en/latest/tutorials/packaging-projects/

# preparation
py -m pip install --upgrade pip

py -m pip install --upgrade build

py -m pip install --upgrade twine

# build
py -m build

# test
py -m twine upload --repository testpypi dist/*

py -m pip install --index-url https://test.pypi.org/simple/ --no-deps example-package-YOUR-USERNAME-HERE

# distribute
twine upload dist/*
