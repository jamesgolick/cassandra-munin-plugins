Cassandra Munin Plugins
=======================

These plugins are configurations for something called jmxquery that I found somewhere. Unfortunately, though, I forget where.

## Installation

Make sure all the files from this repo are in the same directory and that jmx_ is executable. Then in /etc/munin/plugins, create a symlink named after each of the plugin configurations to the jmx_ executable. The symlink needs to be an absolute path, not relative, or jmx_ won't be able to parse it correctly.

If you take a look at the .conf files, it should be fairly straightforward to figure out how to create your own.

If you have JMX running on a non-standard port (something other than 8080), you can set it in your munin config like this:

   [cassandra_]
   env.jmxurl service:jmx:rmi:///jndi/rmi://localhost:YOURPORTHERE/jmxrmi

## Credits

Configs by James Golick and Jonathan Ellis. I wish I knew who wrote jmxquery so I could credit them here.
