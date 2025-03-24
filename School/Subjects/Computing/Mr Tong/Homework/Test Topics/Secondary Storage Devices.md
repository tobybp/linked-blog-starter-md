[[Computing]]
#3/3/25
## Primary and Secondary Storage
- Primary storage is volatile, meaning that it loses the data when power is lost.
- Secondary storage is non-volatile storage
- For example:
	- Solid state devices that use flash memory
	- Magnetic storage e.g. hard disk
	- Optical storage that uses lasers, such as CD-ROM
## Secondary Storage Devices
- There are many different technologies that have evolved for storing data
- Each have their own disadvantages and advantages in terms of:
	- Durability
	- Read/write speed
	- Capacity
	- Portability
	- Cost
## Inside a Hard-disk
### Tracks, Sectors and Platters
- Concentric tracks are created on a magnetic disk
- Disk spins at 3,600 - 7,200 RPM
- Spinning platters are read by drive heads
## Magnetic Storage Devices
- Use a positive or negative polarity of magnetic particles to represent a binary pattern on the disk.
	- Changes from positive to negative (or the other way around) create electromagnetic pulses
	- Each pulse/change is read as a 1, anything else is a 0
## Development of HDDs
- As there are more technological changes, we are fitting more data into the same physical space.
	- More closely packed platters
	- Smaller parts and read/write heads
	- switching to perpendicular recording, as this saves space.
## Disk Latency
- Time taken to read/write disk data
- Includes:
	- Seek delay, time the head takes to move across the disk
	- Rotational delay, time the disk takes to more to the correct sector underneath the read/write head
	- Transfer time to move the data
## CDs
- CDs work on similar principles
- A higher power laser "burns" pits into the CD's surface
	- A low powered laser detects the reflection from pits and lands
	- Only a pit end, or a pit start deflects the laser light. to be read as a binary 1
	![[Pasted image 20250305063959.png]]
## Optical Disk Formats
- Optical disks are available as:
	- Re-writeable
	- Recordable
	- Read only
- Each format uses different techniques to achieve a difference between a "pit" and a "land"
	- Recordable use a transparent dye that becomes opaque when heated with a laser
	- Re-writeable use a laser to change the state of a phase change allow and a magnet to set the new state.
## CDs, DVDs, BluRay
- Different laser wavelengths burn smaller pits
- Therefore using blue light, BluRay can have more data in the same space.
## NAND Flash Memory Cells
- Flash memory contains no moving parts at all
- Floating gate transistors store a charge, charge is retained without power
![[Pasted image 20250305094557.png]]
## Combining Flash Memory Cells
- Cells are combined in blocks
	- An electron in the middle layer reads as a 0, outside is a 1
	- Data is read, deleted or written in blocks
	- Data can't be overwritten without being erased first
## Inside SSDs
- An SSD comprises millions of NAND flash memory cells
- Cells are managed by a controller that organises the blocks and pages of memory
	- These are arranged as an array of chips on a circuit board
## Solid State Disks
- Faster access speed as no moving parts
- Lower power consumption
	- Extended battery life
	- Devices stay cool
- Less susceptible to damage
- Silent in operation
- Lighter
## Capacity and Access Speed
- The development of solid state media is moving rapidly and has generally replaces hard drives.

| Media            | Capacity    | Access Speed |
| ---------------- | ----------- | ------------ |
| Hard disk        | 512GB - 4TB | Fast         |
| CD-ROM           | 650 - 700MB | Medium       |
| DVD              | 4.7 - 9.4GB | Medium       |
| BluRay Disk      | 25 - 50GB   | Medium       |
| Solid State Disk | 4GB - 16TB  | Very fast    |
## Software Mailing
- Often optical disks are used
	- Cheap to manufacture and distribute
	- Robust during carriage
	- Lightweight
## Company Server Data
- Hard disks usually used
	- High capacity
	- Fast read and write speeds
	- Relatively cheap per TB