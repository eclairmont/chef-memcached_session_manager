# Memcached Session Manager Cookbook

[![Cookbook Version](http://img.shields.io/cookbook/v/memcached_session_manager.svg?style=flat-square)][cookbook]
[![Build Status](http://img.shields.io/travis/dhoer/chef-memcached_session_manager.svg?style=flat-square)][travis]
[![GitHub Issues](http://img.shields.io/github/issues/dhoer/chef-memcached_session_manager.svg?style=flat-square)][github]

[cookbook]: https://supermarket.chef.io/cookbooks/memcached_session_manager
[travis]: https://travis-ci.org/dhoer/chef-memcached_session_manager
[github]: https://github.com/dhoer/chef-memcached_session_manager/issues

This cookbook installs Tomcat high-availability clusters with memcached 
(https://code.google.com/p/memcached-session-manager/).

## Requirements

- Java must be installed outside of this cookbook.
- Tomcat must be installed outside of this cookbook.  This cookbook expects `$CATALINA_HOME` to be defined in
the environment. If it is not, then override `node['memcached_session_manager']['tomcat']['lib']`.
- Chef 11.14 or higher.

### Platforms

- CentOS
- RedHat
- Ubuntu


## Usage

Include the default recipe on a node's runlist to ensure that memcached_session_manager is installed on tomcat.

### Attributes
- `node['memcached_session_manager']['version']` - Version of memcached_session_manager. 
- `node['memcached_session_manager']['flavor']` - Flavors `memcached` and `couchbase` are supported. 
Defaults to `memcached`.
- `node['memcached_session_manager']['tomcat']['base_version']` - Defaults to `7`.
- `node['memcached_session_manager']['tomcat']['lib']` -  Defaults to `$CATALINA_HOME/lib/`. 
Be sure to override this if $CATALINA_HOME is not defined in your environment.
- `node['memcached_session_manager']['spymemcached']['version']` -  
Version of `spymemcached` to download to support `memcached` flavor.

## Getting Help

- Ask specific questions on [Stack Overflow](http://stackoverflow.com/questions/tagged/chef).
- Report bugs and discuss potential features in [Github issues](https://github.com/dhoer/chef-memcached_session_manager/issues).

## Contributing

Please refer to [CONTRIBUTING](https://github.com/dhoer/chef-memcached_session_manager/blob/master/CONTRIBUTING.md).

## License

MIT - see the accompanying [LICENSE](https://github.com/dhoer/chef-memcached_session_manager/blob/master/LICENSE.md) file for details.
