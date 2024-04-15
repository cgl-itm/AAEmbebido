Option 1: Live Inference on Raspberry Pi
If you are using a Raspberry Pi, you will want to follow these instructions. More information about installing the Edge Impulse runner on Linux can be 
found here, and information about installing the Edge Impulse Python package can be found here.

Open a terminal and enter the following commands to install the Edge Impulse command line tools and required libraries:

`curl -sL https://deb.nodesource.com/setup_12.x | sudo bash -`

`sudo apt install -y gcc g++ make build-essential nodejs sox gstreamer1.0-tools gstreamer1.0-plugins-good gstreamer1.0-plugins-base gstreamer1.0-plugins-base-apps`

`npm config set user root && sudo npm install edge-impulse-linux -g --unsafe-perm`

`sudo apt install -y libatlas-base-dev libportaudio0 libportaudio2 libportaudiocpp0 portaudio19-dev `

`python -m pip install edge_impulse_linux -i https://pypi.python.org/simple`

We also need the Python version of OpenCV (which comes with Numpy) to assist with various image manipulation operations. If you have not done so already, install OpenCV with pip:

`python -m pip install opencv-python`

Create a folder to hold your program and model file:

`mkdir -p Projects/image-classification-dnn`

`cd Projects/image-classification-dnn`

Use the Edge Impulse tool to download your model file. 

`edge-impulse-linux-runner --clean --download modelfile.eim`

Note: The model file we get is a .eim file that includes both the model and any necessary feature extraction methods. For now, those feature extraction methods just pass raw data to the model for inference.

Your job is to create a program that continuously captures images from the camera (e.g. Pi Camera), adjusts the images as necessary, and performs inference to classify the image. You should output the predicted class to either the console or draw it on the preview window.
