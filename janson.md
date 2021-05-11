Note: only for learn
## compile and run in idea
依赖：gradle 4.6，jdk1.8

为加快编译速度，修改配置文件gradle.properties
```text
## 设置此参数主要是编译下载包会占用大量的内存，可能会内存溢出
org.gradle.jvmargs=-Xmx2048M
## 开启 Gradle 缓存
org.gradle.caching=true
## 开启并行编译
org.gradle.parallel=true
```
编译二进制包：gradlew assemble

生成idea项目文件：gradle idea，然后用idea打开导入

本地启动es，找到org.elasticsearch.bootstrap.ElasticSearch类，配置运行jvm参数
-Des.path.home=eshome -Des.path.conf=eshome/config -Dlog4j2.disable.jmx=true -Djava.security.policy=eshome/config/elasticsearch.policy





