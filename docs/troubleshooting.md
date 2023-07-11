# Troubleshooting FormationFlight

## General Troubleshooting

Many things in FormationFlight can be diagnosed through its HTTP JSON endpoints. To use these, first [connect to the WiFi Network](/wifi/) and follow the specific instructions below.

### How do I know if my Flight Controller & FormationFlight are connected?

Visit the [System Status](/wifi/#_1) endpoint via WiFi and look for the `host` parameter. It'll display `INAV`, `ARDU`, or `BTFL` when a supported flight controller software is connected, or `NoFC` if none are connected.

If `NoFC` is displayed, and your FormationFlight radio is wired to your flight controller, make sure that the RX & TX wires are crossed over, and that the port is set as MSP on your flight controller software. You can follow the more specific flight controller setup pages on the left for more information on port setup.

### My FC & FF are connected, but I can't see my friends

First, verify that your friends are being heard by your FormationFlight system. Visit the [PeerManager status page](/wifi/#peermanagerstatus) and look for the peer count. If it's greater than `0`, FormationFlight is receiving your friends' positions, and you should follow the flight controller setup documents on the left.

### FormationFlight sees 0 peers active, but I have other peers running nearby

First, verify that everyone is using the same band. A 433MHz FormationFlight setup can't talk to a 2.4GHz FormationFlight setup. 

We can use the [RadioManager status page](/wifi/#radiomanagerstatus) to tell us more about what's going on with your FormationFlight system.

If the `TX` counters are going up when you refresh the page, that means the FF system is successfully transmitting information to your peers.

If the `RX` counter is going up, that means the FF system has received a packet from a peer and decoded it successfully.

The other 3 counters, `CRC/SIZE/VAL` are all failure counters.

If `CRC` is counting up, it's likely you have a `GROUPKEY` mismatch, and should work with your flying buddies to all match up.

If `SIZE` is counting up, you're receiving packets from a different system than FormationFlight. In small numbers this isn't a problem, but can be an indicator that the FF system may not work so well if the counter is rising quickly.

If `VAL` is counting up, something about the information you're receiving from peers is invalid. In small numbers this isn't indicative of a problem, but counting up quickly can indicate a problem. 


