# puppet-apply-step


The Puppet Apply Step Plugin executes the 
[puppet apply](http://docs.puppetlabs.com/references/3.3.1/man/apply.html) 
command on each node matching the Job node filter.
The manifest file specified by the plugin is assumed to be present on the remote node.

The plugin can be configured to invoke the puppet command using sudo.
Also, the plugin allows you to pass any standard options to the puppet apply command.


## Plugin Parameters

* File: The puppet manifest file. This file is assumed to be installed on the remote node.
* Arguments: Optional arguments to pass to puppet apply command.
* Sudo: Use sudo to run puppet (default: false)

## Verbose output

If the job invokes the plugin with loglevel==DEBUG, the plugin will configure
puppet apply using the --verbose flag.

## Build


    make

produces:

    puppet-apply.zip

    make install

Copies it to $RDECK_BASE/libext    
