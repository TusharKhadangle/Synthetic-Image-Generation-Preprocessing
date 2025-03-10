# Synthetic-Image-Generation-Preprocessing

Detailed Approach
1. Image Generation (Python)
Objective:
Generate high-quality images based on a textual prompt.
Key Points:
Uses the Stable Diffusion model (runwayml/stable-diffusion-v1-5) from the diffusers library.
Checks for a CUDA-enabled GPU and sets the device accordingly.
Generates three images using a controlled random seed to ensure reproducibility.
Saves images as gen_image_1.png, gen_image_2.png, and gen_image_3.png.


2. Image Preprocessing (Python)
Objective:
Prepare the generated images for model inference.
Process:
Reads each image using Pillow.
Applies a transformation pipeline with torchvision:
Resizes images to a target size (224×224 pixels).
Converts images to tensors.
Normalizes them using standard ImageNet mean and standard deviation.
Converts images to grayscale (1 channel).
Saves the processed tensor along with metadata (original image size and source path) in .pt files (e.g., preprocessed_gen_image_1.png.pt).
