# Analysis of Apache Cassandra to Identify items that can indicate ATD.

Proposed Approach

Figure 1 ![Proposed Approach](https://anonymous.4open.science/r/mycassandra-32D3/images/SummaryofSysRepoAnalysis.png)

Steps of Approach

Figure 2 ![Steps of Approach](https://anonymous.4open.science/r/mycassandra-32D3/images/AnalysisCassandraRepositoryFlow.png)

We analyzed all commits from 2015 to 2021 related to versions from 3.0.0 to 3.11.11, encompassing six years of maintenance and evolution of the [Apache Cassandra](https://github.com/apache/cassandra) project. 

We saved all commits and all modified files using the [Pydriller](https://github.com/ishepard/pydriller) tool.

We used the [Arcan](https://essere.disco.unimib.it/wiki/arcan/#:~:text=Arcan%20is%20a%20Java%20software,are%20less%20stable%20than%20itself.) [1] tool and [Designite](https://www.designite-tools.com/) to extract Architectural Smells [2] and Design Smells [3], respectively. 

We loaded these datasets and performed an exploratory data analysis, using various Python libraries and Data Science techniques to identify patterns that could characterize ATD in source code repositories.

We calculated the following metrics to aid our analysis: *cyclomatic complexity*, *file occurrence in commits*, and *accumulated modified LOCs* over time to analyze the source code's behavior related to the maintenance effort. Besides, we used the following Archictural Smells to select files that can indicate architectural issues: *cyclic dependency* and *hub-like dependency*.

You can access [Analysis of Cassandra](https://github.com/armandossrecife/mycassandra/blob/main/scripts/Analysis_of_Cassandra_Repository_DB%2C_Dataframes%2C_Architectural_Smells_e_RQs.ipynb) to get data collection, analysis, and case study results.

You can access [Analysis of Metrics Behavior](https://github.com/armandossrecife/mycassandra/blob/main/scripts/Analysis_of_the_behavior_of_files_with_ATD_of_calculated_metrics.ipynb) to get details about how each analyzed metrics behavior over time.

You can access [Critical files and dependents with co-change](https://github.com/armandossrecife/mycassandra/blob/main/scripts/Graph_of_Critical_Files_and_Dependents.ipynb) to get details about critical files and impacted files with co-chage.

You can access [Cassandra Treemap Repository](https://github.com/armandossrecife/mycassandra/blob/main/data/treemaps.md) to get treemap visualization for each variable analysed.

[[1]](https://dl.acm.org/doi/abs/10.1145/2851613.2851963) Fontana, F.A., Pigazzini, I., Roveda, R., Tamburri, D., Zanoni, M. and Di Nitto, E., 2017, April. Arcan: A tool for architectural smells detection. In 2017 IEEE International Conference on Software Architecture Workshops (ICSAW) (pp. 282-285). IEEE.

[[2]](https://ieeexplore.ieee.org/abstract/document/4812762) Garcia, J., Popescu, D., Edwards, G. and Medvidovic, N., 2009, March. Identifying architectural bad smells. In 2009 13th European Conference on Software Maintenance and Reengineering (pp. 255-258). IEEE.

[3] Suryanarayana, G., Samarthyam, G. and Sharma, T., 2014. Refactoring for software design smells: managing technical debt. Morgan Kaufmann. 
