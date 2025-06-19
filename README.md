# Hiding Sensitive Information Inside Images using LSB + AES Steganography

In This project, I have demonstrated how to securely embed encrypted messages into image files using a combination of **AES encryption** and **Least Significant Bit (LSB) steganography**.

> Built as part of the **Cybersecurity Internship Program** by **EDUNET Foundation (2025)**

---

## Project Description

In this hybrid approach, the plaintext message is first **encrypted using AES** (Advanced Encryption Standard), ensuring confidentiality.  
The encrypted bytes are then **embedded bit-by-bit** into the image's pixel data using **LSB steganography**, making the presence of hidden information undetectable to the human eye.

### Why this approach?

- **AES ensures encryption** even if the image is extracted.
- **LSB hides the encrypted bytes** in the image.

---

## Technologies Used

- Python 3.x
- OpenCV (`cv2`)
- NumPy
- PyCryptodome (for AES encryption)
- Matplotlib (for image display)

---

## Features

- AES-CBC encryption with a key derived from SHA-256
- Bit-level embedding using Least Significant Bit
- Complete end-to-end flow: message → encrypted → embedded → extracted → decrypted
- Works with any image of sufficient size (e.g. `.png`, `.jpg`)

---

## Folder Structure

```

LSB_AES_Steganography_Project/
│
├── stegno_lsb_aes.ipynb         # Project Jupyter notebook
├── cover.png                    # Sample input image
├── stego_lsb_aes.png            # Output image with hidden encrypted data
├── README.md                    # This file

```

---

## How to Run the Project

1. Clone the repo or download the ZIP
2. Open `stegno_lsb_aes.ipynb` in Jupyter Notebook
3. Ensure you have the required libraries:
   ```bash
   pip install opencv-python numpy pycryptodome matplotlib
   ```
4. Replace the `cover.png` with your own image (ensure it's large enough)
5. Set your secret message and key in the notebook
6. Run all cells to embed → save → extract → decrypt the message

---

## Sample Output

**Input Message:**

**Key : Enter The Key For Encode The Information**
```
Key@123
```

**Message : Enter The Text Information You Want to hide inside Image**

```
I am a CyberSecurity Intern at Edunet Foundation!
```

**Key : Enter The Same Key For Decode The Information**
```
Key@123
```

**Decrypted Output After Extraction:**

```
I am a CyberSecurity Intern at Edunet Foundation!
```

---

## Use Cases

* Hiding passwords or keys in images
* Securing communication in covert channels
* Educational demonstrations for steganography + encryption

---

## Developed By

**Aditya Kumar**
B.Tech Computer Science – Gaya College of Engineering, Gaya (2027)   
Cybersecurity Intern @ EDUNET Foundation (May - June 2025)

---

## Future Scope

* Add GUI interface using Streamlit or Tkinter
* Support for hiding files (PDF, MP3, DOCX)
* Add image integrity checks and tamper detection

---

## References

* [PyCryptodome Documentation](https://pycryptodome.readthedocs.io)
* [OpenCV Python Docs](https://docs.opencv.org/)
* EDUNET Foundation Cybersecurity Internship Sessions (2025)

---

## License

This project is open-source and free to use for **educational and non-commercial** purposes.

> “Encryption hides the content. Steganography hides the existence.”
