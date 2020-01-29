# flink-basic-example
Apache Flink basic Transformation by reading file content, transform to Uppercase, and write into another file.

I am trying to run Flink application on Intellij on Mac OS

$ ./gradlew clean build .   

ERROR : It throw error: bash: ./gradlew: Permission denied
SOLUTION: $ chmod +x gradlew 


Now running flink application from the build jar inside /build/libs/flink-basic-example-1.0.jar

$ flink run build/libs/flink-basic-example-1.0.jar --input input-path --output output-path

ERROR:  bash: flink: command not found
SOLUTION: $ brew install apache-flink

$ flink --version

$ flink run build/libs/flink-jar --input file --output file

ERROR: Connection refused since I didn't start flink cluster
SOLUTION: 

$ cd /usr/local/Cellar/apache-flink/1.9.1/libexec

$ ./bin/./bin/start-cluster.sh 

    Starting cluster.

    Starting standalonesession daemon on host machine

    Starting taskexecutor daemon on host machine

$ flink run build/libs/flink-jar --input AbsolutePath --output AbsolutePath

    Starting execution of program

    Program execution finished

    Job with JobID dfeb977c5ab7b976c73b090cceab0717 has finished.

    Job Runtime: 237 ms

We can see on Flink Dashboard localhost:8081

![Optional Text](/image/image1.png)

![Optional Text](/image/image2.png)


