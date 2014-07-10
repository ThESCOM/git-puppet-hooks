Copyright (c) 2014 ThESCOM (Max Oberberger -- max@oberbergers.de)

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the 
GNU General Public License for more details.

You should have received a copy of the GNU General Public License 
along with this program.  If not, see <http://www.gnu.org/licenses/>.

* * *

Table of Contents
=================
1. [Introduction]()
2. [System Requirements]()
3. [Installation]()

1. Introduction
===============
Everytime I write a puppet-manifest I thought, that it would be pretty cool to
test the puppet manifest before I write my commit message. Because testing after
the commit message via jenkins or something similar just blow up the commit
messages and the reverted commit messages. Therefore I wrote this commit hook to
check the puppet manifest before my commit.

2. System Requirements
===============
- puppet  
- puppet-lint

both can be installed with distribution packages like debian/ubuntu
    
    sudo apt-get install puppet puppet-lint

or with the gem-tool:

    gem install puppet puppet-lint

3. Installation 
===============
The puppet git hook is for client side validation of puppet manifests.
Therefore you have to install the hook at your .git folder of your puppet git
repository:

    Example:
        cp pre-commit /path/to/your/puppet-git-repo/.git/hooks/

If done the hook will check your manifests every time you call `git commit`.
