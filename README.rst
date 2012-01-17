.. role:: branch (emphasis)
.. default-role:: branch



This is a GitHub mirror of the development repository of the **Sage
library**, which is the central Python/Cython foundation of the Sage_
distribution of mathematical software. It is normally found in
``$SAGE_ROOT/devel/sage-main`` in an installed copy of Sage.

.. _Sage: http://sagemath.org/



Development
-----------

First, you must install Sage_.

Where ``$SAGE_ROOT`` denotes the directory where you have unpacked
and/or built Sage, replace the symlink ``$SAGE_ROOT/devel/sage`` with
one pointing to your local clone of this repository. Be aware that this
repository is not the entirety of Sage; checking out old versions of the
Sage library here is not sufficient to produce a vanilla old version of
Sage, since you will still have newer components in other parts of the
Sage system.

When working on this repository, base your topic branches on the
prerelease branch. Don't submit pull requests (unless you want to modify
this README!), as this GitHub repository is only a mirror for now.
Instead, post patches to trac_, along with a link to your topic branch on
GitHub, when you're ready for your code to be reviewed. You will need an
account on trac in order to do this.

Your patches should be in Mercurial ``hg export`` format. There is
a tool which can convert ``git format-patch`` output to this format,
available on GitHub at `kini/patch-converter`_.

For development advice not specific to GitHub or this repository, see
`the Sage Developer's Guide`_. Please also come to `the sage-devel
mailing list`_ and talk to us about what you are doing or want to do! We
may be able to save you a lot of time if you are new to hacking on Sage.

.. _trac: http://trac.sagemath.org/sage_trac/
.. _the Sage Developer's Guide: http://sagemath.org/doc/developer/
.. _the sage-devel mailing list:
    https://groups.google.com/group/sage-devel/
.. _kini/patch-converter: https://github.com/kini/patch-converter/

Branches
--------

The branches I am maintaining on this repository are as follows.

`release`
  This branch tracks the tip of the Mercurial repository distributed
  with the latest stable release version of Sage.

`prerelease`
  This branch tracks the tip of the Mercurial repository distributed
  with the latest development version of Sage. Please base topic
  branches on this branch if you intend to submit patches (Sage does not
  currently use GitHub or even git for that matter, so submitting pull
  requests will get you nowhere, unfortunately.)

`prerelease-x.x.x.x`
  These branches track the tips of the Mercurial repositories
  distributed with various development versions of Sage. Only full
  release versions actually get merged into `master`, so these branches
  are kept around for your convenience (for example if you want to
  rebase a topic branch from one of these prerelease branches onto the
  current `prerelease` branch).

`master`
  This points to the latest release or prerelease.

`github-master`
  The default branch for this GitHub repository. It should consist of
  `master` plus this README file. 

Note that of the above, only `release` and `github-master` are really
suitable for remote tracking, because the others will tend to rewind
themselves often (due to the way that release management of Sage is
currently done). Nevertheless, please base topic branches on
`prerelease`.

Maintainer
----------

This GitHub repository is currently maintained by @kini on github.
