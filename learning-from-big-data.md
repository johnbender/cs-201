# Prof. Tyson Condie - Learning from Big Data

Data is everywhere
- easier and cheaper than ever to get
- data grows faster than moore's law
- hadoop is the current solution for big data (map reduce)
- every two days we produce as much data as we have from the dawn of civ to 2003

Gold Rush
- value in the data
- demonstrated by google facebook
- untapped by most orgs
- lots of data not much used
- data is hard to deal with
- unstructured
- questions are hard

- tools are new, map-reduce doesn't work well with ML

Turing Data into Value
- "money"
- why is user engagement dropping
- ddos attack?
- decisions like what features, personalized medical treatment
- what ads show
- data is only as good as the decisions we derive from it

Machine learning is programming by example
- used when programming is hard
- used when program would need to change constantly
- goal: take huge data and apply learned model
- supervised: classification, regression, and recommendation (~80%)
- unsupervised: clustering, dimensionality, topic modeling

Machine learning workflow
- 1 example formation
- 2 modeling
- 3 evaluation on test set

Example of formation
- email => id: bag of words
- click log => id: label
- often done with hadoop
- example formation, evaluation easy in hadoop
- modeling is hard in hadoop

Learning is iterative
- apply model
- observe issues
- improve model

What normally happens
- examples are put on a single machine (not scalable)
- r / matlab
- output goes to evaluation machines

Distributed Learning
- Hadoop doesn't support iterations
- Hadoop only supports single pass
- 30x slowdown compared to custom solutions
- hacked to use map only jobs, hadoop "abused" to manage machine resources

Abuse: Allreduce and friends
- traversal up and back down the tree

Abuse: Graph view
- message passing with all other nodes
- open source version of Pregel

Many other systems:
- graphlab, pregel
- apache spark
- madlib
- VW
- distbelief
- hyracks

Need for Unification
- todays analytics stack
- data batch/hadoop

Build Unified Big Data Runtime

Resource Manager
- cloud resources
- "Cloud OS"
- nodes, etc
- alternates: apache Yarn, apache mesos, google omega, facebook corona

Hadoop v1
- jobtracker central manager
- task trackers for many nodes connected to jobtracker

YARN (hadoop v2)
- resource manager: broker/api for clients
- resource pool (cpu, mem, disk)
- blocks on app master response when query resource levels
- Google's approach uses an optimistic approach

The Challenge
- mapping the various and varied tasks to these cloud OS systems
- batch (map reduce) needs robustness in the face of failure of nodes, and fast networks
- streaming load spikes, elastic resource needs

REEF
- framework that solves this for YARN at MS
