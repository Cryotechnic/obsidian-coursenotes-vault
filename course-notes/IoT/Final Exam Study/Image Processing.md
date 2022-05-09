# Image Processing in IoT
- Set of computational techniques for analyzing, enhancing, compressing and reconstructing images

## Image Processing Steps
1. Acquire image with optical or digital scanner
2. Analyze image
3. Output modified/processed image based on analysis results

### Purpose of Image Processing
- Visualization: Observing objects that are not normally visible
- Image sharpening & restoration: Create better image
- Image retrieval: Seek image of interest
- Measurement of patter: Measuring of various objects in image
- Pattern recognition: Distinguish objects in image

When AI is used, typically can be applied to Pattern Recognition process

## AI & IoT
AI related services typically follow the following:
1. Create
2. Communicate
3. Aggregate
4. Analyze
5. Act

- IoT deals with devices interacting vs AI make the devices learn from data & experience
- IoT provides data vs AI acquiring the power to unlock responses, adding creativity and context to drive smart(er) actions
- AI-enabled IoT creates intelligent machines simulating smart behavior with little to 0 human interference (e.g. Facial recognition in IoT-based Customer Behaviour System)

## Barcode
- Visual pattern of numbers & parallel lines of variable width readable by machine
- Used to recognize specific product which procures data requirements in any given system
- Accurate, fast, reliable
- Replaced manual entry

### Barcode Types
#### 1-D (Lienar) Barcode
- Most common
- Data storage is more limited (stretched horizontally if more data required)
- Allows for item identification and tracking throughout a supply chain

***GS1*** framework which implements 1D Barcodes and represents companies all part of supply chain
GS1 EPCGlobal use RFID 

- Universal Product Code (UPC-A): 12 digits
- European Article Number / International Article Number (EAN-13): 13 digits, superset UPC
- Data Carrier (GS1-128): Encodes data + provides methods of defining data (Application Identifiers) 
#### 2-D Barcode
- More complex
	- Data stored vertically & horizontally
		- More information in less space
- Quick Response (QR) Code: Most common
- Data Matrix
- Aztec
- PDF417
- Maxicode

### Barcode Scanner Types
- Barcode requires specific type of scanner to scan the code
	- Laser Scanner
	- Charge Coupled Device (CCD)
	- 2D Camera (Imager)

## Object Detection
- Computer vision technique for locating instances of objects in images / videos
- Typically levarges ML or DL for meaningful results
	- Can predict location + class (type) of object

## Graphics Processing Unit (GPU)
- One of the most important type of computing technology
- Designed for parallel processing, used a lot for AI
- Used in HPC (High Powered Computing), DL, ML, etc.

### CPU vs GPU
| Central Processing Unit (CPU) | Graphics Processing Unit (GPU) |
| ----------------------------- | ------------------------------ |
| Several Cores                 | Many cores                     |
| Low Latency                   | High throughput                |
| Good for serial processing    | Good for parallel processing   | 

### GPU & IoT
- Jetson Nano, delivers power of modern AI in small SoC package (Maxwell + 128 cores)
