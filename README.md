modules-cookbook
================

= DESCRIPTION:
Chef cookbook to manage linux modules with /etc/modules and modprobe (linux 2.6 +)

= REQUIREMENTS:

Linux 2.6+
Ubuntu >9.10 (for the moment. use upstart and not init, any contribution is welcome)

= ATTRIBUTES:
node['modules'] = A namespace for modules settings.

= USAGE:
There are two ways of setting sysctl values:
1. Set chef attributes, E.G.:
   default['modules']['loop']
2. With Ressource/Provider

Resource/Provider
=================

This cookbook includes LWRPs for managing:
* modules

modules
--------

# Actions

- :load: load a module
- :unload: unload modules

# Attribute Parameters

- module
- options


# Examples

```
modules "8021q" do
  action :load
end
```

# Examples
