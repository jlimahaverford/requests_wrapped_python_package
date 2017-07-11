# requests_wrapped_python_package
Python package with one dependency, the requests package.  This project was created as a minimal example of introducing a non-standard-library python package as a dependency python development.  While many examples exist, they all seem to strike the same middle-ground between minimal and exhaustive.  This is minimal.

To install:

- pip install -e git+https://github.com/jlimahaverford/hello_world_python_package.git#egg=requests_wrapped_python_package

```
Jonathans-MacBook-Pro:PythonEnvironments jonathanlima$ mkvirtualenv --python=/usr/local/bin/python3.6 test_env

    Running virtualenv with interpreter /usr/local/bin/python3.6
    Using base prefix '/Library/Frameworks/Python.framework/Versions/3.6'
    New python executable in /Users/jonathanlima/PythonEnvironments/test_env/bin/python3.6
    Also creating executable in /Users/jonathanlima/PythonEnvironments/test_env/bin/python
    Installing setuptools, pip, wheel...done.
    virtualenvwrapper.user_scripts creating /Users/jonathanlima/PythonEnvironments/test_env/bin/predeactivate
    virtualenvwrapper.user_scripts creating /Users/jonathanlima/PythonEnvironments/test_env/bin/postdeactivate
    virtualenvwrapper.user_scripts creating /Users/jonathanlima/PythonEnvironments/test_env/bin/preactivate
    virtualenvwrapper.user_scripts creating /Users/jonathanlima/PythonEnvironments/test_env/bin/postactivate
    virtualenvwrapper.user_scripts creating /Users/jonathanlima/PythonEnvironments/test_env/bin/get_env_details

(test_env) Jonathans-MacBook-Pro:PythonEnvironments jonathanlima$ pip freeze

(test_env) Jonathans-MacBook-Pro:PythonEnvironments jonathanlima$ pip install -e git+https://github.com/jlimahaverford/requests_wrapped_python_package.git#egg=requests_wrapped_python_package

    Obtaining requests_wrapped_python_package from git+https://github.com/jlimahaverford/requests_wrapped_python_package.git#egg=requests_wrapped_python_package
      Cloning https://github.com/jlimahaverford/requests_wrapped_python_package.git to ./test_env/src/requests-wrapped-python-package
    Collecting requests (from requests_wrapped_python_package)
      Using cached requests-2.18.1-py2.py3-none-any.whl
    Collecting urllib3<1.22,>=1.21.1 (from requests->requests_wrapped_python_package)
      Using cached urllib3-1.21.1-py2.py3-none-any.whl
    Collecting certifi>=2017.4.17 (from requests->requests_wrapped_python_package)
      Using cached certifi-2017.4.17-py2.py3-none-any.whl
    Collecting idna<2.6,>=2.5 (from requests->requests_wrapped_python_package)
      Using cached idna-2.5-py2.py3-none-any.whl
    Collecting chardet<3.1.0,>=3.0.2 (from requests->requests_wrapped_python_package)
      Using cached chardet-3.0.4-py2.py3-none-any.whl
    Installing collected packages: urllib3, certifi, idna, chardet, requests, requests-wrapped-python-package
      Running setup.py develop for requests-wrapped-python-package
    Successfully installed certifi-2017.4.17 chardet-3.0.4 idna-2.5 requests-2.18.1 requests-wrapped-python-package urllib3-1.21.1

(test_env) Jonathans-MacBook-Pro:PythonEnvironments jonathanlima$ pip freeze

    certifi==2017.4.17
    chardet==3.0.4
    idna==2.5
    requests==2.18.1
    -e git+https://github.com/jlimahaverford/requests_wrapped_python_package.git@c583807da1477549012df1778dba0ff6eef43635#egg=requests_wrapped_python_package
    urllib3==1.21.1

(test_env) Jonathans-MacBook-Pro:PythonEnvironments jonathanlima$ python

    Python 3.6.1 (v3.6.1:69c0db5050, Mar 21 2017, 01:21:04)
    [GCC 4.2.1 (Apple Inc. build 5666) (dot 3)] on darwin
    Type "help", "copyright", "credits" or "license" for more information.
    >>> from requests_wrapped_python_package import requests_wrapped
    >>> requests_wrapped.get('https://www.google.com').status_code
    200
    >>>

```