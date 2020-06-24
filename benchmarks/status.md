|bm | updated | jdk 8 | jdk 11 | clean | scratch | validation | small | default | large | huge | latency |
|-|-|-|-|-|-|-|-|-|-|-|-|
|avrora|✓|✓|✓|✓|✓|✓|✓|✓|✓|||
|batik|✓|✓|✓|✓|✓|✓|✓|✓|✓|✓||
|biojava|✓|✓|✓|✓|✓|✓|✓|✓|✓|✓||
|cassandra|✓|✓|✓|✓|✓|✓|✓|✓|✓|?|?|
|eclipse|✓|✓|✓|✓|✓|✓|✓|✓|✓|||
|fop|✓|✓|✓|✓|✓|✓|✓|✓||||
|graphchi|✓|✓|✓|✓|✓|✓|✓|✓|✓|✓||


### TODO
* Data is read only
  * check that benchmarks never write to dat director
* Packaging
  * Checksum all jars and data (not just huge)
  * Consider packaging everything aside from huge as a zip
  * have all within a folder of the same root name as the jar
  * have them all copied into place as part of the ant build
  * create a single dacapo zip that contains the jar, the dat and jar folders
* Biojava: why do we not see any parallelism? [maybe this](https://bugs.openjdk.java.net/browse/JDK-8247980)
* Cassandra: further calibration required.   Not clear that workload configs are affecting heap size.
* Eclipse
  * Check that build is not happening in DATA