# The new features in Wi-Fi 6 (2)

The challenges that we encounter in improving performance in the previous page can be resolved by enhancing **airtime efficiency**.

## Resource allocation
Wi-Fi 6 chooses to use **OFDMA** instead of OFDM of Wi-Fi 5. The difference between the two modulation schemes is the resource allocation for multi-users. You can simply think the multi-user version of OFDM is OFDMA. 
In OFDM, multiple users are separated by only space(spatial streams) and time, not by frequency. OFDMA adds a third multi-user dimension, frequency or data tone. Like in the below picture, OFDMA diagram(the right one) is also divided on the z-axis. OFDM cannot allot each channel to multi-users, whereas OFDMA is able to allot each subcarrier to different users.

![comparision](assets/images/3-1-OFDMA.png)

This feature brings many advantages to Wi-Fi 6. In a high-density environment, if there is a client who uses only a small amount of data traffic, OFDM wastes most of the bandwidth of the channel assigned to the client. But OFDMA can utilize the spare bandwidth for other clients, keeping its throughput high with many users. (The other advantage)



## Improving capacity
It is a challenge to overcome the interference in the environment sharing the same channel bandwidth in the same physical space. This happens in the mobile environment in a large place sharing APs. A client should decide which an AP it will connect among several APs, or which *Basic Service Set(BSS))* it should be in. BSS is a set of clients connected to an AP. In the situation that a client is the middle of two BSSs or APs, the client also hear the traffic from overlapping BSS(OBSS). This can cause the OBSS interference.

Wi-Fi 6 introduces BSS(Basic Service Set) Coloring. BSS coloring is the way to differentiate BSS in the same channel by BSS number(color) in the PHY header. So clients can ignore the traffic, not from connected AP. This also improves the battery life.


## Flexible low-power device scheduling
This section is not directly related to airtime efficiency, but about a power-saving mode. The prior versions of Wi-Fi has some kinds of low-power mode like Unscheduled Automatic Power Save Delivery (U-APSD). But a low-power device should wake up periodically to receive beacons generally a multiple of every 102.4 ms. This periodic listening to beacons restricts potential energy-saving.
Wi-Fi 6 introduces the new power-savings mode called **Target-Wakeup Time (TWT)**. A device or a station(STA) can schedule any length of sleeping time up to 5 years. This will help many small IoT devices to save their energy.

![TWT](assets/images/3-3-TWT.png)
