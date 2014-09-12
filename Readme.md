A Heroku buildpack to figure out what the fuck is going on up there.

I'm using it like this:

```sh
$ heroku buildpacks:list | grep multi
ddollar/multi
vizify/multi

$ heroku buildpacks:set vizify/multi
Modifying BUILDPACK_URL for turingschool-moi... done

$ cat .buildpacks
https://github.com/JoshCheek/heroku-buildpack-fuck-everything.git
https://github.com/JoshCheek/heroku-buildpack-for-cmake-and-pkg-config.git
https://github.com/heroku/heroku-buildpack-ruby.git

$ git commit -m 'Empty commit so I can push to Heroku again' --allow-empty
[master 76c99a4] Empty commit so I can push to Heroku again

# output snipped to just show what this outputs and hide maybe sensitive values
$ git push heroku master:master
[SNIP]
-----> Fetching custom tar buildpack... done
-----> Multipack app detected
=====> Downloading Buildpack: https://github.com/JoshCheek/heroku-buildpack-fuck-everything.git
=====> Detected Framework: FuckEverything
The fuck everything script
  AKA what the fuck is going on up there, Heroku?
________________________________________
ENV:
  {"DEPLOY"=>"production",
   "DYNO"=>"receive.9742",
   "GROUP"=>"production",
   "HOME"=>"/app",
   "LOGNAME"=>[SNIP],
   "LOGPLEX_URL"=>"https://east.logplex.io/logs",
   "LOG_TOKEN"=>[SNIP],
   "MAIL"=>[SNIP],
   "OLDPWD"=>"/app/tmp/repo.git",
   "PATH"=>
    ":/tmp/codon/vendor/bin:/app/bin:/usr/ruby1.9.2/bin:/usr/local/bin:/usr/local/sbin:/usr/bin:/bin:/usr/sbin:/sbin",
   "PWD"=>"/tmp/buildpackIr1dt",
   "REQUEST_ID"=>[SNIP],
   "SHELL"=>"/bin/bash",
   "SHLVL"=>"2",
   "SSH_CLIENT"=>[SNIP],
   "SSH_CONNECTION"=>[SNIP],
   "STACK"=>"cedar",
   "USER"=>[SNIP],
   "_"=>"/tmp/buildpackIr1dt/bin/compile"}
________________________________________
ARGV:
  ["/tmp/build_126e18e7-16dd-49c7-b77c-bc7ff6b6122f", "/app/tmp/cache", "/tmp/d20140912-317-t1s0je"]
Files in "/tmp/build_126e18e7-16dd-49c7-b77c-bc7ff6b6122f"
  "example.gif"
  "Rakefile"
  "Gemfile.lock"
  "lib"
  "Procfile"
  ".buildpacks"
  "Readme.md"
  "config.ru"
  ".gitignore"
  ".profile"
  "spec"
  "features"
  "Gemfile"
Files in "/app/tmp/cache"
  ".bundle"
  "vendor"
  "cedar"
Files in "/tmp/d20140912-317-t1s0je"
  "RACK_ENV"
  "BUILDPACK_URL"
  "LANG"
________________________________________
Values of files in ARGV[2] aka /tmp/d20140912-317-t1s0je
  RACK_ENV:
    production
  BUILDPACK_URL:
    https://codon-buildpacks.s3.amazonaws.com/buildpacks/vizify/multi.tgz
  LANG:
    en_US.UTF-8
________________________________________
STDIN:
  ""
[SNIP]
```

LICENSE:

```
            DO WHAT THE FUCK YOU WANT TO PUBLIC LICENSE
   TERMS AND CONDITIONS FOR COPYING, DISTRIBUTION AND MODIFICATION

  0. You just DO WHAT THE FUCK YOU WANT TO.
```
