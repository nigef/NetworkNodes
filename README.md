# NetworkNodes
Network of Mutiple Nodes


## Requirements
- Upload code updates to arduino wirelessly.
- Supports multiple, 1 - 50 (or "infinite"?) nodes on the network.
- Isolation: any nodes going "down" does not affect the rest of the network.


## Topology
- TBD: Star, or Peer-to-Peer, or Mesh
- Central monitor/hub to aggregate, and display or forward the data. Acts as a secure layer between node network and the internet.


## RF Transceiver Technology
- TBD: Bluetooth "4.0/LE/BLE" CC2540 or CC2541 (encrypted, more packet overhead, very low power), or [nRF24L01+](https://www.nordicsemi.com/eng/Products/2.4GHz-RF/nRF24L01P) module (unencrypted, less overhead, very low power 900nA with sleep mode, limited packet size 32 bit)
- Cost of BLE/nRF each: $1.00
- Both use the 2.4 Ghz band.
- Interestingly [the nRF24L01 can be used to broadcase BLE](http://hackaday.com/2013/09/21/sending-data-over-bluetooth-low-energy-with-a-cheap-nrf24l01-module/) because both use the same protocol
- Theres also the low energy [ANT™ protocol](https://www.nordicsemi.com/eng/Products/ANT)
- One obvious protocol choice is WiFi/802.11 protocol... which is relatively very high power, high bandwidth, and depends on local network uptime. (This WiFi protocol may not be the best suited choice?)
- Also note, [Noric semi](https://www.nordicsemi.com/eng/Products/Bluetooth-low-energy) makes so many different modules for: BLE, ANT, 2.4 GHZ RF, SUB 1-GHZ RF, ...

## Software Model
- Producer/Consumer model with shared buffer, and locking mechanism, (with "condition variable"?).



## TODO
- research the best protocol and choose it. Then order 10 nodes on eBay.
- find the best suited Arduino that has enough pins for the transceiver and sensors. Better to lean towards too many pins than too few. Price for each ranges from $1.00 to $1.75 on eBay.


<p align="center">
    <img src="https://github.com/nigef/NetworkNodes/blob/master/images/micro.png?raw=true" alt="pyta logo" width="500">
</p>

<p align="center">
    <img src="https://github.com/nigef/NetworkNodes/blob/master/images/nano.png?raw=true" alt="pyta logo" width="500">
</p>

<p align="center">
    <img src="https://github.com/nigef/NetworkNodes/blob/master/images/promini.png?raw=true" alt="pyta logo" width="500">
</p>

