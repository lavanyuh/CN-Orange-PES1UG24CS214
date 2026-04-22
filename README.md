# CN-Orange-PES1UG24CS214
# Static Routing using SDN (POX + Mininet)

This project demonstrates static routing using Software Defined Networking.

## Files
- static_topo.py → Defines network topology
- static_routing.py → Controller logic (flow rules)

## How to Run
1. Start POX controller:
   cd ~/pox
   ./pox.py log.level --DEBUG static_routing

2. Run Mininet:
   sudo mn --custom static_topo.py --topo statictopo --controller=remote

3. Test:
   pingall

4. Check flows:
   sudo ovs-ofctl dump-flows s1
