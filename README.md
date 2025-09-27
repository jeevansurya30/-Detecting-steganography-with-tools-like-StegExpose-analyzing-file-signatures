# Detecting-steganography-with-tools-like-StegExpose-analyzing-file-signatures
## AIM:
To detect hidden data using steganography detection tools like StegExpose and analyze file signatures for authenticity and manipulation.
## Requirements:
- **Operating System:** Linux / Windows
- **Tools:**
    - StegExpose (Java-based tool)
    - Hex Editor (e.g., xxd, HxD)
    - File command (Linux) or TrID (Windows)
- **Sample files:**
    - Suspected stego files (.jpg, .png, .wav)
    - Clean reference files
## ARCHITECTURE DIAGRAM:
```mermaid
flowchart TD
    A[Input File: JPG/PNG/WAV] --> B[File Signature Analysis]
    B --> C{Signature Match?}
    C -- Yes --> D[Pass to StegExpose]
    C -- No --> E[File Tampered / Mismatch]
    D --> F[StegExpose Detection: Suspicious or Clean]
    F --> G[Report Findings]
```

## DESIGN STEPS:
### Step 1:
Install StegExpose or use the JAR version to detect steganography in image files.

### Step 2:
Run StegExpose on a directory of suspected image files using the command:

### Step 3:
Analyze file signatures using tools like file, binwalk, or xxd to check for inconsistencies or embedded content.

## PROGRAM:
**Check file type**
```bash
file suspect.jpg
```
or view magic bytes:
```
xxd suspect.jpg | head
```
**Run StegExpose**
```bash
java -jar StegExpose.jar suspect.jpg
```
## OUTPUT:
List of Images with Steganography Detection Scores and File Signature Details

<img width="598" height="107" alt="Screenshot 2025-09-27 143527" src="https://github.com/user-attachments/assets/074b407e-69e4-4a40-b4ae-2c09a12dc16a" />
<img width="774" height="63" alt="Screenshot 2025-09-27 143534" src="https://github.com/user-attachments/assets/e9d3b591-3194-47e9-8ec2-8f921beee360" />

<img width="789" height="98" alt="Screenshot 2025-09-27 143540" src="https://github.com/user-attachments/assets/c2777eb7-e412-4625-a152-e7969812355e" />
<img width="779" height="91" alt="Screenshot 2025-09-27 143550" src="https://github.com/user-attachments/assets/4f1194af-66e6-4ebb-b5d2-7593a34a9049" />
<img width="808" height="81" alt="Screenshot 2025-09-27 143556" src="https://github.com/user-attachments/assets/0c0253ca-82de-477c-bd65-eace9852e9ba" />






## RESULT:
Hidden data was successfully detected and file signatures were analyzed for irregularities.
