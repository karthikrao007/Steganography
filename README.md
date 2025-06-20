# 🕵️‍♂️Steganography -Hiding Information in the Image

**"The art and science of hiding information within another message"**

This project demonstrates how to hide a secret text message inside a PNG image using **LSB (Least Significant Bit) steganography**, along with an added layer of **XOR encryption** using a key. The goal is to achieve hidden, secure communication while preserving image quality.

## 🎯Project Objective

To implement a steganography technique that securely hides text inside an image by modifying only the least significant bits (LSBs) of pixel values. This project was created as part of a college assignment to explore basic cryptographic techniques and image processing using Python.

## 🛠️Features

✅ Hide a secret message inside a PNG image
✅ XOR-based encryption using a secret key
✅ Bit-by-bit embedding in the least significant bits
✅ Clean image output with minimal distortion
✅ Accurate message extraction and decryption

## 🧠How It Works

1. Convert each character of the message to ASCII.
2. Encrypt each ASCII value using XOR with a repeating key.
3. Convert the encrypted number to an 8-bit binary string.
4. Embed each bit into the LSB of pixel values (B, G, R channels).
5. Save the modified image as a `.png`.
6. During decoding:
   - Extract LSBs in order
   - Reconstruct 8-bit encrypted characters
   - XOR with the key to retrieve the original message

 
## 🧑‍💻Technologies Used

- Python 3.x
- OpenCV (`cv2`)
- NumPy


## 🚀How to Run

### 🔧Step 1: Install dependencies

  - pip install opencv-python numpy

### 📂Step 2: Prepare your files

   - Input image: Use a `.png` image
   - Output will be saved as `StegnoEncrypted_image.png`

### 🧾Step 3: Run the script

   - python LSBBasedSteganography.py

> You can change the message and key directly in the script.


## 🔑Example

text = "Secret"
key = "123"

- This will encrypt "Secret" using "123" and hide it inside the image.
- After decoding, the output will be:
  
  Decrypt text Secret


## ⚠️Important Notes

- Always use ".png" images. **do not use ".jpg"**, as JPEG compression may corrupt the hidden bits.
- This is a simple project and does not support long messages or dynamic message lengths yet.
- Feel free to modify the script to support file input or command-line arguments.

  
## 📌Educational Use

This project was built for a **college-level demonstration** on digital privacy, steganography, and beginner-level cryptography. You’re free to:
- Modify it
- Learn from it
- Extend it with features like dynamic message lengths, password protection, etc.


## 🙋‍♂️ Author

**Karthik Rao🐔**  
Beginner Python & Cybersecurity Enthusiast  
Made with ❤️ as part of a college project
