I worked with Alasdair Rae on an application of Combo to commuting data in Scotland. I have recently revisted the tool with the aim of making some adjustments to the output files.
SInce it has been a wile since I used the programme, I have cloned the repository from Casyfill and Express50, whose orginial readme is included below...


# Combo

I came across this neat tool in reading Alasdair Rae and Garrett Dash Nelson's
beautiful [An Economic Geography of the United States: From Commutes to
Megaregions](http://journals.plos.org/plosone/article?id=10.1371/journal.pone.0166083)
in _PLOS One_. Unfortunately, the code wasn't contained in a repository
anywhere, only available in `zip` form from the [Senseable
Cities](http://senseable.mit.edu/community_detection/) website. For my ease, I
put it here. What follows is more or less their original README.

## Description

This is an implementation (for Modularity maximization) of the community
detection algorithm called "Combo" described in the paper "General optimization
technique for high-quality community detection in complex networks" by
Stanislav Sobolevsky, Riccardo Campari, Alexander Belyi and Carlo Ratti.
Please, send your feedback, bug reports and questions to:

alexander.belyi@gmail.com

If you use this code, please, cite:

```
Sobolevsky S., Campari R., Belyi A., and Ratti C. "General optimization technique for high-quality community detection in complex networks" Phys. Rev. E 90, 012811
```

## Running

First you'll need to compile the program. If you're on a Linux/Mac box, make
sure you have `g++` installed, and then run

```
make
```

Once compiled, you can run the program with

```
./comboCPP path_to_network_file.net [max_number_of_communities] [mod_resolution]
```

The options are as follows:
* `path_to_network_file` - path to the file in Pajek .net format
* `max_number_of_communities` - maximal number of communities to be found
  (default is "INF" for infinite)
* `mod_resolution` - modularity resolution parameter (default is 1)
* `file_suffix` - suffix appended to output file (default is "comm_comboC++")

For example, you can make sure the compilation worked correctly by running:
```
./comboCPP karate.net
```
on the included `karate.net` file.

## The Output

The program outputs one file named `path_to_network_file_<file_suffix>.txt`
containing numbers of communities for each vertex on separete line.  And it
writes achieved modularity score to standart output.
