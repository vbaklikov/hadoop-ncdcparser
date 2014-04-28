hadoop-ncdcparser
=================

NCDC dataset MapReduce parser with Secondary Sort on key+value

We set the partitioner to partition by the first field of the key (the year) using a custom partitioner called FirstPartitioner. To sort keys by year (ascending) and temperature (descending), we use a custom sort comparator, using setSortComparatorClass(), that extracts the fields and performs the appropriate comparisons. Similarly, to group keys by year, we set a custom comparator, using setGroupingComparatorClass(), to extract the first field of the key for comparison.[
