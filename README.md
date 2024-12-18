This script processes all image files in a specified directory and calculates total branch lengths using a skeletonization-based approach.

Requirements
Python 3.9 or later
OpenCV 4.10.0
NumPy 1.26.4
scikit-image
pandas
Install dependencies using pip:
pip install opencv-python numpy scikit-image pandas

Input Data
1. Place all images (PNG, JPG, JPEG, TIF, TIFF) in the specified directory.
2. Update image_directory in the code with your input directory path.

How It Works
1. Reads each image in grayscale.
2. Thresholds the image at a pixel intensity of 50.
3. Skeletonizes the binary image to extract one-pixel-wide branch structures.
4. Labels and measures each branch segment.
5. Uses perimeter values as proxies for branch lengths.
6. Sums the perimeters to get the total branch length for each image.

Output
1. The script outputs a table of image file names and total branch lengths (in pixels) as an Excel file.  
2. Update `output_path` in the code with your desired save path.

Running the Script
1. Update `image_directory` and `output_path` in the script.
2. Run:
python script_name.py
3. The output Excel file will be saved to the specified location.

Tips
1. Consider experimenting with different threshold values if the segmentation results are not satisfactory.
2. Ensure the images are of consistent quality and resolution for accurate measurements.


