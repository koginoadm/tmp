```
vUri="https://storage.googleapis.com/golang/go1.9.2.linux-amd64.tar.gz"

mkdir $HOME/local && cd $_
curl -LR ${vUri} -O
tar -C $HOME/local -xvzf "$(basename "${vUri}")"




```
