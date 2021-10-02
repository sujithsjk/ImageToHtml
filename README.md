This project builds on the synthetically generated dataset and model architecture from pix2code by Tony Beltramelli and the Design Mockups project from Emil Wallner & sketch-Code From Ashwin kumar


# Generating HTML Code from a hand-drawn Sketches



# Prerequisites

Python 3+
pip 
 
 # Packages 
 
 Keras 
tensorflow==1.4.0
nltk==3.2.5
opencv-python
numpy==1.13.1
h5py==2.7.1
matplotlib==2.0.2
Pillow==4.3.0
tqdm==4.17.1
scipy==1.0.0


# Install dependencies

pip install -r requirements.txt



# Download the data and pretrained weights:

# Getting the data, 1,700 images, 342mb

git clone https://github.com/ashnkumar/sketch-code.git

cd sketch-code

cd scripts

# Get the data and pretrained weights

sh get_data.sh
sh get_pretrained_model.sh


# Converting an example drawn image into HTML code, using pretrained weights:

cd src

python convert_single_image.py --png_path ../examples/drawn_example1.png \
      --output_folder ./generated_html \
      --model_json_file ../bin/model_json.json \
      --model_weights_file ../bin/weights.h5


 
