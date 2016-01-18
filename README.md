Django Pulseware
====================

**A Django health check application**

[![status-image]][status-link]
[![version-image]][version-link]
[![coverage-image]][coverage-link]
[![download-image]][download-link]


Overview
====================

**Best attempt** to health check a Django application while keeping it **DRY**.


How to install
====================

    1. easy_install django-pulseware
    2. pip install django-pulseware
    3. git clone http://github.com/un33k/django-pulseware
        a. cd django-pulseware
        b. run python setup.py
    4. wget https://github.com/un33k/django-pulseware/zipball/master
        a. unzip the downloaded file
        b. cd into django-pulseware-* directory
        c. run python setup.py


How to use
====================

   ```python
    # Check health of your Django Application, Back-end & Environment
    # Ensure 'pulseware.middleware.heartbeat.HeartbeatMiddleWare' is the first middleware
    # in `MIDDLEWARE_CLASSES`. Add 'pulseware' to the INSTALLED_APPS.
    # Also set `PULSEWARE_DEFAULT_SETTINGS` as follow and adjust per your needs.
    # If `PULSEWARE_DEFAULT_SETTINGS` is not provide, the following default will be used
    # ===============================================================
    PULSEWARE_DEFAULT_SETTINGS = {
        'PATH': '/heartbeat',               # what path to perform health check
        'RETURN_CODE': 503,                 # what status code to return
        'CACHE_HEALTH': False,              # check if cache backend is healthy
        'DATABASE_READ_HEALTH': True,       # check if database read is healthy
        'DATABASE_WRITE_HEALTH': False      # check if database write is healthy
    }
   ```

Running the tests
====================

To run the tests against the current environment:

    python manage.py test


License
====================

Released under a ([BSD](LICENSE.md)) license.


Version
====================
X.Y.Z Version

    `MAJOR` version -- when you make incompatible API changes,
    `MINOR` version -- when you add functionality in a backwards-compatible manner, and
    `PATCH` version -- when you make backwards-compatible bug fixes.

[status-image]: https://secure.travis-ci.org/un33k/django-pulseware.png?branch=master
[status-link]: http://travis-ci.org/un33k/django-pulseware?branch=master

[version-image]: https://img.shields.io/pypi/v/django-pulseware.svg
[version-link]: https://pypi.python.org/pypi/django-pulseware

[coverage-image]: https://coveralls.io/repos/un33k/django-pulseware/badge.svg
[coverage-link]: https://coveralls.io/r/un33k/django-pulseware

[download-image]: https://img.shields.io/pypi/dm/django-pulseware.svg
[download-link]: https://pypi.python.org/pypi/django-pulseware
