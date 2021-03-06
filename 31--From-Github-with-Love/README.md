# 30 -- From Github With Love

## Rituals (~1h 15m)

* **Standup Meeting** (~15m)
* **Three Little Things** (~30m)
* **Homework Review** (~30m)

## Tools on Tuesday

* **Hello, Angular JS!**
  * What is Angular JS?
    * Client-side JavaScript Framework
    * 2-way Data Binding: Reactive View
    * Modular, Service-Oriented Architecture
    * Dependency Injection FTW!
  * How do I use it?
    * `bower install --save angular`
    * `wiredep -s index.html`
    * in `src/js/main.js`: `angular.module('module-name', [ ])`
    * in `src/index.html`: `ng-app="module-name"`
    * What happened to all our placeholders?
  * Attaching data to the View? Use a Controller...
    * in `src/js/main.js`: `.controller('MainController', function(){ })`
    * in `src/index.html`: `ng-controller="MainController"`
    * What goes inside the Controller?
    * Attach data to `MainController`... But how?
    * Add `as app` to `ng-controller` directive...
    * ...and change placeholders.
  * What about my JSON data? Can I use `jQuery.getJSON` like before?
    * Yes, but what is `this` inside of `then`...?
    * Yes, but no. Use [`$http`](https://docs.angularjs.org/api/ng/service/$http) instead...
    * Well, that was different... Try `.success` instead.
* **Intermission**
* **Shave that Yak...**
  * `yo gulp-webapp`
    * `tree | less`
    * `package.json`
    * `bower.json`
    * `gulpfile.babel.js` (WTF?)
      * What is `babel`? AKA `npm home babel`
      * [JavaScript is an ogre...](https://en.wikipedia.org/wiki/ECMAScript)
      * [Ogres are like onions...](http://shaunlebron.github.io/solar-system-of-js/#0)
      * Welcome to [ES6 / ES2015 / hell](https://babeljs.io/docs/learn-es2015/)
    * Okay, but can you read it?
      * `gulp serve`
      * `gulp serve:test`
      * `gulp html` (aka `build`)
      * `gulp serve:dist`
  * `bower install --save angular`
    * in `app/scripts/main.js`:
      * define module `tiy-gradebook`
      * define controller `MainController`
    * in `app/index.html`:
      * attach `tiy-gradebook` with `ng-app` directive
      * attach `MainController as app` with `ng-controller` directive

## Assignment

```markdown
* [ ] **Yak Shaving**
  * _WIP Issue_: `31 -- From Github With Love -- YOUR NAME`
    * Links to PRs in:
      * `USERNAME.github.io`
        * `journal-week-7` into `master`
        * `feature/*` into `remodeling`
        * `remodeling` into `master`
      * `TIY-Gradebook`
        * `feature/cached-data` into `develop`
        * `feature/mockups-repositories` into `develop`
        * `feature/mockups-milestones` into `develop`
  * _WIP Branch_:
    * `USERNAME.github.io`
      * `journal-week-7` -- journal entries
      * `feature/*` -- (small) feature branches
      * `remodeling` -- merged features
    * `TIY-Gradebook`
      * `master` -- _only_ release `0.0.0`
      * `develop` -- _only_ merged features
      * `feature/cached-data` -- saved data from the Github API
      * `feature/mockups-repositories` -- HTML+SCSS for Repositories list
      * `feature/mockups-milestones` -- HTML+SCSS for Milestones list
  * _WIP Files_:
    * `TIY-Gradebook`
      * `api/github/` -- cached API data!
      * `app/`
        * `scripts/`
          * `main.js` -- no need to break it up... yet
        * `styles/`
          * `main.scss` -- don't forget to `@import`
          * `_repositories.scss`
          * `_milestones.scss`
        * `views/` -- copy `index.html` to start
          * `repositories.html`
          * `milestones.html`
        * `index.html`
      * `bower.json` -- need Angular JS _and_ Bootstrap!
      * `gulpfile.babel.json`
      * `package.json`
* [ ] **Journal, Week 7: Any Way You Want It**
  * Feature 1: Complete!
  * Feature 2: Started!
  * Feature 3: Planned!
* [ ] **Reading APIs: Github Issues**
  * What credentials do I need to authenticate with the Github API?
  * How can I provide authentication credentials to Github?
* [ ] **API Gymnastics**
  * [ ] Fetched Repositories for `TheIronYard--Orlando`...
  * [ ] Fetched Milestones for `2015--SUMMER--FEE`...
  * [ ] Fetched Labels for `2015--SUMMER--FEE`...
  * [ ] Fetched Issues for `2015--SUMMER--FEE`...
    * [ ] ...with label "Attendance".
    * [ ] ...with any Milestone assigned.
    * [ ] ...with _no_ Milestone assigned.
* [ ] **Shaping Up with Angular JS**
  * [ ] Completed Level 1!
  * [ ] Completed Level 2!
  * [ ] Pics or it didn't happen!
* [ ] **From Github With Love**
  * [ ] Installed Bootstrap... if necessary.
  * [ ] Adjusted and ran `gulp wiredep`...
  * [ ] `feature/mockups-repositories`
    * [ ] Start with a [`.list-group`](http://getbootstrap.com/components/#list-group)...
    * [ ] Links would be nice...
    * [ ] Maybe more semantic HTML would help...
    * [ ] How about one with placeholders?
    * [ ] **BEAST MODE** Use `@extend` instead?
  * [ ] `feature/mockups-milestones`
    * [ ] Also probably a [`.list-group`](http://getbootstrap.com/components/#list-group)...
    * [ ] But what's that nifty [`.progress-bar`](http://getbootstrap.com/components/#progress)?
    * [ ] Some labels and colors would be nice...
    * [ ] Don't forget links!
    * [ ] Try that semantic HTML one more time...
    * [ ] Put some placeholders in one...
    * [ ] **BEAST MODE** It's called semantic CSS...
  * [ ] `feature/cached-data` -- DID YOU READ API GYMNASTICS!?
```

### Journal, Week 7: Any Way You Want It

Welcome to Tuesday! Math quiz: if three features leave the station and are due on Thursday, how many should be complete by tonight? Remember that people who were _not_ on your team should be reviewing your journals this week. Hooray!

### Reading APIs: Github Issues

Please answer any of the questions from Monday that you didn't get to and additionally refresh your memory (and notes) on how authentication works with the Github API by answering these questions:

  * What credentials do I need to authenticate with the Github API?
  * How can I provide authentication credentials to Github?

### API Gymnastics

Gonna need some data from that API, y'all. Create a directory called `api/github/` and start putting cached JSON data in there. We'll need a list of all the Repositories for `TheIronYard--Orlando`, the list of Labels and Milestones for _our_ repo -- `2015--SUMMER--FEE` -- _and_ a bunch of Issies for that repo. Any potential problems there? I mean, how many can there be, right?

### Shaping Up With Angular JS

Last night was a (very) quick tour of the course. Tonight is reinforcement: play through (as in, try to complete without help) levels 1 and 2. You've got a lot to do tonight, so don't spend too much time here. If you get stuck, buy the answer and move on. Tomorrow you'll do the same with levels 2 (again) and 3. It'll come back around.

### From Github With Love

In `TIY-Gradebook`, you're working in your teams on basic mockups of the two main pages in the application: the Repository list and the Milestone list. Ensure that you've got Bootstrap included in your project, and review the [List Group](http://getbootstrap.com/components/#list-group) and [Progress Bar](http://getbootstrap.com/components/#progress) components. Using lorem ipsum and / or hard-coded values from the API data to create _at least three_ dummy list items for each view.

#### BEAST MODE

If you selected both Bootstrap and Sass when you used `yo gulp-webapp` then you got `bootstrap-sass` -- the Sass port of Bootstrap -- as a dependency, which means you can `@extend` those classes instead of just assigning them to HTML elements. That would be a more... sophisticated approach.

## Resources

* **How do I learn more about this EcmaScript 6 / 2015 / 2016 / 7 mess?**
  * https://en.wikipedia.org/wiki/ECMAScript
  * https://babeljs.io/docs/learn-es2015/ -- taken from https://github.com/lukehoban/es6features/blob/master/README.md
* **How do I learn more about tagging and releases?**
  * [`git` Basics: Tagging](https://git-scm.com/book/en/v2/Git-Basics-Tagging)
  * [`git tag`](http://git-scm.com/docs/git-tag)
  * [_Release Your Software_ on Github.com](https://github.com/blog/1547-release-your-software)
  * [Releases in Github Help](https://help.github.com/categories/releases/)

