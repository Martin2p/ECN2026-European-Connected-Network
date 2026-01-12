# Cable Validation & Stress Test

## Test Date
2026-01-11

## Cable Details
- Type: Self-crimped Ethernet cable
- Category: Cat5e
- Length: ~15 m
- Construction: flat / unshielded

## Test Environment
- Switch: TP-Link Omada SG3210X-M2 (Managed L2+)
- Link Speed: 1 GbE / 2.5 GbE
- Duplex: Full
- Test Tool: iperf3

## Tests Performed

### TCP Multistream Test
Command:
iperf3 -c <target-ip> -t 300 -P 8

Result:
- Peak throughput: ~941 Mbit/s
- CRC errors: 0
- RX/TX errors: 0

### UDP Throughput Test
Command:
iperf3 -c <target-ip> -u -b 1G -t 60

Result:
- Sustained throughput: ~949 Mbit/s
- Packet loss: 0%
- Jitter: negligible (<1 ms)
- CRC errors: 0
- RX/TX errors: 0

## Observations
- Stable performance at 1 GbE under sustained load
- No CRC, RX or TX errors observed during active cable movement
- Physical connectors and crimps remained stable under mechanical stress

## Conclusion
Cable construction impacts high-speed Ethernet stability.
Round, shielded cables recommended for ≥2.5 GbE.
