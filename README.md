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
