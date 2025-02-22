# Car-Contact-QR
Upload Your Contact Page
On your new repository page, click Add File > Upload Files.
Upload your contact.html file.
Click Commit changes.
Step: Enable GitHub Pages
Go to Settings in your repository.
Scroll down to the Pages section.
Under Branch, select main (or master) and / (root).
Click Save.
GitHub will generate a URL like:
bash
Copy
Edit
https://your-username.github.io/Car-Contact-QR/contact.html
Copy this URL.
Step 4: Generate the QR Code
Modify your Python script to use the GitHub Pages URL:

python
Copy
Edit
import qrcode

# Your GitHub Pages URL
contact_url = "https://your-username.github.io/Car-Contact-QR/contact.html"

# Generate QR Code
qr = qrcode.QRCode(version=1, box_size=10, border=5)
qr.add_data(contact_url)
qr.make(fit=True)

# Save QR code as an image
img = qr.make_image(fill="black", back_color="white")
img.save("contact_qr.png")

print("QR Code generated! Scan it to test.")
Step 5: Print & Use Your QR Code
Run the script, and it will generate contact_qr.png.
Print the QR code and place it on your windshield.
Test it by scanning it with your phone.
