## hello-world-env

A docker image for learning and testing with web apps and environment variables.

```
prodriguezmira/hello-world-env
```

### Using with local docker

```
docker run --publish=3000:3000 --rm prodriguezmira/hello-world-env
```

```
GET http://localhost:3000/
```

Prints

```
Hello, world!
Version: 1.0.0
Hostname: 14beaf9a39df
MESSAGE:
```

### Using with environment variables

```
docker run -p "3000:3000" -e "MESSAGE=container version 1"  -d prodriguezmira/hello-world-env:1.0.0
```

```
GET http://localhost:3000
```

Prints

```
Hello, world!
Version: 1.0.0
Hostname: 14beaf9a39df
MESSAGE:container version 1!
```

Thanks @widemeshio
