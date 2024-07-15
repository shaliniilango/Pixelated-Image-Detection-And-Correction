PIXELATION DETECTION AND CORRECTION:

In today's digital age, high-quality images are crucial across various fields like photography, video production, and medical imaging, yet pixelation remains a common problem, causing images to appear blocky and distorted. This report, "Detecting and Correcting Pixelated Images," provides a comprehensive exploration of this issue. It starts with an explanation of problem statement , then delves into detection methods including visual inspection, automated algorithms, and edge detection techniques. This project  aims to equip readers with the knowledge and tools to effectively address pixelation, enhancing image quality and utility.

PROBLEM  STATEMENT:-
                     The problem involves detecting and correcting pixelated images to enhance visual quality and accuracy in various digital applications. The goal is to develop methods that can automatically identify pixelation in images and apply suitable corrections to restore clarity and detail, ensuring optimal image presentation across different platforms and uses. This project aims to explore both detection techniques for identifying pixelation and correction methods such as super-resolution algorithms to improve image quality effectively. The ultimate objective is to provide users with tools that can reliably enhance image resolution and mitigate the visual artifacts associated with pixelation in digital imagery
                     
The The proposed solution involves developing a two-stage system that integrates deep learning-based pixelation detection and advanced super-resolution techniques for image correction. The system will leverage Convolutional Neural Networks (CNNs) for detecting pixelation and Enhanced Super-Resolution Generative Adversarial Networks (ESRGAN) for enhancing the image quality. This approach ensures that images are not only identified for pixelation but also corrected to a high degree of visual fidelity. 

1. DETECTION METHODOLOGY:-

   
•	Machine Learning Model: Utilize a pre-trained convolutional neural network (CNN) model (pixelated_image_detector.h5) to classify images as pixelated or non-pixelated.

•	Preprocessing: Resize and normalize images for consistent input to the detection model.

•	Thresholding: Use a threshold (e.g., 0.5) to classify images based on the model's prediction probability.

2. CORRECTION TECHNIQUES:-
•	ESRGAN Super-Resolution: Implement ESRGAN (Enhanced Super-Resolution Generative Adversarial Network) to enhance pixelated images by generating high-resolution versions with improved visual quality.

o	PyTorch Implementation: Load a pre-trained ESRGAN model (RRDB_ESRGAN_x4.pth) and process images using GPU acceleration if available.

o	Output Handling: Convert and display the corrected images, allowing users to visualize the improvements.

•	Real-ESRGAN Alternative: Provide an alternative correction method using Real-ESRGAN, executed through a subprocess call to realesrgan-ncnn-vulkan.exe.

3. GRAPHICAL USER INTERFACE (GUI):-
   
•	Tkinter Application: Developed a GUI application that allows users to:

o	Load images from local directories.

o	Display original and corrected images side by side.

o	Dynamically update pixelation detection status and correction results.

SAMPLE OUTPUT:

![image](https://github.com/user-attachments/assets/f1c547c1-14b3-485d-ba72-b973ba883db7)
![image](https://github.com/user-attachments/assets/791ff1a7-0741-4330-b278-a125c5f19a7c)
![image](https://github.com/user-attachments/assets/58921d28-af0f-4f19-a1cc-52cd97f4d31b)

video demo: https://drive.google.com/file/d/1eaJt9NcrZVADwc6R6n9GsFURZ3gsshoU/view?usp=sharing

the corrected images using both ESRGAN and real_ESRGAN are saved seperately in the working folder as "corrected_image_esrgan.jpg" and "corrected_image_real_esrgan.jpg"


Installation and Running the Project:

To run this project from GitHub, follow these steps:

Prerequisites:

Ensure you have the following software installed on your system:

Python 3.7 or later
pip (Python package installer)
Git

Clone the Repository

Open a terminal or command prompt.

Clone the repository using the following command:
git clone https://github.com/your-username/your-repository-name.git

Navigate to the project directory:

cd your-repository-name

Set Up a Virtual Environment

Create a virtual environment to manage dependencies:

python -m venv venv

Activate the virtual environment:
Windows:

venv\Scripts\activate

macOS/Linux:

source venv/bin/activate

Install Dependencies:
Install the required Python packages:

pip install -r requirements.txt

Download and Prepare Pre-trained Models

Pixelation Detection Model: Place the pixelated_image_detector.h5 file in the appropriate directory. (Ensure you have the model file downloaded and located in the specified path in the script.)

ESRGAN Model: Place the ESRGAN model file (RRDB_ESRGAN_x4.pth) in the appropriate directory.

Real-ESRGAN: Ensure you have the Real-ESRGAN executable (realesrgan-ncnn-vulkan.exe) and place it in the specified directory.

Run the Application

Start the application using the following command:

python pixelation_correction.ipynb

for detailed report on this project check here: https://drive.google.com/file/d/18OLv4RZd4eFT7AfXYyu2cg4KlW1_XOBa/view?usp=sharing
PROJECT PPT : https://drive.google.com/file/d/1xMsLlFMVXWizOpjbW2riYCI7KPjOhBDu/view?usp=sharing

NOTE: This project is done as a part of intel unnati industrial training.







