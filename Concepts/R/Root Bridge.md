- Every other switch picks one **root port**, its lowest-cost path back to the root bridge, based on cumulative path cost (faster links = lower cost).
- Each segment elects one **designated port** (the one forwarding toward the root for that segment).
- Any remaining ports get **blocked** to break the loop.

Switch that [[STP]] uses at the top of layer 2 