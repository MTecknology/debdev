Debian Dev
==========

The learning curve for building ``.deb`` packages can be a bit steep. The vast
number of tools and different way to do things only adds to this challenge. This
project attempts to decrease this learning curve.

Repository Structure
--------------------

.dotfiles/
~~~~~~~~~~

Any file in ``.dotfiles/`` is a template that can be copied to ``./`` and
modified for personal use. It is guaranteed no ``git pull --rebase`` will ever
conflict with files copied into ``./``.

Use ``./.dotfiles/.init`` to create a symlink to dotfiles that do not contain
the string ``TODO`` and copy those that do. See ``-h`` for additional options.

.sync/
~~~~~~

This directory is used to share files with the virtual machine.

Pre-Development
---------------

There are a few steps to 

GPG Key
~~~~~~~


Usage
-----

Requisites:

- vagrant
- virtualbox

Deploy:

.. code-block:: sh

    ./.dotfiles/.init
    vagrant up

Log in:

.. code-block:: sh

    vagrant ssh

Sample Project
--------------

.. code-block:: sh

    gbp clone https://github.com/MTecknology/tdc.git
    cd tdc
    git checkout debian
    build-unstable
    ls ..
