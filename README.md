### Requirements 
1. Java 11+


### Build 
```
mvn clean package
```

### Execute with DDB client 

```
java -jar target/try-dax-1.0-SNAPSHOT.jar
```

### Find the DAX cluster endpoint 

```
aws dax describe-clusters --query "Clusters[*].ClusterDiscoveryEndpoint"
```

### Run with DAX 

```
java -jar target/try-dax-1.0-SNAPSHOT.jar dax://my-cluster.l6fzcv.dax-clusters.us-east-1.amazonaws.com

```

or use `daxs://` scheme if using a secure endpoint 

```
java -jar target/try-dax-1.0-SNAPSHOT.jar daxs://my-cluster-dax.vbw29g.dax-clusters.us-east-1.amazonaws.com
```

### Reference

Please refer to https://docs.aws.amazon.com/amazondynamodb/latest/developerguide/DAX.client.run-application-java.html for help on TryDax application.