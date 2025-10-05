[[Computing]]
#20/10/24
## Data Transfer and Storage
- Data is always moving around computer systems and networks.
	- Transfer usually happens at high speeds and is accurate.
	- As the distances get longer, then the transfer becomes slower and more susceptible to interference.
	- Storage space can also be limited.
## Reducing Data Requirements
- Text, image and sound data can be greatly reduced in size using compression.
- By reducing the amount of data that is being sent:
	- The data will be sent faster
	- Less bandwidth is used.
	- Buffering is less likely to occur when streaming video or audio.
	- Less storage is occupied by the data.
## Compressing Data
- There are two different ways of compressions data.
	- Either using lossy compression, where non-essential data is permanently removed, e.g different shades of the same colour within an image, or the frequencies of sound that the human ear cannot hear due to being out of range.
	- Or using lossless, finds patterns within the data and they are summarised ina. shorter format without permanently removing any information.
## Lossy Compression - JPG
- Removes data permanently to reduce file size
- Tries to reconstruct an image without the missing data.
## Lossy Compression - MP3
- Lossy compression removes the sounds in the frequency ranges that are not so easy to hear or that least affect the perceived playback quality.
- Quieter notes played at the same time as louder notes are also removed.
## Lossless Compression
- Lossless compression works by recording patterns in the data rather than the data itself.
	- Using these patterns, a new file can be replicated without any loss of data or information.
	- There is less of a reduction in file size when using lossless, compared to lossy.
	- Lossless is used in situations where data simply cannot be lost, such as code.
## Run Length Encoding (RLE)
- A basic method of compression that summarises consecutive patterns of the same data.
- Works well with image and sound data where data could be repeated many times.
## RLE of Sound
- A sound recording could have many thousands of samples taken every second (usually 44,000)
## Dictionary Compression
- Spots regularly occurring data and stores it separately in a dictionary
## Encryption
- Encryption is a way of making sure that data cannot be understood if you don't possess the means to decrypt it.
## Caeser Cipher
- A Caeser cipher is the most common and basic type of encryption, and the least secure.
- Letters of the alphabet are shifted by a consistent amount.
## Brute Force Attack
- A brute force attack attempts to apply every possible key to decrypt the ciphertext until one works.
## Frequency Analysis
- Letters within the alphabet are not used equally as often as each other.
- In English, E is the most common letter, with T, A, O, I, N, S, R, and H following