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
```

LICENSE:

```
            DO WHAT THE FUCK YOU WANT TO PUBLIC LICENSE
   TERMS AND CONDITIONS FOR COPYING, DISTRIBUTION AND MODIFICATION

  0. You just DO WHAT THE FUCK YOU WANT TO.
```
