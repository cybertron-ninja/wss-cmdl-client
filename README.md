# Overview
---

This code builds a websocket client, which connects to a wss server using the URL you specify on the command line.
Presently, it writes all messages it receives to standard output.  But, it will
be upgraded, so it can retransmit all received messages to a REST API endpoint to 
be parsed and processed in whatever way an application server needs.

# Dependencies
---

The following development version libraries must be installed before building the websocket client.

* CMake >= 3.13.4
* Boost
* pthread
* crypto
* ssl

To install the required libraries on Debian Buster execute the following command.

```
apt-get update -y
apt-get install -y cmake
apt-get install -y libboost-all-dev libboost-system libboost-system-dev
apt-get install -y libpthread-stubs0-dev libevent-pthreads-2.1-6
apt-get install -y libcrypto++-dev
apt-get install -y libssl-dev
```

# Build
---

To build the websocket client execute the following commands.

```
mkdir build
cd build
cmake ..
make
```

# Running the Websocket Client
---

The websocket client accepts one command line argument.  To make it easier to understand, the following
is an example, which will subscribe to all level 2 order book updates from Bitmex for the BTC/USD market.

```
wss "wss://testnet.bitmex.com/realtime?subscribe=instrument,orderBookL2_25:XBTUSD"
```

To shutdown the webosocket client press `Ctrl-C`.

# Authored By
---

* Michael Ellertson


# Disclaimer
---

The BitMEX Test Net is used by this project only to test the websocket connection.  
We do not endorse BitMEX nor are we afiliated with BitMEX in any way.  Trading
on BitMEX is prohibited in the United States and some other countries.  It is your
responsibility to verify the legality of connecting to BitMEX before using this 
tool.


