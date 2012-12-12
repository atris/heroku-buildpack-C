# Heroku Buildpack: C

Use C-Buildpack if you need Heroku to execute a C application.

## Usage

NOTE: The C app being deployed with this buildpack needs a makefile that will specify the build rules of the project.

<br>$> heroku create myapp_name -s cedar
<br>$> heroku config:add BUILDPACK_URL=https://github.com/atris/heroku-buildpack-C.git

# create your app, see test-app for an example

$> git push heroku master

<br>-----> Heroku receiving push
<br>-----> Fetching custom git buildpack... done
<br>-----> C app detected
<br>-----> makefile found
<br>makefile:4: *** missing separator.  Stop.
<br>-----> Compilation done
<br>-----> Discovering process types
       <br>Procfile declares types -> (none)
<br>-----> Compiled slug size: 4K
<br>-----> Launching... done, v5

