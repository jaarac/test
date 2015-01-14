Visual Recognition Library
==========================

This library is provided *as is*. ...

1. Dependencies
---------------

* python 2.7
* numpy
* scikit-learn -> scikit-learn.org/
* scikit-image -> http://scikit-image.org/
* colorama -> https://pypi.python.org/pypi/colorama
* gcc
* vlfeat -> http://www.vlfeat.org/
* openmp -> http://openmp.org/wp/

***1.1. Installing Dependencies in Debian***

In debian you can install all the dependencies, except vlfeat, with:

    # apt-get install python2.7 python-numpy python-skimage python-sklearn python-colorama build-essential libgomp1

2. Installation
---------------

This is an example installation, tested on linux (Linux-3.11-2-amd64-x86_64 with Debian)

***2.1. Download and compile the VLFeat library***

> $ wget http://www.vlfeat.org/download/vlfeat-0.9.17-bin.tar.gz

> $ tar -xf vlfeat-0.9.17-bin.tar.gz

> $ cd vlfeat-0.9.17

> $ make

> $ export VLFEAT_PATH=$PWD

> $ cd ../

***2.2. Build the module***

> $ python setup.py build

***2.3. Install the module***

For single user installation run as user:

> $ python setup.py install --user

For all users installation run as root:

> # python setup.py install

***2.4 Run simple example***

> $ python samples/descriptors.py --image="path_to_image_file" --output="path_to_existing_directory"


3. Classification example
---------------------------------

Downloading the KTH_TIPS2 dataset.

> $ mkdir dataset

> $ cd dataset

> $ wget http://www.nada.kth.se/cvap/databases/kth-tips/kth-tips2-a_col_200x200.tar

> $ tar xvf kth-tips2-a_col_200x200.tar

Running the classification example on the KTH_TIPS2 dataset.

> $ cd ..

> $ python bin/classification.py --output=TMPData --dataset=dataset/kth-tips2-a_col_200x200 --experiment=lbp_mob

Wait for the results, approx 30' for a core i7 machine.
