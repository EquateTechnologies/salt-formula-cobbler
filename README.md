salt-formula-cobbler
======================
Formula to install/manage Cobbber


Install, configure and set up Cobbler. Tested on CentOS 7.

.. note::

    See the full `Salt Formulas installation and usage instructions
    <http://docs.saltstack.com/en/latest/topics/development/conventions/formulas.html>`_.

Available states
================

.. contents::
    :local:

``cobbler``
--------
Includes cobbler.install and cobbler.config

``cobbler.repo``
-----------
Configure appropriate package repo source/s based on distro and distro version.

``cobbler.install``
-----------
Installs cobbler package/s and dependencies as configured by pillar.

``cobbler.config``
-----------
Configure cobbler. NOTE: does not configure cobbler-web. See ``cobbler.web`` state.

``cobbler.web``
----------
Installs and configures the cobbler-web package. NOTE: cobbler-web package will pull in Apache. Use an appropriate formula to configure Apache properly.

``cobbler.sync``
-----------
Runs 'cobbler sync'

``cobbler.repo``
-----------
Configures repos based on pillar.

``cobbler.reposync``
-----------
Runs 'cobbler reposync --only=repo-name' for repos listed in pillar.

``cobbler.pxe``
-----------
Imports pxe files from sources based on pillar

``cobbler.kickstarts``
-----------
Imports kickstart files from sources based on pillar

``cobbler.snippets``
-----------
Imports snippet files from sources based on pillar

``cobbler.loaders``
-----------
Imports loaders files from cobbler repository + from sources based on pillar

``cobbler.images``
-----------
Imports images files from sources based on pillar

``cobbler.distros``
-----------
Configures distros based on pillar.

``cobbler.profiles``
-----------
Configures profiles based on pillar.

``cobbler.systems``
-----------
Configures systems based on pillar.
