Command Line Client to AllMyChanges.com
=======================================

Installation
------------

    pip install allmychanges

Next, go to <http://allmychanges.com/account/token/> and obtain
your personal OAuth token.

Write this token into the config file like that:

    # allmychanges.cfg
    [allmychanges]
    token = MY-SECRET-TOKEN

Exporting package list
----------------------

    amch export

Export to a number of formats is available `--help` will tell you everything.


Adding new packages in batch mode
---------------------------------

Prepare a datafile in one of supported formats and run

    amch import --format yaml --input data.yaml

If you didn't entered sources for some packages, script
will ask you where these sources are. Answer honestly. :)

In some cases, script will try to help you. If somebody
already added package with such name and namespace, it will
suggest you the source. Or for python packages, it will
search different urls on the PyPi's pages.


Roadmap
-------

* Process pip's requirements.txt files.
* May be process some requirements of ruby and npm packages too.

Hacking
-------

Feel free [to fork](https://github.com/svetlyak40wt/allmychanges), file issues and send me patches.
