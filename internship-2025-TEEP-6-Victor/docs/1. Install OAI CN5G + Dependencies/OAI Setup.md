## Step 1: OpenAirInterface (OAI) Preview
OAI is an open-source 4G/5G implementation, and to do an end-to-end (E2E) test, some setups to do:
- gNB (5G base station) or eNB (4G LTE base station)
- Core Network (5GC or EPC)
- User Equipment (UE)

Hardware Requirements
- A Linux machine (Ubuntu 20.04 recommended)

Software Requirements
- Ubuntu 20.04 (recommended)
- Docker
- OAI dependencies (GCC, CMake, Python, etc.)

## Step 2: Setup Ubuntu Environment
**Update system** 
```
sudo apt update && sudo apt upgrade -y
sudo apt install -y git cmake build-essential python3 python3-pip
```

**Clone OAI Repository**
```
git clone https://gitlab.eurecom.fr/oai/openairinterface5g.git
cd openairinterface5g
git checkout develop
```

**Install OAI Dependencies**
```
cd cmake_targets
./build_oai -I
```
