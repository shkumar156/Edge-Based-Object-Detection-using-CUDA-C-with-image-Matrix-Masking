# Edge-Based-Object-Detection-using-CUDA-C-with-image-Matrix-Masking
📘 Objective

To detect objects (edges) in an image using a 3×3 mask in CUDA C by converting the image to matrix form and processing each pixel in parallel using GPU threads.

⚙️ Tools & Technologies

CUDA Toolkit (nvcc compiler)

C/C++ with NVIDIA extensions

BMP Image Format

Google Colab (for GPU access)

Python (for preprocessing/postprocessing)

🧠 Working Principle

The input image is converted to grayscale using weighted RGB values.

A 3×3 Laplacian mask is applied to each pixel using a CUDA kernel.

Each thread processes one pixel and computes the convolution result.

The result is written back as a new image showing detected edges.

The output matrix can also be viewed to understand detection numerically.

🧪 Mask Used

Laplacian Edge Detection Mask:

[[-1, -1, -1],

 [-1,  8, -1],

 [-1, -1, -1]]

This highlights areas with high-intensity changes (edges of objects).

🧾 Steps

Upload image and convert to .bmp

Compile CUDA file with nvcc

Run executable with input and output filenames

Display or download the processed result

🖼️ Sample Output

Input: Dog image
![Cat4](https://github.com/user-attachments/assets/e1b2a03b-9667-411f-8798-f33756cf77d6)

Output: 
1. 10x10 Matix showing the object detection 

![image](https://github.com/user-attachments/assets/1c88195c-095d-4b2d-b1a8-bf9cb1002edf)


2. Grayscale image with clear object boundaries

![image](https://github.com/user-attachments/assets/372dc361-a82f-4d20-9ef8-1ce2166d65f6)



