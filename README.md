### Multi-Scale CNN Classifier 
This project uses Google TensorFlow to implement a multi-scale convolutional neural network architecture created using concepts from [LeNet 5](http://yann.lecun.com/exdb/publis/pdf/lecun-01a.pdf) (LeCun, 1998),
the [Sermanet & LeCun's multi-scale CNN architecture](https://drive.google.com/open?id=0B_huqLwo5sS1RzVxMlFKV0RrSmc) (2011), and [the dropout concept](https://drive.google.com/open?id=0B_huqLwo5sS1QXd3S0NJY2pNeFk) (Srivastava, 2014). 
We test the classifier's performance using the [German Traffic Sign Dataset](http://benchmark.ini.rub.de/?section=gtsrb&subsection=dataset).

#### Installation
This procedure was tested on Ubuntu 16.04 and Mac OS X 10.11.6 (El Capitan). GPU-accelerated training is supported on Ubuntu only.

Prerequisites: Install Python package dependencies using [my instructions.](https://github.com/alexhagiopol/deep_learning_packages) Then, activate the environment:

    source activate carnd-term1

Optional but recommended: Install support for NVIDIA GPU acceleration with CUDA v8.0 and cuDNN v5.1:

    wget https://www.dropbox.com/s/08ufs95pw94gu37/cuda-repo-ubuntu1604-8-0-local-ga2_8.0.61-1_amd64.deb
    sudo dpkg -i cuda-repo-ubuntu1604-8-0-local-ga2_8.0.61-1_amd64.deb
    sudo apt-get update
    sudo apt-get install cuda
    wget https://www.dropbox.com/s/9uah11bwtsx5fwl/cudnn-8.0-linux-x64-v5.1.tgz
    tar -xvzf cudnn-8.0-linux-x64-v5.1.tgz
    cd cuda/lib64
    export LD_LIBRARY_PATH=`pwd`:$LD_LIBRARY_PATH
    cd ..
    export CUDA_HOME=`pwd`
    sudo apt-get install libcupti-dev
    pip install --ignore-installed --upgrade https://storage.googleapis.com/tensorflow/linux/gpu/tensorflow_gpu-1.1.0-cp35-cp35m-linux_x86_64.whl

Clone the image_classifier repo:

    git clone https://github.com/alexhagiopol/image_classifier
    cd image_classifier

Download the [German Traffic Dataset](http://benchmark.ini.rub.de/?section=gtsrb&subsection=dataset) with annotations in a Python Pickle format that is easy to work with:
        
    wget https://www.dropbox.com/s/mwjjb67xbpj6rgp/traffic-signs-data.tar.gz
    tar -xvzf traffic-signs-data.tar.gz
    rm -rf traffic-signs-data.tar.gz

#### Execution
Perform preprocessing and data augmentation:

    python preproc.py
    
Run the code to train the model on your machine:

    python main.py

### Technical Report

#### Dataset Summary

#### Exploratory Visualization

#### Preprocessing

#### Model Architecture

#### Model Training

#### Solution Approach

#### Acquiring New Images from Outside the Dataset

#### Performance on New Images

#### Model Certainty


    