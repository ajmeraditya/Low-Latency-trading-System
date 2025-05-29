# Low-Latency-Trading-System

A complete C++ implementation of a low-latency electronic trading exchange, built following **Building Low Latency Applications with C++** by Sourav Ghosh.

## Features

- In-memory limit-order book and matching engine with price/time priority  
- Cache-aware data structures and memory alignment  
- Custom fixed-size memory pools to eliminate runtime heap allocations  
- Lock-free SPSC ring buffers for inter-thread messaging  
- CPU affinity and NUMA-aware allocations for deterministic latency  
- Lightweight `rdtsc`-based profiling macros for cycle-accurate measurement  
- Custom TCP/UDP socket layer with compact binary protocol

## How to run

- **build.sh**  
  Configures and performs full Release & Debug builds (clean + all targets) via CMake + Ninja

- **run_clients.sh**  
  Starts multiple `trading_main` client processes (MAKER/TAKER/RANDOM) to generate order traffic against a running exchange

- **run_exchange_and_clients.sh**  
  Orchestrates end-to-end workflow: builds and launches the exchange, waits, runs clients, then cleanly shuts down


## References

- **Building Low Latency Applications with C++** by Sourav Ghosh (Packt Publishing): [Packt Product Page](https://www.packtpub.com/en-cl/product/building-low-latency-applications-with-c-9781837639359?type=print) :contentReference[oaicite:0]{index=0}  

