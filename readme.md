# Heroku Buildpack: Ø

Use C-Buildpack if you need Heroku to execute a C application.

## Usage

Create a directory for our Heroku app:

```bash
$ mkdir -p myapp/bin
$ cd myapp
```

Here is an example of an executable that will run on 64bit linux machine:

```bash
$ echo -e "#\!/usr/bin/env bash\n echo hello world" > ./bin/program
$ echo -e "program: bin/program" > Procfile
$ chmod +x ./bin/program
$ ./bin/program
hello world
```

Push the app to Heroku and run our executable:

```bash
$ git init; git add .; git commit -am 'init'
$ heroku create --buildpack http://github.com/ryandotsmith/null-buildpack.git
$ git push heroku master
$ heroku run program
Running `program` attached to terminal... up, run.8663
hello world
```

## Motivation

I wanted to run various executables (e.g. [log-shuttle](https://github.com/ryandotsmith/log-shuttle)) on Heroku without compiling them on Heroku. Thus, I compile programs on my linux 64 machine, or fetch the binary from the project, commit them to a repo and then run them on Heroku with the Ø buildpack.

## Issues

You will need to make sure that a 64bit linux machine can execute the binary.
