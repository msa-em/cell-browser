---
title: Supplementary Information
numbering:
  enumerator: 12.%s
---

---

# MNIST autoencoder

## Training history

:::{figure} #sfig12a_data
:label: sfig12a
:placeholder: ./figures/sfig12a.png
Autoencoder MSE reconstruction loss over one-hundred epochs of training on the MNIST dataset.
:::

---

# NucleusNet

:::{figure} #sfig12b_data
:label: sfig12b
:placeholder: ./figures/sfig12b.png
The number and brightness of ROIs in the stitched images was measured using the associated cellpose mask files. A pre-computed centroid 694.5 ROIs and 79.0 mean intensity was marked.
:::

```{list-table} Representative stitched images ranked by distance to centroid: 694.5 ROIs, 79.0 mean intensity
:label: table3
:header-rows: 1

* - Filename
  - Number of ROIs
  - Mean intensity
  - Distance*
* - Run72TR_bottom_left
  - 685
  - 78.6
  - 0.046
* - Run63TR_top_right
  - 709
  - 78.6
  - 0.066
* - Run72BR_top_right
  - 687
  - 80.3
  - 0.074
* - Run68TR_top_right
  - 711
  - 79.6
  - 0.076
* - Run25BR_top_right
  - 698
  - 77.5
  - 0.079
* - Run25BR_bottom_left
  - 681
  - 78.0
  - 0.080
* - Run72BR_top_left
  - 712
  - 79.5
  - 0.080
* - Run102TR_top_left
  - 716
  - 78.3
  - 0.099
* - Run50TL_top_right
  - 714
  - 77.8
  - 0.104
* - Run72BL_top_right
  - 720
  - 79.1
  - 0.109
```
Z-score-normalized euclidean distance was used for equal weighting because the features had different scales.

---

# NucleusNet autoencoder

## Model

The entire single-cell image collection was sharded into [TFRecords](https://www.tensorflow.org/tutorials/load_data/tfrecord) to better load the dataset into memory and shuffle it during training.
An autoencoder model was trained for 50 epochs on NucleusNet and the encoder and decoder weights were saved.
The input was 256 by 256 pixel grayscale images that were embedded into 512-dimensional latent vectors.
Barkley interpreted that the model overfit because the training loss and validation loss diverged at later epochs.

### Training history

:::{figure} #sfig12c_data
:label: sfig12c
:placeholder: ./figures/sfig12c.png
History of MSE reconstruction loss (batch size: 32) for the training and validation datasets over 50 epochs.
:::

## Latent space interpolation

A method to evaluate the quality of latent space is interpolation, whereby mixing codes in latent space and decoding the result creates a semantically meaningful combination of the datapoints [@doi:10.48550/arXiv.1807.07543].
Interpolating with an autoencoder describes the process of using the decoder to decode a convex combination of two latent vectors [@doi:10.48550/arXiv.1807.07543].
A high-quality interpolation should have two characteristics: intermediate points along the interpolation should resemble real data and they should provide a semantically meaningful transition between the endpoints [@doi:10.48550/arXiv.1807.07543].
Interpolating between any two latent vectors of embedded NucleusNet images produced reasonable intermediate reconstructions from the decoder with a smooth transition between endpoints ([](#sfig12d)).

:::{figure} #sfig12d_data
:label: sfig12d
:placeholder: ./figures/sfig12d.png

Random pairs from NucleusNet-10K. All images are decoded vectors. t=0.00 and t=1.00 correspond to latent vectors of real images. Four intermediate interpolations at t=0.20, t=0.40, t=0.60 and t=0.80 are mixed codes. Run the notebook to resample random pairs of embedded vectors from NucleusNet-10K.
:::

---

# Replication study

Barkley noted the type of result for all data in the original study.
There were four possible data types; light microscopy image, electron microscopy image, correlative light-electron microscopy image, and quantitative analysis.
Some figure panels had multiple images.
If the images were unique examples, then the figure counted as more than one image.
Multi-channel or time-lapse images were considered one image with multiple frames.

```{list-table} Assessment of results by data type: 45/47 (96%) were representative images.
:label: table4
:header-rows: 1
* - Figure
  - Data type
  - Images
  - Frames
  - Frame type
* - 1A
  - Light microscopy image
  - 1
  - 1
  -
* - 1B
  - Light microscopy image
  - 1
  - 1
  -
* - 1C
  - Electron microscopy image
  - 1
  - 1
  -
* - 1D
  - Correlative light-electron microscopy image
  - 1
  - 1
  -
* - 1E
  - Correlative light-electron microscopy image
  - 1
  - 1
  -
* - 1F
  - Electron microscopy image
  - 1
  - 1
  -
* - S1A
  - Light microscopy image
  - 2
  - 1
  -
* - S1B
  - Electron microscopy image
  - 4
  - 1
  -
* - 2A
  - Electron microscopy image
  - 1
  - 1
  -
* - 2B
  - Electron microscopy image
  - 1
  - 1
  -
* - 2C
  - Electron microscopy image
  - 1
  - 1
  -
* - 2D
  - Electron microscopy image
  - 1
  - 1
  -
* - 2E
  - Electron microscopy image
  - 1
  - 1
  -
* - 2F
  - Electron microscopy image
  - 1
  - 1
  -
* - 2G
  - Electron microscopy image
  - 1
  - 1
  -
* - 2H
  - Electron microscopy image
  - 4
  - 1
  -
* - 3
  - Electron microscopy image
  - 1
  - 1
  -
* - 4A
  - Light microscopy image
  - 1
  - 4
  - Time
* - 4B
  - Light microscopy image
  - 1
  - 2
  - Channel
* - 4C
  - Light microscopy image
  - 1
  - 3
  - Channel
* - S2A
  - Light microscopy image
  - 1
  - 3
  - Time
* - S2B
  - Light microscopy image
  - 1
  - 3
  - Time
* - 5A
  - Light microscopy image
  - 4
  - 1
  -
* - 5B
  - Light microscopy image
  - 1
  - 3
  - Channel
* - 5C
  - Light microscopy image
  - 1
  - 3
  - Channel
* - 5D
  - Electron microscopy image
  - 1
  - 1
  -
* - 5E
  - Electron microscopy image
  - 1
  - 1
  -
* - S3A
  - Light microscopy image
  - 1
  - 3
  - Channel
* - S3B
  - Light microscopy image
  - 1
  - 3
  - Channel
* - S3C
  - Light microscopy image
  - 1
  - 3
  - Channel
* - S3D
  - Light microscopy image
  - 1
  - 3
  - Channel
* - S3E
  - Light microscopy image
  - 1
  - 3
  - Channel
* - S3F
  - Light microscopy image
  - 1
  - 3
  - Channel
* - S3G
  - Light microscopy image
  - 1
  - 3
  - Channel
* - S3H
  - Light microscopy image
  - 1
  - 3
  - Channel
* - S3I
  - Light microscopy image
  - 1
  - 3
  - Channel
* - 6A
  - Quantitative
  - 0
  - 0
  -
* - 6C
  - Quantitative
  - 0
  - 0
  -
* - Total
  - 
  - 45 images
  - 69 frames
```

---

# Stereotypical images cherry-picked from NucleusNet-10K

### Anaphase
```{image} ./figures/anaphase.png
:label: anaphase
```

### Telophase
```{image} ./figures/telophase.png
:label: telophase
```

---

# Autoencoders

## MNIST

```{code} python
:label: mnist-ae
:caption: Autoencoder model trained on MNIST digits

# ────────────────────────────────────────
# 2) Load & preprocess MNIST
# ────────────────────────────────────────
(x_train, y_train), (x_val, y_val) = tf.keras.datasets.mnist.load_data()
x_train = np.expand_dims(x_train.astype("float32") / 255.0, -1)
x_val   = np.expand_dims(x_val.astype("float32")   / 255.0, -1)

# ────────────────────────────────────────
# 3) Hyperparameters
# ────────────────────────────────────────
n_layers      = 2
base_filters  = 16
latent_dim    = 64
learning_rate = 3e-4
batch_size    = 32
epochs        = 100

AUTOTUNE = tf.data.AUTOTUNE
train_ds = (
    tf.data.Dataset
      .from_tensor_slices((x_train, x_train))
      .shuffle(10_000)
      .batch(batch_size)
      .prefetch(AUTOTUNE)
)
val_ds = (
    tf.data.Dataset
      .from_tensor_slices((x_val, x_val))
      .batch(batch_size)
      .prefetch(AUTOTUNE)
)

# ────────────────────────────────────────
# 4) Autoencoder
# ────────────────────────────────────────
# Encoder
inp = Input((28,28,1), name="encoder_input")
x = inp
for i in range(n_layers):
    f = base_filters * (2**i)
    x = Conv2D(f, 3, padding="same")(x)
    x = ReLU()(x)
    x = AveragePooling2D()(x)

flat = Flatten()(x)
z    = Dense(latent_dim, name="z")(flat)
encoder = Model(inp, z, name="encoder")

# Decoder
latent_in = Input((latent_dim,), name="z_sampling")
spatial = 28 // (2**n_layers)
channels = base_filters * (2**(n_layers-1))
x = Dense(spatial * spatial * channels)(latent_in)
x = Reshape((spatial, spatial, channels))(x)

for i in reversed(range(n_layers)):
    f = base_filters * (2**i)
    x = Conv2DTranspose(f, 3, strides=(2,2), padding="same")(x)
    x = ReLU()(x)

decoded = Conv2D(1, 3, padding="same", activation="sigmoid", name="decoder_output")(x)
decoder = Model(latent_in, decoded, name="decoder")

ae = Model(inp, decoder(encoder(inp)), name="autoencoder")
ae.compile(
    optimizer=Adam(learning_rate=learning_rate),
    loss="mse",
    metrics=["mse"],
)
```

## NucleusNet

```{code} python
:label: nucleus-ae
:caption: Autoencoder model trained on NucleusNet

# ────────────────────────────────────────────────────────────────────────
# 4) Autoencoder
# ────────────────────────────────────────────────────────────────────────
latent_dim    = 512
learning_rate = 3e-4

inp = Input((256,256,1), name='encoder_input')
x = inp
for filters in [16, 32, 64, 128]:
    x = Conv2D(filters, 3, padding='same')(x); x = ReLU()(x)
    x = Conv2D(filters, 3, padding='same')(x); x = ReLU()(x)
    x = AveragePooling2D()(x)

flat = Flatten()(x)
z = Dense(latent_dim, name='z')(flat)
encoder = Model(inp, z, name='encoder')

latent_in = Input((latent_dim,), name='z_sampling')
x = Dense(16 * 16 * 128)(latent_in)
x = Reshape((16, 16, 128))(x)
for filters in [128, 64, 32, 16]:
    x = Conv2DTranspose(filters, 3, strides=2, padding='same')(x); x = ReLU()(x)
    x = Conv2D(filters, 3, padding='same')(x); x = ReLU()(x)

decoded = Conv2D(1, 3, padding='same', activation='sigmoid', name='decoder_output')(x)
decoder = Model(latent_in, decoded, name='decoder')

ae = Model(inp, decoder(encoder(inp)), name='autoencoder')
ae.compile(optimizer=Adam(learning_rate), loss='mse', metrics=['mse'])
```