# flink-basic-example
Apache Flink basic Transformation by reading file content, transform to Uppercase, and write into another file.

I am trying to run Flink application on Intellij on Mac OS

$ ./gradlew clean build

It throw error: bash: ./gradlew: Permission denied

So I did

$ chmod +x gradlew 


Now running flink application from the build jar inside /build/libs/flink-basic-example-1.0.jar

$ flink run build/libs/flink-basic-example-1.0.jar --input input-path --output output-path

bash: flink: command not found

$ brew install apache-flink

$ flink --version

$ flink run build/libs/flink-jar --input file --output file
