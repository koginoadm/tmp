# Install Golang
```

apt -y install git
yum -y install git

declare vUri="https://storage.googleapis.com/golang/go1.9.2.linux-amd64.tar.gz"

mkdir -p $HOME/local
curl -LR ${vUri} -o $HOME/local/$(basename ${vUri}) && tar -C $HOME/local -xvzf $_

grep -q 'export GOROOT=$HOME/local/go' $HOME/.bash_profile || cat >> $HOME/.bash_profile << '__EOD__'
# For golang
export GOROOT=$HOME/local/go
export GOPATH=$HOME/go
export PATH=$PATH:$GOROOT/bin:$GOPATH/bin
__EOD__
source $HOME/.bash_profile

go get -u github.com/gogits/gogs








```
