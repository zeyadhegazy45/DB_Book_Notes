# classifiaction of Storage Media based on :
- the speed with which data can be accessed
- the cost per unit
- reliability
# Types of Storage Media:
1. **Cache:**
- Fastest and most expensive storage.
- Managed by the computer's hardware, not the database.
- Database designers consider cache effects in system design.
  
2. **Main Memory (RAM):**
- Operates directly with general-purpose instructions.
- Limited storage can be volatile (data lost on power failure).
- Suitable for enterprise databases but not large databases.

3. **Flash Memory:**
- Non-volatile (data retained without power).
- Cheaper than main memory but costlier than magnetic disks.
- Used in devices like USB flash drives, cameras, phones, and SSDs.

4. **Magnetic Disk Storage (HDD):**
- Main medium for long-term, online storage.
- Non-volatile, survives power failures but has slower access rates than SSDs.
- Cost-effective with high capacities, e.g.: 1TB at $50 (2018 prices).

5. **Optical Storage (DVD/Blu-ray):**
- Data stored and read with lasers.
- Suitable for storing digital data backups, not for active databases.
- Types include read-only, write-once (WORM), and rewritable disks.

6. **Tape Storage:**
- Primarily for backup and long-term archival data storage.
- Sequential-access storage, slower than direct-access storage (e.g., HDD/SSD).
- High-capacity and cost-effective for large, archival data
  

# Storage Hierarchy:
- Primary Storage: Fast and costly (cache and main memory).
- Secondary Storage: Online storage (flash memory and magnetic disks).
- Tertiary Storage: Offline storage (tape and optical storage).
  
- ![image_alt](https://github.com/zeyadhegazy45/DB_Book_Notes/blob/d00527cbf9760c088bbd29e3e1d6d76470516fc2/Ch12(%20Physical%20Storage%20Systems)/storage.png)

  
# some notes 
- Random Access: Direct access to any data location; fast for scattered data.(volatile)
- Sequential Access: Data accessed in order; slower for distant data, but efficient for reading large blocks in sequence (not volatile)
  
- The main measures of the qualities of a disk are capacity, access time, data-transfer rate, and reliability

- **Access Time:**

- Definition: The total time needed for a storage device to locate and transfer data to/from memory.
- **Components:**
- Seek Time: The time for the read/write head to move to the correct track.
- Rotational Latency: The time waiting for the desired sector of the disk to rotate under the read/write head. On average, rotational latency is half the time it takes for a full disk rotation.
- Transfer Time: The time required to actually transfer the data once the read/write head is in the correct position
