Smart Entry-Exit System for IIT Guwahati

https://github.com/Ritikkoshta02/Automated-Entry-Exit-System-using-Image-Processing/assets/78507349/922c02b7-70ad-40f7-8764-7ed7b904e386

An Automated Entry-Exit System built specifically for IIT Guwahati, leveraging YOLO-based object detection, face recognition, and OCR techniques to validate individuals using their ID cards. The system ensures secure, real-time, and seamless entry-exit logging with a modern UI and backend integration.

Overview
This project implements a smart surveillance and identity verification system using real-time image processing, face recognition, and text extraction. It detects ID cards through a webcam, classifies their type, extracts details using OCR, and matches the face on the ID card with a live webcam feed. Entry and exit logs are stored in a MySQL database and an Excel sheet.

Features
ID Card Detection: Uses YOLOv5 to detect ID cards in real-time via webcam.

Image Processing: Automatically crops and aligns ID card for accurate downstream processing.

Card Classification: Classifies ID card type (e.g., College ID, Aadhar, DL) using a CNN model. Currently supports College ID cards.

Face Recognition: Verifies identity by matching the card's photo with a live webcam image.

Text Extraction: Extracts textual data (e.g., Name, Roll No.) from the ID using pytesseract.

Database Integration: Stores ID and entry/exit logs using MySQL for easy tracking and reporting.

Frontend with Streamlit: Interactive and user-friendly web interface for admins/staff.

Automatic Logging: Maintains Excel logs based on an even-odd roll number logic for entry/exit.

Notification System: Sends alerts to students outside the campus before gate closing time.

Installation
Clone the repository:

git clone https://github.com/Ritikkoshta02/Automated-Entry-Exit-System-using-Image-Processing.git
cd Automated-Entry-Exit-System-using-Image-Processing

Install dependencies:

pip install -r requirements.txt

Configure Database:

Set up your MySQL server.

Create the required tables as per your schema.

Update the credentials and database name in config.py.

Run the application:

streamlit run app.py

Usage
Ensure a webcam is connected and positioned to capture ID cards.

Run the system using the command above.

The system will:

Detect ID cards

Crop and extract the image

Perform face recognition with live capture

Classify ID type

Extract text from the ID

Log entry or exit based on roll number parity (even/odd)

Use the Streamlit UI to visualize logs and system status.

Future Scope
Add support for Aadhar and Driving License recognition.

Improve face recognition accuracy and speed.

Integrate with central academic/student systems.

Enhance notification system and mobile UI.

Tech Stack
YOLOv5 – Real-time object detection

OpenCV + Face Recognition – Identity verification

pytesseract (Tesseract OCR) – Text extraction

Streamlit – Web-based user interface

MySQL – Backend database

Excel (via pandas) – Log recording

Credits
YOLOv5

Face Recognition

Tesseract OCR

Streamlit
