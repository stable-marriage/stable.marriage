#Details
-------
This project contains the implementation of algorithms that solve the stable marriage problem. (https://en.wikipedia.org/wiki/Stable_marriage_problem)

Algorithms implemented from the literature:
* Gale-Shapley [https://www.researchgate.net/publication/228108175_College_Admissions_and_Stability_of_Marriage]
* MinRegret [https://dl.acm.org/citation.cfm?id=23802]
* MinEgalitarian [https://dl.acm.org/citation.cfm?id=28871]
* Approx [https://dl.acm.org/citation.cfm?id=1868239]
* DACC [https://dl.acm.org/citation.cfm?id=2940727]
* BiLS [https://www.researchgate.net/publication/312256504_A_Bidirectional_Local_Search_for_the_Stable_Marriage_Problem]

Novel algorithms implemented:
* PowerBalance: proposal-based algorithm that tries to keep a good balance between both sides and then terminates by a compromising procedure
* iBiLS (refined version with rotations)
* Hybrid, HybridMultiSearch: combinations of PowerBalance with the local search method

#Usage
-----
Clone from github and run:
```
mvn package
```
To run an algorithm with random input (uniform lists) you can execute the following classes from the produced jar:

*algorithms.(algorithm)*

OR

Run experiments with lists drawn from diverse distributions and plot results:

* cd scripts
* Create dataset (*create_data.sh*)
* cd Experiment_*
* Run the algorithms (*run.sh*)
* Plot (*do_plots.sh*)

The raw outputs and plots are placed in the results directory.

There is also the option to produce and run zipped input files to save space.

#Dependencies
-----
For the plotting scripts you need:

* pip install numpy
* pip install pandas
* pip install seaborn
* sudo apt-get install python-tk
* sudo apt-get install texlive-full

Tested on Ubuntu 18.04.