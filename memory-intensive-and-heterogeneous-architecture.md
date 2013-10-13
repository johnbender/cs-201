# Uri Weiser, Memory Intensive and Heterogeneous Architecture

Professor Weiser's presentation covered two main areas of his research. Initially he set the stage for his work by describing the existing state of processor research and how it is motivated by the computing requirements of todays market. In particular he discussed how performance unit per power unit has become extremely important in the market and in research.

He then discussed some of the work his research group has done with heterogeneous architectures and determining the optimal architecture with a given set of constraints. It's well know that task specific processing units can deliver very serious performance per power benefits by sacrificing generality. One of the primary contributions of his research in this area is to view the problem as a search for the local maxima and minima for a given constraint (eg, power consumption) where a given program executes different portions on different components in a heterogeneous architecture.

He also discussed how memristors are providing very fruitful ground for research because they don't require refreshes like traditional RAM. The main example he illustrated was layering memristor based memory above the processor pipeline on-die. The idea was to "swap" pipeline executions out to the memristor layer when fetch from cache or main memory happens. The reduced power consumption of memristors means this approach provides legitimate performance/power benefits for most execution contexts. It was also pointed out at the end that this type of architecture is not likely to be adopted because of the way it radically departs from the existing architectures of the main processor manufacturers.