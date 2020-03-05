# BRIG_java12

Recompiled BRIG jar compatible with Java SE version 12

This repository contains an updated jar file for BRIG (BLAST Ring Image Generator), since original version of the program has not been updated for several years, and may not run on modern Java versions.


## Do I need this?

If you get an error "Comparison method violates its general contract!" while parsing BLAST results, download updated BRIG.jar and replace the original file.
Please note, that you still need all the files from [BRIG v.0.95 distribution](https://sourceforge.net/projects/brig/).


## What is different?

Original implementation of BlastComparator class was changed to conform [Java contract to compare](https://docs.oracle.com/javase/8/docs/api/java/util/Comparator.html).

In addition, type casting was added to some lists.

There is no guarantee that the updated version will produce absolutely the same output as the original version. 




## Alternative solution

Start original version of BRIG with additional parameter:

> java -Djava.util.Arrays.useLegacyMergeSort=true -jar BRIG.jar

