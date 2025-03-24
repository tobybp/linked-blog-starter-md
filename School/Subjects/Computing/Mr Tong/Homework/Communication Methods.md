[[Computing]]
#13/3/25 
## Serial vs. Parallel Data Transmission

### Serial Data Transmission

- Bits are sent one after another along a single data line.
- Requires only one wire for transmission in one direction.
- For two-way communication, two data lines are needed, plus a common ground wire.
- Example: USB (Universal Serial Bus)
- Advantages:
    - More reliable over long distances.
    - Less interference compared to parallel transmission.
    - Higher frequencies possible.
    - Uses smaller and cheaper connectors (e.g., USB).

### Parallel Data Transmission

- Multiple bits (e.g., 1 byte = 8 bits) are sent simultaneously over multiple lines.
- Requires one wire per bit plus additional control lines.
- Example: Internal computer components use parallel buses.
- Advantages:
    - Faster than serial transmission over short distances.
### Problems with Parallel Transmission

- Skew:
    - Bits arrive at different times due to slight differences in wire properties.
    - Causes timing errors as data bits don’t align correctly.
- Crosstalk:
    - Electromagnetic interference between adjacent wires.
    - Becomes worse as speed (frequency) increases.
    - Corrupts data, requiring retransmission.
- Limitation:
    - Can only be used reliably over short distances (typically < 2m).
    - Serial transmission is preferred for long distances.

## Synchronous vs. Asynchronous Transmission

### Synchronous Transmission

- Data is transmitted in continuous blocks with no gaps.
- Clock pulses synchronize transmission between sender and receiver.
- The receiver counts the bits and reconstructs bytes.
- Efficient for high-speed communication.

### Asynchronous Transmission
- Each byte is sent separately, as soon as it is available.
- No need to wait for a clock signal.
- Each byte includes:
    - Start bit (indicates the beginning of a byte).
    - Stop bit (indicates the end of a byte).
    - Parity bit (optional error checking).
- Slower than synchronous transmission due to extra bits.
- Cheap and effective for low-speed communication (e.g., keyboard, mouse).

## Parity Bit and Error Checking
- A parity bit is used for error detection.
- Odd or even parity ensures that the total number of `1`s is always odd or even.
- Helps detect single-bit errors, but not multiple-bit errors.
## Key Communication Terms

### Baud Rate vs. Bit Rate
- Baud Rate: The number of signal changes per second in a transmission channel.
- Bit Rate: The number of bits transmitted per second (bps).
- Formula: Bit Rate=Baud Rate×Number of Bits per Signal\text{Bit Rate} = \text{Baud Rate} \times \text{Number of Bits per Signal}Bit Rate=Baud Rate×Number of Bits per Signal
- Baseband Transmission:
    - Each signal change represents 1 bit.
    - Bit Rate = Baud Rate.
- Broadband Transmission:
    - Each signal change carries multiple bits.
    - Bit Rate > Baud Rate.
    - Example: If each signal represents 2 bits, then Bit Rate=2×Baud Rate\text{Bit Rate} = 2 \times \text{Baud Rate}Bit Rate=2×Baud Rate
### Bandwidth and Data Transfer Rate
- Bandwidth: Maximum capacity of a communication channel.
- Measured in: bps (bits per second), Mbps (megabits per second), Gbps (gigabits per second).
- Higher bandwidth = Higher potential bit rate.
- Example bandwidth needs:
    - Instant Messaging: ~1,000bps
    - HD Video Streaming: ~4Mbps
    - Digital TV (Multiple Channels): ~19Mbps
### Latency
- Time delay between sending and receiving data.
- Example: News broadcasts where a reporter takes time to respond due to satellite delay.
- Geostationary satellites orbit 22,300 miles above Earth, introducing significant latency.
### Protocol

- A set of rules that devices follow for communication.
- Ensures different manufacturers’ devices can work together.
- Defines:
    - Physical connections and cabling.
    - Transmission rates (baud rate, bit rate).
    - Data format.
    - Error checking mechanisms (e.g., parity bits).
    - Synchronous or asynchronous transmission methods.

---

## Recap of Key Terms

|Term|Definition|
|---|---|
|Latency|Time delay between sending and receiving data.|
|Protocol|Set of rules for communication between devices.|
|Baud Rate|The number of signal changes per second in a channel.|
|Bit Rate|The number of bits transmitted per second (bps).|
|Bandwidth|Maximum data transfer capacity of a channel.|
