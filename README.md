# Analysis-of-the-Disk-Structure-using-Sleuth-Kit
## AIM:
To analyze the disk structure of a given disk image using Sleuth Kit tools in Kali Linux.

## DESIGN STEPS:
### Step 1:
Obtain or create a disk image file (e.g., disk.dd) to analyze. Open the terminal in Kali Linux.

### Step 2:
Use Sleuth Kit tools like mmls, fsstat, and fls to examine the partition layout, file system details, and file listing.

### Step 3:
Interpret the output of the tools to understand the disk structure, including partitions, sectors, and files.

## PROGRAM:
Sleuth Kit Disk Analysis Commands

✅ Option 1: Create a Sample Disk Image (for Testing)

Let’s create a 10MB blank disk image and simulate file system activity:

```bash
cd ~/Downloads

# Step 1: Create an empty disk image
dd if=/dev/zero of=disk.dd bs=1M count=10

# Step 2: Format it with a file system (like FAT32)
mkfs.vfat disk.dd
```

## OUTPUT:
<img width="592" height="465" alt="Screenshot 2025-09-15 003621" src="https://github.com/user-attachments/assets/0f83b6b9-b593-48c2-84ec-e0995cdcd99c" />


### Create Disk

<img width="562" height="452" alt="Screenshot 2025-09-15 003629" src="https://github.com/user-attachments/assets/f2471613-d3cf-4c4c-bcbd-e44ec9518775" />


### mmls 
```bash
mmls disk.dd
```
### fls
```bash
fls -f fat -o 0 disk.dd
```
<img width="562" height="452" alt="Screenshot 2025-09-15 003629" src="https://github.com/user-attachments/assets/d0f6dc1e-ac3d-410a-94fd-ddc145b74b8a" />

<img width="558" height="450" alt="Screenshot 2025-09-15 003639" src="https://github.com/user-attachments/assets/cbf8f179-b17c-4c6d-a45a-c72c7b88e298" />

## RESULT:
The analysis was performed successfully using Sleuth Kit, and the disk structure was understood in detail.
