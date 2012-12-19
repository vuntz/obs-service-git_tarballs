=========================================
 OBS service for downloading git tarballs
=========================================

This is an `Open Build Service`_ source service.

Requires argparse which is part of python2.7, but available as a third-party dependency in python2.6.

The ``git_tarballs`` service will also change the specfile's ``Source:`` to the
``filename`` argument of the service and the ``%setup -q`` line to match the
parent folder name in the tarball.


TODO:

* ignore Merge commits
* use current user's email address in .changes file
* stop parsing when we reach the last known commit
* tests


.. _Open Build Service: http://openbuildservice.org/
