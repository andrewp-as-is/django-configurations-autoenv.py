<!--
https://readme42.com
-->


[![](https://img.shields.io/pypi/v/django-configurations-autoenv.svg?maxAge=3600)](https://pypi.org/project/django-configurations-autoenv/)
[![](https://img.shields.io/badge/License-Unlicense-blue.svg?longCache=True)](https://unlicense.org/)
[![](https://github.com/andrewp-as-is/django-configurations-autoenv.py/workflows/tests42/badge.svg)](https://github.com/andrewp-as-is/django-configurations-autoenv.py/actions)

### Installation
```bash
$ [sudo] pip install django-configurations-autoenv
```

#### How it works
+   environment variable must be prefixed with `DJANGO_`
+   `True` values: `'yes'`, `'y'`, `'true'`, `'1'`
+   `False` values: `'no'`, `'n'`, `'false'`, `'0'`
+   list values: must contain a comma `,`

##### `settings.py`
```python
from configurations import Configuration
from django_configurations_autoenv import AutoenvMixin

class Base(AutoenvMixin,Configuration):
```

```python
from django_configurations_autoenv import AutoenvConfiguration

class Base(AutoenvConfiguration):
```

##### `.env`
```bash
DJANGO_STATIC=/static/
DJANGO_ALLOWED_HOSTS=domain1.com,domain2.com
DJANGO_DEBUG=false
```

#### Links
+   [django-configurations](https://github.com/jazzband/django-configurations)

<p align="center">
    <a href="https://readme42.com/">readme42.com</a>
</p>
