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


