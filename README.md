puppet-repository
===========

[![Puppet Forge](https://img.shields.io/puppetforge/v/halyard/repository.svg)](https://forge.puppetlabs.com/halyard/repository)
[![Dependency Status](https://img.shields.io/gemnasium/halyard/puppet-repository.svg)](https://gemnasium.com/halyard/puppet-repository)
[![MIT Licensed](https://img.shields.io/badge/license-MIT-green.svg?style=flat)](https://tldrlegal.com/license/mit-license)
[![Build Status](https://img.shields.io/circleci/project/halyard/puppet-repository.svg)](https://circleci.com/gh/halyard/puppet-repository)

Module to define repository type

## Changes from upstream

* Clean up syntax for newtype creation

## Usage

```puppet
repository { '/path/to/code':
    source   => 'user/repo', #short hand for github repos
    provider => 'git'
}
repository { 'my emacs config':
    source   => 'git://github.com/wfarr/.emacs.d.git',
    ensure   => '32811db53e109197244c21a84b0fa2b36f497966',
    path     => '/etc/emacs.d',
    provider => 'git',
}
```

## Required Puppet Modules

* [git](https://github.com/halyard/puppet-git)

