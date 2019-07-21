# disable to ping from outside from public ip
`for that, the icmp-config would be the following:`
- echo requests get dropped, but all the other icmp types are still allowed.

-------------------------------------------------------------------------------

```bash
icmp deny any echo outside
icmp permit any outside
```

# ISP1
-----------------------------------------
```bash
ASA5550(config)# icmp deny any echo your_Outside 
ASA5550(config)# icmp permit any your_Outside 
```
---------------------------------------------

# ISP2
-------------------------------------------------
```bash
ASA5550(config)# icmp deny any echo your_-Outside 
ASA5550(config)# icmp permit any your_Outside 
```
--------------------------------------------------

# ISP3
-------------------------------------------------
```bash
ASA5550(config)# icmp deny any echo your_-Outside 
ASA5550(config)# icmp permit any your_Outside 
```
--------------------------------------------------
