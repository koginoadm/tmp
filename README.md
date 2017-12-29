```
vUri="https://storage.googleapis.com/golang/go1.9.2.linux-amd64.tar.gz"

mkdir $HOME/local && cd $_ && pwd
curl -LR ${vUri} -O
tar -C $HOME/local -xvzf $(basename ${vUri})

cat >> $HOME/.profile << '__EOD__'
# For golang
export GOROOT=$HOME/local/go
export GOPATH=$HOME/go
export PATH=$PATH:$GOROOT/bin:$GOPATH/bin
__EOD__
source $HOME/.profile



```
