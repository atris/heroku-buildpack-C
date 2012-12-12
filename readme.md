# Heroku Buildpack: C

Use C-Buildpack if you need Heroku to execute a C application.

## Usage

$> heroku create myapp_name -s cedar
$> heroku config:add BUILDPACK_URL=https://github.com/atris/heroku-buildpack-C.git

# create your app, see test-app for an example

$> git push heroku master

-----> Heroku receiving push
-----> Fetching custom git buildpack... done
-----> C app detected
-----> makefile found
makefile:4: *** missing separator.  Stop.
-----> Compilation done
-----> Discovering process types
       Procfile declares types -> (none)
-----> Compiled slug size: 4K
-----> Launching... done, v5

