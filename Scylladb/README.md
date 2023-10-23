# Scylladb Docker image

### To build image

```
docker build -t my-scylla-image .
```

### This image comes with authenticator enable by default
``` 
username : cassandra
password : cassandra
```

###  To presit data , we have to create volume

```
docker volume create scylladb_data

```

### To run the container

```
docker run -d --name my-scylla-container -p 9042:9042 -p 19042:19042 -v scylladb_data:/var/lib/scylla my-scylla-image
```

### Exposed Port
```
9042
19042
```

