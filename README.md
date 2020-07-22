About requests-oauthlib
=======================

Home: https://github.com/requests/requests-oauthlib

Package license: ISC

Feedstock license: BSD-3-Clause

Summary: OAuthlib authentication support for Requests.

Requests-OAuthlib
=========================================================

This project provides first-class OAuth library support for [Requests](http://python-requests.org).

The OAuth 1 workflow
--------------------

OAuth 1 can seem overly complicated and it sure has its quirks. Luckily,
requests_oauthlib hides most of these and let you focus at the task at hand.

Accessing protected resources using requests_oauthlib is as simple as:

    >>> from requests_oauthlib import OAuth1Session
    >>> twitter = OAuth1Session('client_key',
                                client_secret='client_secret',
                                resource_owner_key='resource_owner_key',
                                resource_owner_secret='resource_owner_secret')
    >>> url = 'https://api.twitter.com/1/account/settings.json'
    >>> r = twitter.get(url)

Before accessing resources you will need to obtain a few credentials from your
provider (e.g. Twitter) and authorization from the user for whom you wish to
retrieve resources for. You can read all about this in the full
[OAuth 1 workflow guide on RTD](https://requests-oauthlib.readthedocs.io/en/latest/oauth1_workflow.html)

The OAuth 2 workflow
--------------------

OAuth 2 is generally simpler than OAuth 1 but comes in more flavours. The most
common being the Authorization Code Grant, also known as the WebApplication
flow.

Fetching a protected resource after obtaining an access token can be extremely
simple. However, before accessing resources you will need to obtain a few
credentials from your provider (e.g. Google) and authorization from the user
for whom you wish to retrieve resources for. You can read all about this in the
full [OAuth 2 workflow guide on RTD](https://requests-oauthlib.readthedocs.io/en/latest/oauth2_workflow.html).


Current build status
====================


<table><tr><td>All platforms:</td>
    <td>
      <a href="https://dev.azure.com/conda-forge/feedstock-builds/_build/latest?definitionId=3525&branchName=master">
        <img src="https://dev.azure.com/conda-forge/feedstock-builds/_apis/build/status/requests-oauthlib-feedstock?branchName=master">
      </a>
    </td>
  </tr>
</table>

Current release info
====================

| Name | Downloads | Version | Platforms |
| --- | --- | --- | --- |
| [![Conda Recipe](https://img.shields.io/badge/recipe-requests--oauthlib-green.svg)](https://anaconda.org/conda-forge/requests-oauthlib) | [![Conda Downloads](https://img.shields.io/conda/dn/conda-forge/requests-oauthlib.svg)](https://anaconda.org/conda-forge/requests-oauthlib) | [![Conda Version](https://img.shields.io/conda/vn/conda-forge/requests-oauthlib.svg)](https://anaconda.org/conda-forge/requests-oauthlib) | [![Conda Platforms](https://img.shields.io/conda/pn/conda-forge/requests-oauthlib.svg)](https://anaconda.org/conda-forge/requests-oauthlib) |

Installing requests-oauthlib
============================

Installing `requests-oauthlib` from the `conda-forge` channel can be achieved by adding `conda-forge` to your channels with:

```
conda config --add channels conda-forge
```

Once the `conda-forge` channel has been enabled, `requests-oauthlib` can be installed with:

```
conda install requests-oauthlib
```

It is possible to list all of the versions of `requests-oauthlib` available on your platform with:

```
conda search requests-oauthlib --channel conda-forge
```


About conda-forge
=================

[![Powered by NumFOCUS](https://img.shields.io/badge/powered%20by-NumFOCUS-orange.svg?style=flat&colorA=E1523D&colorB=007D8A)](http://numfocus.org)

conda-forge is a community-led conda channel of installable packages.
In order to provide high-quality builds, the process has been automated into the
conda-forge GitHub organization. The conda-forge organization contains one repository
for each of the installable packages. Such a repository is known as a *feedstock*.

A feedstock is made up of a conda recipe (the instructions on what and how to build
the package) and the necessary configurations for automatic building using freely
available continuous integration services. Thanks to the awesome service provided by
[CircleCI](https://circleci.com/), [AppVeyor](https://www.appveyor.com/)
and [TravisCI](https://travis-ci.com/) it is possible to build and upload installable
packages to the [conda-forge](https://anaconda.org/conda-forge)
[Anaconda-Cloud](https://anaconda.org/) channel for Linux, Windows and OSX respectively.

To manage the continuous integration and simplify feedstock maintenance
[conda-smithy](https://github.com/conda-forge/conda-smithy) has been developed.
Using the ``conda-forge.yml`` within this repository, it is possible to re-render all of
this feedstock's supporting files (e.g. the CI configuration files) with ``conda smithy rerender``.

For more information please check the [conda-forge documentation](https://conda-forge.org/docs/).

Terminology
===========

**feedstock** - the conda recipe (raw material), supporting scripts and CI configuration.

**conda-smithy** - the tool which helps orchestrate the feedstock.
                   Its primary use is in the construction of the CI ``.yml`` files
                   and simplify the management of *many* feedstocks.

**conda-forge** - the place where the feedstock and smithy live and work to
                  produce the finished article (built conda distributions)


Updating requests-oauthlib-feedstock
====================================

If you would like to improve the requests-oauthlib recipe or build a new
package version, please fork this repository and submit a PR. Upon submission,
your changes will be run on the appropriate platforms to give the reviewer an
opportunity to confirm that the changes result in a successful build. Once
merged, the recipe will be re-built and uploaded automatically to the
`conda-forge` channel, whereupon the built conda packages will be available for
everybody to install and use from the `conda-forge` channel.
Note that all branches in the conda-forge/requests-oauthlib-feedstock are
immediately built and any created packages are uploaded, so PRs should be based
on branches in forks and branches in the main repository should only be used to
build distinct package versions.

In order to produce a uniquely identifiable distribution:
 * If the version of a package **is not** being increased, please add or increase
   the [``build/number``](https://conda.io/docs/user-guide/tasks/build-packages/define-metadata.html#build-number-and-string).
 * If the version of a package **is** being increased, please remember to return
   the [``build/number``](https://conda.io/docs/user-guide/tasks/build-packages/define-metadata.html#build-number-and-string)
   back to 0.

Feedstock Maintainers
=====================

* [@BrentDorsey](https://github.com/BrentDorsey/)
* [@pmlandwehr](https://github.com/pmlandwehr/)
* [@xylar](https://github.com/xylar/)

