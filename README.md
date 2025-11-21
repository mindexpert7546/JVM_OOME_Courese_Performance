## Find Out which methods are being compiled in our applications - 

e.g - 
```
java -XX:+PrintCompilation main.Main 10
```

## The C1 and C2 Compilers and logging the compilation activity
eg. - 
```
java -XX:+UnlockDiagnosticVMOptions -XX:+LogCompilation main.Main 10
```

## Tuning the Code Cache 
e.g- 
```
java -XX:+PrintCodeCache main.Main 10
```
To set the code cache -

```
java -XX:ReservedCodeCacheSize=28m -XX:+PrintCodeCache main.Main 10
```

## JVM Versions 
#### 32 bit - 
1. Might be faster if heap <3GB
2. Max heap size = 4GB
3. Client compiler only (C1)

#### 64 bit 
1. Might be faster if using long/double
2. Necessary if heap > 4GB
3. Max heap size - OS dependent
4. Client & Server compilers (C1 & C2 )

#### JVM Compilers flags 
```
-client 
-server
-d64

-XX:-TieredCompilation
```

## JVM Tuning 
```
-XX:+PrintStringTableStatistics
-XX:StringTableSize=n

-XX:MaxHeapSize=n 
-XX:InitialHeapSize=n

-XX:+UnlockDiagnosticVMOptions
-XX:+PrintFlagsFinal

```
for MaxH

## Monitoring the Garbage Collectors 
```
-verbose:gc
```

## Memory size set e.g 
```
-Xms2g
-Xmx2g
-XX:+UseG1GC
-XX:G1HeapRegionSize=4m
-XX:+UnlockExperimentalVMOptions
```

## Tuning Garbage Collection 
```
-XX:NewRatio=n
-XX:SurvivorRation=n
-XX:MaxTenuringThreshold=n
```

## Choosing a Garbage Collector

Types
1. Serial = -XX:+UseSerialGC
2. Parallel = -XX:+UseParallelGC
3. Mostly COncurrent = -XX:+UseConcMarkSweepGC
                       -XX:+UseG1GC

Other Tuning GI
```
-XX:+UseG1GC

or

-XX:ConcGCThreads=n

or

-XX:InitiatingHeapOccupancyPercent=n
```

## String De-duplication  (Only available if using GI)
```
-XX:UseStringDeDuplication
```


