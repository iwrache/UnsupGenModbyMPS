# Experiment on MNIST

## `./`

* `MNIST_main.py` carries out the trianing.

* `assessing.py` consists of reconstruction and denoising, but denoising has not a very good performance.

* `canon_middle.py` is a simple piece of script that gauge transform a MPS into the mix-canonical form whose only uncanonical tensor is in the center. You can immitate its way to carry out gauge transformation that you need.


### `./mnist_ori`

* `data.npy` saves a (70000, 28*28) numpy array of the MNIST images in grayscale.

* `target.npy` saves their corresponding labels.

### `./mnist-rand1k_28_thr50_z`

* `_data.npy` saves a (1000, 28*28) numpy array which is the binary data;

* `_prob.npy` saves a (1000,) numpy array which is the empirical probability distribution of the dataset in `_data.npy`;

* `_shannon.npy` saves the Shannon entropy of the dataset in `_data.npy`;

* `example.pdf` shows some of the images in the dataset;

* `indices.npy` indicate the indices of these 1000 images in the original MNIST database.

#### `./mnist-rand1k_28_thr50_z/recon-denos`

* `ori_indices.npy` saves the indices among the 1000 images for the 20 images in `original.pdf`;

* `annoised05.npy`, `annoised10.npy` and `annoised20.npy` are the results of adding different levels of noise (5%, 10%, 20%) on these 20 images, respectively.

#### `./mnist-rand1k_28_thr50_z/others1k`

* `_data.npy` saves an (1000, 784) array for 1000 binarized mnist images other than those indicated by `./mnist-rand1k_28_thr50_z/indices.npy`.

* `indices.npy` saves the indices among the original MNIST database of the images in `_data.npy`.

* `otherimg.npy` saves and 20 images in `_data.npy`, and they are demonstrated in `otherimg.pdf`.