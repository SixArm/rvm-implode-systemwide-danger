# Ruby Version Manager (RVM) implode systemwide. THIS IS DANGEROUS.

This script tries to eliminate RVM everywhere on the system,
by doing these steps:

  * Run `rvm implode`
  * Delete all known RVM-related files everywhere on the system.
  * Delete all users' home directory `.rvm` directories and `.rvmrc` files.
  * Uninstall all known RVM gems.
  * Search the system for potential lingering items and print them.

## Use at your own risk

This script is not advanced:

  * it does not do any error checking
  * it does not ensure anything worked
  * it does not guarantee success

If it doesn't work for you, please let us know and we'll improve it.

We welcome feedback, patches, and pull requests.

## Warnings

Some of the script lines may report missing directories.

For example, a Mac system typically has a /Users/ directory,
whereas a Linux system typically has a /home/ directory.
You can delete the lines that you don't need, if you like.

If rvm implode gives errors like this loop:

    line 72: /usr/local/rvm/scripts/rvm: No such file or directory

then the rvm setup is bonked and we can delete the rvm script
by hand then run this script again; rvm implode won't work,
but the rest of the script will do a decent job of deleting
any lingering rvm files and reporting any remainders.

## About

  * Command: rvm-implode-systemwide-danger
  * Version: 2.0.0
  * Created: 2011-08-22
  * Updated: 2016-02-09
  * License: GPL
  * Contact: Joel Parker Henderson (joel@joelparkerhenderson.com)
