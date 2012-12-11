=========================================
 OBS service for downloading git tarballs
=========================================

This is an `Open Build Service`_ source service.

Requires argparse which is part of python2.7, but available as a third-party dependency in python2.6.

Uses a ``majorversion`` macro in the spec file which contains the upstream stable version number.

The spec files should already contain the macro and ``%setup`` should use it e.g::

    %define majorversion 201
    ...
    %setup -q -n %{component}-%{majorversion}


The ``git_tarballs`` service will also change the specfile's ``Source:`` to the ``filename`` argument of the service.


TODO:

* ignore Merge commits
* use current user's email address in .changes file
* stop parsing when we reach the last known commit
* tests


.. _Open Build Service: http://openbuildservice.org/
