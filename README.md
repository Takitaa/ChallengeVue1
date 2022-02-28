# vue1-challenge

> SidePanel chat video-player challenge

## Environment Setup

```
npm install vue
```

```
npm install vue@csp
```

```
Vue Cli version 5.0.1
```

Making sure it's Vue 1

```
 npm install  vue@1.x latest
```

It found vue@1.0.28

> Following Vue 1 documentation I should do
> $ npm install -g vue-cli
> $ vue init webpack my-project
> $ cd my-project
> $ npm install
> $ npm run dev

> Because I already had vue cli I skiped this part

```
vue init webpack Vue1-Challenge
```

ERROR . it asked for the vue cli

```
$ sudo npm I -g @vue/cli-init
```

(without sudo it cried about permission because of the -g)

```
$ vue init webpack Vue1-Challenge
```

Setup as it happens tu $vue create
It complained about the capital letters - this scared me that I would still be inside a Vue 3 setup or something, but soon different options appeared such as viue-router, test, etc.

> Jest or Karma - Mocha test environment?
> What is one or the other?!?! hihihi<br>
> Searched about what those were, advantages etc (my heart was already proned to Karma/Mocha for the flexibility of having two tools to help - what one wouln't cover, the other could...)<br>
> BINGO! Jest didn't seeme worth it for Vue projects, plus much documentation to setup as a down side they said.

> Looooooonnnng Terminal information about hundred different installation.

> Project initialization finished!

```
cd Vue1-Challenge
npm run dev
```

> localhost:8080 up and running

> VS folder has /build on it with webpacks inside, a /config

## Adding video-player

> Version 1 - tried vue-core-video-player
> Version 2 - vue-core-video-player with something different (I didn't specified what but this seems added to App.vue)
> Version 3 - still same library, however following step-by-step from youtuber guy

```
ctrl + z
```

Back to zero - starting point

> Tried the video library used in the Inspiration Code. Tried their documentation but couldn't figure out where should I add the CDN, cheated looking up in Inspiration Code. Hmmm HTML, ok. I had added the scripts given in the documentation to my App.vue template area.

> Got some videos of my own (Honda Grr and Honda the Impossible Dream converted from YouTube - not all of them work well but one works, honda and grr files)

> I wanted to use something not given, even though I stumbled into this library by myself first.

> Version 4 - using vjs-no-vjs, it finally works (it's like this in my notes but the one I know works is vue-vam, maybe I got blocked with vjs at some point and switched to vue-vam)
> Only remote videos work, tried adding /assets to /dist, added working video files to /dist, still didn't work

> It autoplayed perfectly at first and then occasionally, leaving the play button on the screen (>) to finally not autoplay it.

## Sidepanel

> had a good source, it added the button (not toggleable) chat (it looked like Win 31) just under the video, we could click and all but the css was not yet there so nothing happened.<br>

```
$ npm install -D node-sass sass-loader
```

Actually sass could not be configurated/installed via npm due to "depedency conflict", later suggesting the version was not good - webpack I have is 3.6.0.

```
import /./styles/my-styles-scess  - in VS

<style lang="scss">
```

I had issues with my file name as it should have .module on it (example name.module.scss). I corrected it.

> Sass loader broke the browser, VS stepped in suggesting for me to get an extenstion, which I have: Live Sass Compiner and Sass

> UPDATE about video-player: now I see that while I struggled with the sidepanel, the video-player was still hanging and broken, I managed to implement vjs code as seen [here](https://jsfiddle.net/u69gnx90/) only to see {{message}} as displayed in this playground. Imanaged to display it once I had properly installed the npm which somehow scaped me - I noticed the error I was having for Sass with issues on the npm looked alike the ones I was having from the video player 💡 and BINGO!

Only then I switched to [vue-vam-video ](https://github.com/maomincoding/vue-vam-video)- not a fan of the asian characters going on in the code though.

## Mock async call Infinite Scroll

Source [here](https://learnvue.co/2020/09/a-quick-vue3-infinite-scrolling-component-daily-vue-tips-4/#handling-vue3-infinite-scrollin)

```

```

## Build Setup

```bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report

# run unit tests
npm run unit

# run e2e tests
npm run e2e

# run all tests
npm test
```

For a detailed explanation on how things work, check out the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
