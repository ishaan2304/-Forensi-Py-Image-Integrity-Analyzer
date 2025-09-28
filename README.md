# Forensi-Py: Image Integrity Analyzer

## Project Overview

**Forensi-Py: Image Integrity Analyzer** is a mini-project developed for a Computer Science and Digital Forensics (CSDF) course, focusing on the critical task of verifying the authenticity and detecting manipulation in digital images.

In an era where digital content can be easily altered, establishing the integrity of an image is paramount for forensic investigations, journalism, legal proceedings, and various other fields. This tool provides a foundational, Python-based framework to analyze image files through several key forensic techniques.

It aims to identify traces of tampering by examining metadata, file integrity, and compression artifacts, thereby offering insights into an image's history and potential alterations. Forensi-Py serves as a practical demonstration of how digital forensics principles can be applied to image analysis, making it an ideal educational project for understanding the challenges and methodologies in image authentication.

## Features

Forensi-Py currently includes three core forensic analysis modules:

1.  **Integrity Verification (Hashing):**
    * Calculates and displays **MD5** and **SHA-256** cryptographic hash values of the image file.
    * **Purpose:** Provides a unique digital fingerprint for the image. Any alteration, no matter how minor, will result in a different hash, proving that the file's integrity has been compromised since the hash was last recorded. Essential for maintaining a chain of custody.

2.  **Metadata (EXIF) Analysis:**
    * Extracts and displays key **EXIF** (Exchangeable Image File Format) metadata, such as camera make/model, date/time of capture, and crucially, any `Software` tags indicating post-capture editing.
    * **Purpose:** Reveals information about the image's origin and history. Inconsistencies (e.g., a `Software` tag pointing to an advanced photo editor, or a complete lack of EXIF data where it would normally be present) can be strong indicators of manipulation or processing.

3.  **Error Level Analysis (ELA):**
    * Performs Error Level Analysis to detect areas of an image that have been re-saved with a different JPEG compression level than the rest of the image.
    * **Purpose:** Highlights regions where new content might have been inserted, or existing content significantly altered. Manipulated areas often show a distinctly different "error level" (appearing brighter or darker with sharp boundaries) compared to the original parts of the image, due to their unique compression history. The ELA output is provided as a visual grayscale image.

## How It Works

The tool is a Python-based command-line interface (CLI) application. It takes an image file path as input, processes it through each analysis module, and outputs a summary report to the terminal. The ELA module also generates a separate visual output window and saves the ELA image.

## Getting Started

### Prerequisites

To run Forensi-Py, you need Python 3 installed on your system. You also need the following Python libraries:

* `Pillow` (PIL Fork)
* `Numpy`
* `Matplotlib`

You can install them using `pip`:

```bash
pip install Pillow numpy matplotlib
```

##clone the repository
```bash
git clone
```
