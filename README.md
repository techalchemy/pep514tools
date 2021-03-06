# pep514tools

Tools for finding, modifying and cleaning up registered Python environments.

See [PEP 514](https://www.python.org/dev/peps/pep-0514/) for the background and specification
of registered environment information.

# Installation

To install:

```
pip install pep514tools
```

Note that this module only works (and is only useful) on Windows.

# Usage

The basic functions are `findall` and `find`.

Calling `findall` will return all detected registrations. `find` will only return those
with the specified tag or company/tag.

For example:

```
>>> pep514tools.find('2.7')
[<environment PythonCore\2.7>]

>>> pep514tools.find('ContinuumAnalytics', 'Anaconda35-64')
[<environment ContinuumAnalytics\Anaconda35-64>]

>>> list(pep514tools.findall())
[<environment PythonCore\2.7>, <environment PythonCore\3.5>, <environment PythonCore\3.5-32>, <environment PythonCore\3.6>,
 <environment ContinuumAnalytics\Anaconda35-64>]
```
