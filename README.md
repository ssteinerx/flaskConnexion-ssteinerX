# flaskConnexion-ssteinerX

Improved version of swagger codegen (https://github.com/swagger-api/swagger-codegen) Flask template.

Warning: This is a work in progress and will be unstable as heck until I get to a release which I'll bundle up properly according to GitHub conventions.

# Where is this in the original?

Mostly I'm writing this to remind myself.  Not to remind myself why I don't use Java very often, I already remember that, but to remind myself where it is.
 
 The template portion is in:
    
    swagger-codegen/modules/swagger-codegen/src/main/resources/flaskConnexion
    
 The Java portion is in:
    
    swagger-codegen/modules/swagger-codegen/src/main/java/io/swagger/codegen/languages/FlaskConnexionCodegen.java
    
 Well, of course it is...have I mentioned that I'm not a big Java fan lately?  

# Improvements

1. Add documentation of configuration variable values to generated README file

1. Add WSGI server compatible startup function (not relying on running as __main__ to start server)

1. Add simple [Gunicorn](http://gunicorn.org/) configuration and dependency

# How To Use

1. Clone this repository.

2. Add the `--template-dir` parameter to the call to swagger-codegen substituting the checkout directory for TEMPLATE_DIR below.

    --template-dir $(TEMPLATE_DIR)
    
There is no 3.

# TODO

1. Make server port configurable either in generator or by environment variable.
    NOTE: it is configurable but does not print out when getting available parameters from the command line with:

        <swagger path>/swagger-codegen-cli.jar config-help -l python-flask. 
        
1. Figure out how to `make` my own version of the Java that generates this and bundle it with the template.  It should really be a plug-in architecture, not one monolithic repository (which includes all of the compiled examples!) as it is now.  That way people could create stand-alone-ish generators without having to deal with the whole gigantic repository.
