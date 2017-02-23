# Aframe Go 🚀

This is my StarterKit for Aframe. There are many like it but this one is mine.

My StarterKit is my best friend. It is my life. I must master it as I must master my life.

---

I created this using the things I used all the time for building prototypes and fleshing out ideas when working with Aframe. Its goals are simple. I want to go from idea to deploy as quick as possible and use all the things that I like to use. This isn't supposed to be prescriptive or 'The RIGHT way', just A way, a way that I like. 

I want to use Pug  ( because I like it )

I want to use Scss ( because I like it )

I want to write ES6 ( samesies )

I want to deploy to surge ( it's pretty quick and cool ) Why not Github? [Reasons can go here]

---

### Dependencies

`budo`
Development server, supports browserify and livereload
`imagemin`
minify images
`node-sass`
Compile Sass
`npm-run-all`
nice way to run tasks syncronosly and paraelle without all the && || and &
`onchange`
Watch files for changes and then run a task
`pug` & `pug-cli`
To compile Pug templates
`rimraf`
A nice removal module - works on windows too

You have to have surge installed globally, run `npm install surge -g` for deployment.

### I usually add additional tasks depending on the project. 

Move models from a src folder to a dist folder for deployment
Move other media types ( sounds and videos etc )

### Tasks


```
"start": "run-p start:budo watch:* & wait"
```

`npm start` runs budo and watch tasks in parallel - budo starts a local server on port `3000` along with livereload.

```
"prebuild": "rimraf dist/assts/{css/*,js/*,images/*}",
```

Before the build task - we clear out old files

```
"build": "run-s build:*",
```

Runs all of the build tasks syncronously.

```
"deploy": "run-s build deploy:upload"
```

`npm run deploy` runs all the build tasks 


Change `{YOUR.SURGE.SH DOMAIN}` to a domain you'd like to use on surge, for example, `timetravelstuff.surge.sh`




