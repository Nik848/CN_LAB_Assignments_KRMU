# Simulation and Comparison of RIP and OSPF Routing Protocols

## Overview

This project demonstrates the configuration, simulation, and comparison of two routing protocols:

* RIP (Routing Information Protocol)
* OSPF (Open Shortest Path First)

The simulations are created using Cisco Packet Tracer to analyze performance, convergence time, and routing efficiency across multiple networks.

---

## Project Files

* rip_simulation.pkt → Network simulation configured with RIP
* ospf_simulation.pkt → Network simulation configured with OSPF
* output.txt
* README.md

---

## Network Design

### Topology

* Multiple routers connected in a mesh or linear topology
* Each router connected to at least one LAN
* IP addressing assigned manually
* Same topology used for both RIP and OSPF to ensure fair comparison

---

## Configuration Details

### RIP Configuration

* Protocol: RIP Version 2
* Commands:

```
router rip
version 2
network <network_address>
no auto-summary
```

* Characteristics:

  * Distance vector protocol
  * Uses hop count as metric
  * Maximum hop count is 15

---

### OSPF Configuration

* Protocol: OSPF with Process ID 1
* Commands:

```
router ospf 1
network <network_address> <wildcard_mask> area 0
```

* Characteristics:

  * Link state protocol
  * Uses cost as metric based on bandwidth
  * Faster convergence

---

## Simulation Process

1. Created identical network topology in Packet Tracer
2. Configured RIP on all routers and tested connectivity
3. Saved routing tables and ping results
4. Repeated the same process using OSPF
5. Compared both protocols based on convergence time, routing updates, and efficiency

---

## Results and Observations

### RIP

* Slower convergence
* Periodic updates increase network traffic
* Limited scalability due to maximum hop count
* Easier to configure

### OSPF

* Faster convergence
* Event driven updates reduce overhead
* Supports large and complex networks
* More complex configuration

---

## Comparison Summary

| Feature     | RIP             | OSPF       |
| ----------- | --------------- | ---------- |
| Type        | Distance vector | Link state |
| Metric      | Hop count       | Cost       |
| Convergence | Slow            | Fast       |
| Scalability | Limited         | High       |
| Updates     | Periodic        | Triggered  |
| Complexity  | Easy            | Moderate   |

---

## Output Verification

Refer to output.txt for:

* Routing tables using show ip route
* Ping results between networks
* Connectivity verification

---

## Conclusion

OSPF performs better than RIP in terms of speed, scalability, and efficiency. RIP is simpler but not suitable for large or complex networks. OSPF is more appropriate for modern network environments.

---

## Tools Used

* Cisco Packet Tracer
* CLI based configuration

---

## Author

Nikhil
B.Tech CSE AIML

---
