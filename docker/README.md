# Docker environment for training

This docker image is an Ubunty 'trusty' server that has java, groovy, maven, git, and all the other
things you'll need for this class

## building it (when developing the class)

cd to this directory and

```

docker build -t diceunc/jargontrain:latest .

```

Push it to that schemaLocation

## running it (in the class)

```

docker pull diceunc/jargontrain:latest

docker run diceunc/jargontrain:latest

```

That puts you at the # prompt ready to go. You can build jargon with maven and run the
class examples using the Groovy REPL to run java code! 
