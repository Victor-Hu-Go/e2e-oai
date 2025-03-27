## Install iPerf3
```
sudo apt install -y iperf3
```

## Throughput Test
While nrUE, gNB, and CN5G is running, open another terminal and run
```
iperf3 -s
```
This will run a server on the CN5G

To do the throughput test, you need the IP of the OAI-CN5G, run
```
ip addr show
```
It will show alot of IP. Search for the "oai-cn5g" labeled and there will be "inet (OAI-CN5G IP)"
The OAI-CN5G IP will be the IP you use for the test

To run the test,
```
iperf3 -c 192.168.70.129 -p 5201 -t 30 -i 1
```
This will increment every 1 second for total 30 seconds and give the results on the end
