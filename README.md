# CN-Orange-PES1UG24CS214
# Static Routing using SDN (POX + Mininet)

This project demonstrates static routing using Software Defined Networking.

## Files
- static_topo.py → Defines network topology
- static_routing.py → Controller logic (flow rules)

## How to Run
1. Start POX controller:
   ```bash 
   cd ~/pox
   ./pox.py log.level --DEBUG static_routing
   ```

3. Run Mininet:
   ```bash
   sudo mn --custom static_topo.py --topo statictopo --controller=remote
   ```

5. Test:
   ```bash
   pingall
   ```

7. Check flows:
   ```bash
   sudo ovs-ofctl dump-flows s1
   ```
