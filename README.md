# avail-madara

## Install Go
Make sure you installed the latest version of `Go` before you run this code. Run `go version` to verify.
```
ver="1.22.0"

wget "https://golang.org/dl/go$ver.linux-amd64.tar.gz"

sudo rm -rf /usr/local/go

sudo tar -C /usr/local -xzf "go$ver.linux-amd64.tar.gz"

rm "go$ver.linux-amd64.tar.gz"

echo "export PATH=$PATH:/usr/local/go/bin:$HOME/go/bin" >> $HOME/.bash_profile

source $HOME/.bash_profile

go version
```

## Install Screen
```
apt install screen
```

## Run The Code
* Clone the repository.
```
git clone https://github.com/Kamus-Crypto/avail-madara.git
```

* Go to `avail-madara` directory.
```
cd avail-madara
```

* Change the RPC URL. Use your own RPC URL.
```
nano rpc.json
```
Example:
```
{
    "url": "http://178.132.4.42:9944"
}
```

* Clean up and update the module's dependencies
```
go mod tidy
```

* Create new screen.
```
screen -S tx
```

* Run the code.
```
go run main.go
```
