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

--- Object Detection Output Matrix (Top-left 10x10) ---
  0   0   0   0   0   0   0   0   0   0 
  0   1   3   3   1   2   4   4   3   4 
  0   2   3   3   0   0   1   4   2   2 
  0   2   4   1   2   3   3   1   5   4 
  0   1   4   1   5   3   3   8   7   3 
  0   1   7   1   5   1   2   6  10   1 
  0   8   8   4   2   3   5  11   7   5 
  0   0   6   1   1   6   0  10   6   3 
  0   2   1   2   2   1   2   9   6   2 
  0   2   1   3   3   1   2   9   7   3 
Object detection completed. Output saved to output.bmp

2.Grayscale image with clear object boundaries

![image](https://github.com/user-attachments/assets/372dc361-a82f-4d20-9ef8-1ce2166d65f6)



