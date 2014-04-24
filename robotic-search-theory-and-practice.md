# Stefano Carpin - Robotic Search: Theory and Practice

search
- find things in an environment
- fundamental (water, food)
- critical, time consuming
- domain is large search target is small

human search
- downed aircraft
- stranded hikers
- disaster aftermath
- locate intruder
- stress detection for crops
- critical, time consuming, potentially dangerous
- after disasters 72 hours is critical

robotic aid
- many robots
- less danger for searchers
- humans can participate

robocup urban search
- urban search competition for robotics
- many different goals/activities

research directions
- map merging
- hierarchical search
- fast deployment
- graph clear
- wifi localization

hierarchical search

motivation
- quadrocopter
- resolution of images is not fixed
- search for item of interest in an image
- integrates existing information
- close:precise further:more area
- results mapped to actions

uniform grids
- standard
- lawn mower search pattern
- closed form bayes updates

variable resolution accuracy
- error rate sky rockets as elevation increases
- not necessarily monotonic

Goal
- design an efficient variable resolution data
- bootstrapped from uniform reps.
- online updates
- inform searchers route
- eventually make search decisions

Quadtrees
- rooted tree
- 2 : binary as 4 : quad

prob. quadtree
- probability assigned to every area
- relationship with elevation, higher == more levels of the tree

One step lookahead planning
- what is the best next place to look

online updates
- look further at nodes in the tree that return promising information

online belief updates
- update the whole tree
- linear in the size of the tree
- low probability at the root of the tree determines moving to another area
- or the leaf surpasses a certain value and the search is done

field validation
- experiments at Millan air feild camp
- restricted airspace not subject to FAA

experimental platform
- brushless motor
- experiment
- fast, 30 min battery life, camera, gps, no onboard computation
- bad images
- wobbly

results
- varied height matters
- hierarchical results are much better on raw detections
- timeouts higher on lawn mower for uniform grid
- average time to detection is better for hierarchical search
