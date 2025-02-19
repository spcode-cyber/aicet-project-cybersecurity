
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
Key Unique Features:
Steganography with RGB Channels:
The message is embedded directly into the image pixels by converting each character of the message into its corresponding RGB value using a dictionary (d and c).
The message is hidden by modifying the RGB values of the image in a way that does not noticeably distort the image visually, making it a form of steganography.
Encryption with Password:
Before embedding the message, a password is required for encryption. The message can only be decrypted with the correct password, which adds a layer of security.
The use of a password ensures that only those who know the passcode can retrieve the hidden message, enhancing the privacy of the embedded data.
Image-based Encryption:
This project uses the actual image as a medium for encryption. Rather than creating an entirely new encrypted file, the image itself becomes the carrier of the hidden message.
The message is embedded pixel by pixel (in RGB channels), making the encrypted message part of the image's data.
Cross-platform Displaying:
The code includes a command to automatically open the encrypted image (os.system("start encryptedImage.jpg")), which works on Windows.
This makes it easier for the user to visualize the encrypted image and see how the message is hidden without needing any additional viewer.
Manual Decryption:
The decryption process requires input from the user, specifically the correct password to decode the hidden message.
This manual intervention allows for added security, as it prevents unauthorized access to the original message without the correct password.



