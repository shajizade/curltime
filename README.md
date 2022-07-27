# curltime
A Bash script for observe all timings in a curl request

## Installation
Donwload `curltime` file and put it in somewhere included in your `PATH` (like `/usr/local/bin`). You May use this:
```
sudo curl https://raw.githubusercontent.com/shajizade/curltime/main/curltime | sudo tee /usr/local/bin/curltime
sudo chmod +x /usr/local/bin/curltime
```

## Usage
Use it just like curl. You can type `curltime` instead of `curl` in any curl command, and it will show you the timing. 

Here is a sample:

```
> curltime https://google.com

start:     0
        -> dns request
        <- dns response
namelookup:  0.004225s
        -> SYN to WebServer
        <- SYN/ACK
connect:  0.004814s
        -> "Hello"
        -> SSL Handshake
        <- SSL Handshake
appconnect:  0.000000s
        Client sets SSL Params and starts requesting
pretransfer:  0.004855s
        Any Redirectredirect:  0.000000s
        -> HTTP Requets
        Creating Response on Server
        <- First Bit of Response Arrives
starttransfer:  0.005638s
        <- All Response
total:  0.005654s
```
