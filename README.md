# Welcome to the HackOregon front end app!

## Philosophy
The core Hack Oregon application is meant to expose answers to 4 main questions about campaign finance using open data:   
**who?**  Who is being funded, and by which PACs, Corporations, and individuals.    
**what?**  What are the outcomes of campaing finance dollars at work?  (good or bad)    
**when?**  When do cycles of campaign and funding take place and how does this effect the political process and civic life?    
**where?** What does the breakdown of donors/funders look like in Oregon and how does 'place' effect the political process?

Components for the core application lives at the top level of each directory.  Additionally, in each folder there is a `community` folder for contributions that do not relate to the core application, but should exist on their own.

** TODO add gist viewer (like bl.ocks.org) to allow easy integration of community apps **

## Getting started    
We're using yeoman for workflow.  
```
#Install yeoman:
npm install -g yeoman
git clone <this_repo>
cd <this_repo>
#install node packages:    
npm install
#install bower and front end dependencies:
bower install
```

Once everything is installed run:    
`grunt serve`    
to get your development server fired up.   

## Getting aquainted with things
Hack Oregon's front end is contained in an [Angular JS app](http://angularjs.org).   

Additionally, we are using [SASS](http://sass-lang.com/) which compiles into css and [coffeescript](http://coffeescript.org).  

**Adding new styles:** add a partial to the styles folder e.g. `_mypartial.scss` and then include the partial in the `main.scss` file with an import statement `@import '_mypartial';`  If you prefer to use plane css, simply import it by adding an import line to the `main.scss` file: `@import plainolcss.css;`

**Adding scripts:** More documentation *to come.*  In the mean time, read about how to add to the angular application with the yeoman angular-generator [here](https://github.com/yeoman/generator-angular).  Using angular generator you can add new routes, controllers, views, etc. with the simple commands listed in their [documentation](https://github.com/yeoman/generator-angular).  For example,    
`yo angular:route myAwesomeRoute`   
This will create a new route, a new controller for that route, as well as an html view that will be rendered at that route.  If you are a javascript purist, you can run the same command with a flag that tells the generator to use javasript.  For example,   
`yo angular:controller myAwesomeCtrl --coffee=false`

We will be updating the grunt file as the project progresses to make it easy for coffee script and javascript to coexist.    

## Contributing
**OUTDATED**

You probably have some amazing ideas, and things you'd like to contribute - we'd love to include them.  There are two main ways to contribute:

1. make the core 'who', 'what', 'when', 'where' application better,
2. include your own data visualization that uses data from our [API](https://github.com/hackoregon/hackoregonnode) or a data set that you think is important.


In either case here are the steps you should take:
`fork this repo`    
`git clone <your_fork>`    
`git checkout -b <your_awesome_new_feature>`    
`git branch -D master`    
hack away!

When you feel like you are ready for your visualization or enhancement to be included submit a pull request.  There may be some things to change (especially if you are working on the core application) and we'll work together to get things running nicely.

If you are working on a visualization that is not one of the 'who', 'what', etc. parts of the application, pick a unique name for your visualization and then you can include everything you need under the `community` folder.  Convention is to use the name of your viz as the prefix for any components you add to the app.  E.g. if you are creating a new directive for your feature, it should live in the `app/scripts/directives/community` folder and if the route is `mynewfeature` you should call the file `myNewFeatureDir.{js/coffee}` with a directive of the same name `myNewFeatureDir`.  This can then be used as `<my-new-feature-dir></my-new-feature-div>` within your template.

