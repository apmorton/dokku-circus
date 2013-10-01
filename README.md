# dokku-circus

dokku-circus is a plugin for [dokku][dokku] that injects
[circus][circus] to run applications.

Normally, dokku only runs the `web` process within Procfile. The
dokku-circus plugin will run all process types (web, worker, etc.) and
will restart crashed applications.

## Usage

This plugin does not read a traditional Procfile, instead you must provide `circus.ini` in its place


## Installation

```sh
git clone https://github.com/apmorton/dokku-circus.git /var/lib/dokku/plugins/dokku-circus
```

All future deployments will use circus to start all processes.

## Derived From

The basis for this readme and dokku hook are based on [dokku-supervisord](https://github.com/statianzo/dokku-supervisord)

## License

The MIT License (MIT)

Copyright (c) 2013 Austin Morton

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

[dokku]: https://github.com/progrium/dokku
[circus]: https://circus.readthedocs.org/