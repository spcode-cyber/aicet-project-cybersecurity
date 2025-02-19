
In the project you mentioned (image encryption and decryption), the primary library used is OpenCV. Here’s a list of the libraries used in the code:
1. OpenCV (cv2):
Purpose: OpenCV is used to read, manipulate, and save the image.
Functions used:
cv2.imread() — Reads an image from a file.
cv2.imwrite() — Saves an image to a file.
cv2.imread() — Loads an image.
os.system() — This is used to open the encrypted image using the default viewer (on Windows).


Installation: You can install OpenCV using
pip install opencv-python

2. os:
Purpose: This library is used to interact with the operating system. In your code, it’s used to open the encrypted image on Windows by running the command os.system("start encryptedImage.jpg").
Functions used:
os.system() — Executes system commands like opening files or programs.
Installation: os is part of the Python Standard Library, so you don’t need to install it separately.
3. string (implicitly used in the original code but not directly referenced in the encryption-decryption logic):
Purpose: In your original encryption script, string was used to potentially handle a character set. However, it’s not directly referenced in the final encryption and decryption logic.
It could be useful if you were to map characters to indices or process the message further.
Installation: string is also part of the Python Standard Library, so no installation is needed.
Summary of Libraries:
OpenCV (cv2): For image processing (reading, saving, manipulating the image).
os: For system-level operations (opening images in the default viewer).

