# Go Positive Word Generator Lambda
A super random Go Lang lambda function that generates a words that have a positive connotation... 


### Go Version
I'm using go version go1.13.4 darwin/amd64


### VERY IMPORTANT - Cloning This Project Properly 
This is a Go proejct, and for some strange reason GoLang is incredibly picky about where you sdcaffold you proejcts- you MUST build your Go projects within a directory that is in a folder named "src" that is located directly within your GOPATH.

You can see what your GOPATH is with this command:
```
echo $GOPATH
```

This should give you something like this following:
```
/Users/jim/go
```
Basically, it's a folder called "go" inside your home directory. Now personally, before I started using go I had my own git repo naming conventions where I would clone everything into a local repo named `~/Git-Projects`, but for go project I just clone them into `/Users/jim/go/src`. This makes my life way simpler, and you should use this strategy too. ;) 

### Running Locally
to start function locally:
first, rebuild the binaries:
```
make
```

Then invoke it with a file containing a sample payload:
```
sls invoke local -f hello --path ./fake-payload.json
```
(Note: You may need to use `sudo` to get it to work)

### Deploying
First, install aws cli and login:
```
aws configure
```

then serverless deploy:
```
sls deploy
```


### Scaffolding
This project was created with the serverless framworks' "aws-go-dep" template:
```
sls create --template aws-go-dep
```