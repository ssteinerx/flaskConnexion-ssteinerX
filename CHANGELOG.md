# January 28, 2017
Initial publish on GitHub.

> Add [Gunicorn](http://gunicorn.org/) config and add to dependencies

> Update dependencies in generated requirements.txt to latest releases

> Update generated README to include values of all configuration variables.  NOTE: a couple are not printing out values, not worrying about it ATM.  Also, some vars (e.g. serverPort) are not printing at all.  I'm sure this is in the Java code somewhere; not going in there unless absolutely necessary.

> List of available vars obtained by:

    <swagger path>/swagger-codegen-cli.jar config-help -l python-flask

> Remove Python 3.2 support from setup and testing

> 
    
    