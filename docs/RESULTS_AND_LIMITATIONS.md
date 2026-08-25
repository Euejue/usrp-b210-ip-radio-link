# Results and Limitations

## Recorded Demonstration

The controlled laboratory run produced three independent forms of evidence:

1. **Radio evidence:** the expected received waveform was visible in the spectrum display.
2. **Link evidence:** the receiver repeatedly reported successful synchronization and integrity-valid frame recovery.
3. **Application evidence:** ICMP packets and interactive TCP text crossed the bidirectional radio path.

## Observed Results

| Observation point | Transmitted | Received | Packet loss | Average RTT |
|---|---:|---:|---:|---:|
| Node A receiving the return path | 83 | 75 | 9.63855% | approximately 2.62 s |
| Node B receiving the forward path | 98 | 84 | 14.2857% | approximately 2.63 s |

The screenshots in `docs/images/` preserve the terminal, radio, and application evidence from the recorded run.

## Interpretation

The experiment demonstrates end-to-end integration, not production network performance. Packet delivery in both directions confirms that the radio, framing, host-interface, and application layers operated together. The observed delay and loss also show that successful connectivity does not imply an optimized or robust link.

## Known Limitations

- High latency and non-trivial packet loss.
- Sensitivity to synchronization, buffering, hardware scheduling, and RF conditions.
- No claim of production-grade security, reliability, or standards compliance.
- No guaranteed throughput, jitter, or service-quality result.
- Results are based on a limited controlled laboratory run.

## Future Work

- Improve burst handling and end-to-end latency.
- Add stronger error-control and recovery mechanisms.
- Measure repeatability across multiple sessions and channel conditions.
- Evaluate throughput, jitter, and longer-duration stability.
- Add security and authentication appropriate to the intended application.

