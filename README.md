# helloworld-go-docker-k8s



##Prerequisites

Homebrew
```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

go
```
brew install go
```

godep
```
brew install dep
```

docker
```
brew install docker
```

docker-compose
```
brew install docker-compose
```

docker-machine
```
brew install docker-machine
```

VirtualBox
```
brew cask install virtualbox
```

Run env command
```
eval $(docker-machine env default)
```

A bit of trickiness - you have to open the virtualbox config, navigate to "network" and add a forwarding rule for your default docker image.

Build the docker image:

```
docker build -t helloworld .
```

Run the thing with port exposed (this really should be dynamic not hard at 3000):

```
docker run -p 3000:3000 helloworld
```
