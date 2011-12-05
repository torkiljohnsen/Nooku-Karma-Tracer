# Ye olde Nooku Karma Tracer

This is the home of my effort to map karma in the Nookusphere. Karma is the main currency of exchange in such a young ecosystem and to increase the impact of karma, it needs to be visible.

Instead of some sort of canonical blogging effort, however, I will try to solve this like a programmer would: With git.

Right now, karma exists as developers submitting work to repositories. What is missing is a way to string those together, and this is where the nooku karma tracer comes in.

## Data Structure of the nkt

The core of nkt will be nothing but a collection of json files - a large, coordinating one and one for each developer involved. I will curate the big list, but the small files will be written by the individual developers (with me providing a basic syntax for making one). Submitting a file to me will happen as pull requests, so you'd need to keep a local copy of nkt, which also means that this concept is inherently decentralized. The basic features (showing you a birds-eye view of the community) will always work offline, if need be, ie. - you can always open nkt in your browser locally.

The json file that developers provide will look something like this:

    {
       "dev":{
          "name":"David Deutsch",
          "handles":[
             "daviddeutsch",
             "skore"
          ],
          "affiliation":"valanx",
          "twitter":"@skore_de"
       },
       "projects":[
          {
             "name":"Cool Project 1",
             "description":"Just another cool project",
             "handle":"cp1",
             "repository":{
                "type":"git",
                "location":"git@github.com:daviddeutsch/cp1.git"
             }
          }
          {
             ...
          }
       ]
    }

All of this is subject to change, of course. (And again - keeping this as a public repository means that if I change the syntax, it would mean that >I< would have to maintain your files and you could then pull the updates if you want to push your own changes back.)

## Visualization

The nkt will mainly be about displaying all available data as a Big Frigging Map - visualized through d3.js. Projects and developers would be the major entities and there will be connection between developers (collaborations), projects (dependencies) and of course between both (showing who works on what, directly).

## Future plans

I would really LOVE to get into running statistics on the repositories, so I will probably look into this as a second step. Statistics will help weigh the developer graph around nooku, boosting egos left and right. Cause that's what we're in for, right?