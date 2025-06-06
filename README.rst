nginx-build-script
==================

Enhance the building of nginx with the following features

- Split ``clean`` & ``mrproper`` targets. ``clean`` just removes object
  files & binaries, ``mrproper`` cleans all
- A ``tags`` target for generating a ctags file
- Enhance the ``objs/Makefile`` with ``D``, ``E`` & ``EXTRA_CFLAGS`` variables.
  ``D`` = 1 sets ``-O0``, ``E`` = 0 disables ``-Werror``

Usage
-----

Just copy the ``cnginx`` and ``Makefile.ac`` into the nginx repository root.
You can call ``cnginx`` whatever you like.

Edit the ``PREFIX`` variable in ``cnginx`` as desired. This will be the
default installation prefix. You can override it with ``--prefix=``.

Then instead of calling ``auto/configure`` you call ``./cnginx``, passing all
the same arguments you would to ``auto/configure``.

License
-------

`BSD-2-Clause license </LICENSE>`__

Andrew Clayton <ac@sigsegv.uk>
