# nodejs-cookbook [![Build Status](https://travis-ci.org/redguide/nodejs.svg)](https://travis-ci.org/redguide/nodejs)

## DESCRIPTION

Installs Node.JS

## REQUIREMENTS


### Platform

* Tested on Debian 6 and Ubuntu 10.04
* Should work fine on Centos, RHEL, etc.

### Cookbooks:

* [build-essential](https://github.com/opscode-cookbooks/build-essential)
* [apt](https://github.com/cookbooks/apt)
* [yum](https://github.com/cookbooks/yum)

Opscode cookbooks (http://github.com/opscode/cookbooks/tree/master)

## ATTRIBUTES

* nodejs['install_method'] = source or package
* nodejs['version'] - release version of node to install
* nodejs['src_url'] - download location for node source tarball
* nodejs['dir'] - location where node will be installed, default /usr/local
* nodejs['npm'] - version of npm to install
* nodejs['npm_src_url'] - download location for npm source tarball
* nodejs['check_sha'] - test for valid sha_sum, default: true

## USAGE

Include the nodejs recipe to install node on your system based on the default installation method:

*  include_recipe "nodejs"

Include the install_from_source recipe to install node from sources:

*  include_recipe "nodejs::install_from_source"

Include the install_from_package recipe to install node from packages:
Note that only apt (Ubuntu, Debian) appears to have up to date packages available.
Centos, RHEL, etc are non-functional. (Try install_from_binary for those)

*  include_recipe "nodejs::install_from_package"

Include the install_from_binary recipe to install node from official prebuilt binaries:
(Currently Linux x86, x86_64, armv6l only)

*  include_recipe "nodejs::install_from_binary"

Include the npm recipe to install npm:

*  include_recipe "nodejs::npm"

## LICENSE and AUTHOR

Author:: Marius Ducea (marius@promethost.com)
Author:: Nathan L Smith (nlloyds@gmail.com)

Copyright:: 2010-2012, Promet Solutions
Copyright:: 2012, Cramer Development, Inc.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
