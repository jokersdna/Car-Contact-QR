Car Contact QR Code

This project allows you to generate a QR code that links to a contact page. When someone scans the QR code, they will be redirected to a webpage with your contact details.

Features

Generate a QR code with a URL to your contact page.

Host the contact page on GitHub Pages for free.

Easily printable QR code to place on your car windshield.

Setup Instructions

1. Generate the QR Code

Make sure you have Python installed. Then, install the required library:

pip install qrcode[pil]

Run the following Python script to generate the QR code:

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

2. Host the Contact Page on GitHub Pages

Create a GitHub repository and name it something like Car-Contact-QR.

Upload your contact.html file to the repository.

Go to Settings > Pages and select the main (or master) branch as the source.

Copy the generated URL (e.g., https://your-username.github.io/Car-Contact-QR/contact.html).

3. Print & Use Your QR Code

Run the script to generate contact_qr.png.

Print and place the QR code on your windshield.

Scan it with a phone to ensure it redirects correctly.

Contact Page (Example)

Save this as contact.html:

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Contact Me</title>
    <style>
        body { font-family: Arial, sans-serif; text-align: center; margin: 50px; }
        .container { max-width: 500px; margin: auto; background: #f8f9fa; padding: 20px; border-radius: 10px; }
        h2 { color: #333; }
        p { font-size: 18px; }
        .contact { font-weight: bold; font-size: 20px; color: #007bff; }
    </style>
</head>
<body>
    <div class="container">
        <h2>Contact Me</h2>
        <p>If you need to reach me, please use the details below:</p>
        <p class="contact">📧 Email: your.email@example.com</p>
        <p class="contact">📞 Phone: +123 456 7890</p>
    </div>
</body>
</html>

License

This project is open-source. Feel free to modify and use it as needed!
