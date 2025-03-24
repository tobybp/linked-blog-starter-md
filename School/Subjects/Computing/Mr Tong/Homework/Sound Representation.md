[[Computing]]
#13/10/24

### Understanding Sound Representation:

- **Real-world data** is typically analog, continuously changing over time. For example, sound is created by changes in air pressure, which make our eardrums vibrate, and our brain interprets these vibrations as sound.

---
### Digital Representation of Sound:

- **Analog Signals** are continuous, but **Digital Signals** are discrete, meaning they take specific values at intervals.
- To convert sound from analog to digital, devices such as microphones (ADC - Analog to Digital Converters) record sound by measuring its wave height (amplitude) at regular intervals (sampling). These values are then stored as binary data.

---
### Sampling Concepts:

- **Sampling Rate:** This is the frequency of sound measurements per second, measured in Hertz (Hz). A higher sampling rate gives more detailed sound but increases the file size.
- **Sample Resolution:** The number of bits used to store each sample. More bits mean better sound quality but also larger files. For example, a 16-bit sample is more accurate than an 8-bit sample.
- **File Size Calculation:** File size depends on both the sampling rate and resolution. The formula is:
    File size (bits)=sampling rate×resolution×duration (seconds)\text{File size (bits)} = \text{sampling rate} \times \text{resolution} \times \text{duration (seconds)}File size (bits)=sampling rate×resolution×duration (seconds)
    
    For stereo sound, the file size doubles, as two channels (left and right) are recorded.

---
### Nyquist Theorem:

- The theorem states that the sampling rate must be at least twice the highest frequency present in the sound to capture it accurately. This is crucial for ensuring that digital recordings faithfully replicate the original analog sound.

---
### Human Hearing Range:

- Humans can hear sounds ranging from 20 Hz to about 22 kHz, which decreases with age. CDs are sampled at 44.1 kHz because it covers the full range of human hearing.

---
### MIDI (Musical Instrument Digital Interface):

- Unlike actual recordings, **MIDI** uses synthesised sounds. Instead of recording the entire sound, MIDI sends instructions on how to recreate the sound. This reduces the data transmitted and makes it easy to modify sound characteristics like pitch and tempo.

---
### Key Advantages of MIDI:

- It reduces file size significantly because it doesn't store sound, just commands. However, since sounds are synthesized, they may not always feel as realistic as live recordings.