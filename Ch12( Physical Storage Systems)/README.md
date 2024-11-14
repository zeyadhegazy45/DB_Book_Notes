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

![image_alt](https://github.com/zeyadhegazy45/DB_Book_Notes/blob/63c7883b70bfea2bee4e583a729712d41fa345ef/Ch12(%20Physical%20Storage%20Systems)/fake_disk.png)

# RAID(edundant arrays of independent disks)
- هو نظام بنستخدمه عشان نقدر نخزن الداتا بتاعتنا علي اكتر من هارد ديسك طب ايه الفكره ؟! الفكره اني لو هارد عطل يبقي عندنا استبن للداتا بتاعتنا علي ما الاول يرجع
## Improvement in Performance via Parallelism
1. **Mirroring (Duplicating Data on Multiple Disks):**

- With mirroring, data is stored on two disks, so you can read from either one.
- This doubles the read speed since both disks can handle read requests simultaneously.

2. **Striping Data Across Multiple Disks:**

1. Bit-level Striping:
- Splits each bit of a byte across different disks.
- For example, if you have 8 disks, each disk stores a different bit of the byte.
- This increases data transfer for large reads but doesn’t help much with small operations.

2. Block-level Striping:
- Splits larger blocks of data across multiple disks.
- For large files, data is read in parallel from all disks, increasing speed.
-  For small reads, only one disk is used, but the other disks are free for other tasks.
# the common RAID levels

1. **RAID 0 (Striping):**
- No redundancy, just data striping. Data is split across multiple disks, which increases performance but if one disk fails, all data is lost.

2. **RAID 1 (Mirroring):**
- Data is duplicated on two disks, so if one disk fails, the other has the exact copy. This increases reliability but is expensive since you need double the number of disks.

3. **RAID 5 (Distributed Parity):**
- Data and parity (error-correcting information) are spread across all disks. Parity is used to rebuild data in case of a disk failure, making it more efficient and reliable than RAID 0 and RAID 1.
- The parity information is distributed across all disks to avoid data loss if one disk fails. This is a common setup for cost-effective redundancy.

4. **RAID 6 (Double Parity):**
- Similar to RAID 5 but with two sets of parity blocks, allowing the system to tolerate two disk failures without data loss. It provides even higher reliability but has more overhead.

# Techniques to Improve Disk Access:

1. **Buffering:**
- Data read from the disk is temporarily stored in memory to be used later.
2. **Read-ahead:**
- Consecutive blocks are read into memory even if not immediately needed, helping speed up sequential access.
3. **Scheduling:**
- Access requests are arranged to minimize disk-arm movement. The elevator algorithm is often used to reorder requests for efficiency, similar to how elevators work.
4. **File Organization:**
- Storing blocks in a way that matches the expected access pattern can reduce access time. For example, storing blocks sequentially on the disk can help with sequential file access.
5. **Non-volatile Write Buffers:**
- To prevent data loss during a power failure, data is first written to non-volatile memory (like NVRAM or flash memory) before being transferred to disk. This speeds up writes and ensures data integrity in case of a crash.
