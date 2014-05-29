# Stefano Carpin - Robotic Search: Theory and Practice

Mr. Carpin began by defining what "search" meant for the domain of Robotic Search. Informally he characterized it as finding things in an environment where things might be fundamental like food and water. More generally any activity that is critical but very time consuming and most often when there is a large search area and the search target is small. Additionally robots can and should be used to find missing humans from downed aircraft, stranded hikers, or in the aftermath of a disaster when the first 72 hours are critical for survival.

Robots have many obvious advantages when performing these tasks, many can be used at once and, especially in disasters there is a significant reduction in risk for humans assisting in the rescue effort. To this end there is a competition each year to search an urban environment called the Robocup Urban Search.

He further discussed the directions that his research is proceeding in this domain: map merging, hierarchical search, fast deployment, and more. His research groups primary tool is the quadrocopter which has become ubiquitous of late, though the version they use is expensive and extremely well equipped relative to the consumer models available today.

He also covered in detail the trade-offs in elevation based image search that are completely intuitive in hindsight. Primarily that, when the quadrocopter is close to the ground or the target search area the detail is high and the results are accurate, but when the 'copter moves away from the ground it can see much more but with less detail and accuracy. The ideal solution uses elevation as a tool for refining candidates.

Their approach leverages quadtrees as a theoretical basis for their search refinement algorithm with each internal node having smaller children made up of its internal area. Then probabilities are assigned to each area with the probabilities being rolled up to the parent nodes which represent higher levels of elevations.

All together the results were impressive!
