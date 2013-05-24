# pv

Pv makes installing site-wide python tools easy. It automatically pip installs a package into its own virtualenv, and then updates $PATH to include the installed binaries.

## Installation

Copy/symlink the `pv` executable into /usr/bin/. Better installation coming soon...

## Usage

```
Macintosh:~ tpetr$ pv httpie==0.5.0
----> creating virtualenv httpie
New python executable in /Users/tpetr/.pv/virtualenvs/httpie/bin/python
Installing setuptools............done.
Installing pip...............done.
----> installing / upgrading httpie==0.5.0
Downloading/unpacking httpie==0.5.0
  Using download cache from /Users/tpetr/.pip_cache/http%3A%2F%2Fpypi.python.org%2Fpackages%2Fsource%2Fh%2Fhttpie%2Fhttpie-0.5.0.tar.gz
  Running setup.py egg_info for package httpie

Downloading/unpacking requests>=1.0.4 (from httpie==0.5.0)
  Using download cache from /Users/tpetr/.pip_cache/http%3A%2F%2Fpypi.python.org%2Fpackages%2Fsource%2Fr%2Frequests%2Frequests-1.2.2.tar.gz
  Running setup.py egg_info for package requests

Downloading/unpacking Pygments>=1.5 (from httpie==0.5.0)
  Using download cache from /Users/tpetr/.pip_cache/http%3A%2F%2Fpypi.python.org%2Fpackages%2Fsource%2FP%2FPygments%2FPygments-1.6.tar.gz
  Running setup.py egg_info for package Pygments

Installing collected packages: httpie, requests, Pygments
  Running setup.py install for httpie

    Installing http script to /Users/tpetr/.pv/virtualenvs/httpie/bin
  Running setup.py install for requests

  Running setup.py install for Pygments

    Installing pygmentize script to /Users/tpetr/.pv/virtualenvs/httpie/bin
Successfully installed httpie requests Pygments
Cleaning up...
----> collecting executables
      - http
      - pygmentize
----> complete

add this line to your .bashrc / .zshrc:
[ -f "/Users/tpetr/.pv/env.sh" ] && source "/Users/tpetr/.pv/env.sh"
```

*add line, reload shell*

```
Macintosh:~ tpetr$ http
usage: http [--json] [--form] [--pretty {all,colors,format,none}]
            [--style STYLE] [--print WHAT] [--verbose] [--headers] [--body]
            [--stream] [--output FILE] [--download] [--continue]
            [--session SESSION_NAME | --session-read-only SESSION_NAME]
            [--auth USER[:PASS]] [--auth-type {basic,digest}]
            [--proxy PROTOCOL:HOST] [--follow] [--verify VERIFY]
            [--timeout SECONDS] [--check-status] [--help] [--version]
            [--traceback] [--debug]
            [METHOD] URL [REQUEST ITEM [REQUEST ITEM ...]]
http: error: too few arguments
```

