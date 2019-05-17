求助，为什么把java代码编译打包成jar包后就无法正常运行了？
```
javac HelloWorld.java 
cd ..
java java_test.HelloWorld

Hello World
```
```
cd -
jar -cvfe ./hello.jar java_test.HelloWorld ./*.class
java -jar ./hello.jar 

Error: Could not find or load main class java_test.HelloWorld
```
```
jar -cfm ./testjar.jar ./manifest.txt ./*.class
java -jar testjar.jar 

Error: Could not find or load main class java_test.HelloWorld
```
我把java_test.HelloWorld改为HelloWorld或者HelloWorld改为HelloWorld或者java_test.java_test.HelloWorld,但也还同样报错。

```
# 相关环境变量
export JAVA_HOME=/home/java/jdk1.8
export PATH=$PATH:$JAVA_HOME/bin
export CLASSPATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/li/tools.jar:$JRE_HOME/lib/rt.jar:/root/java_local_class/*
```
