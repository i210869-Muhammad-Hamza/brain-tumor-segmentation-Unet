# Brain-Tumor-Segmentation-Unet
![bt2](https://github.com/user-attachments/assets/58a8eb7f-ac81-45d1-a999-0636108bbb20)

Brain Tumor Segmentation Using U-Net Architecture

Introduction

Brain tumors are critical medical conditions that require precise diagnosis and treatment. Accurate segmentation of brain tumor regions from MRI images is essential for treatment planning, surgical interventions, and monitoring disease progression. This project aims to develop an automated brain tumor segmentation model using the U-Net architecture, which is well-suited for medical image analysis due to its ability to capture spatial features and contextual information.
Methodology
Data Collection and Preprocessing

    Data Sources: The dataset used for this project consisted of MRI scans of brain tumors sourced from publicly available medical imaging repositories. The dataset included a diverse range of tumor types and patient demographics.
    Data Preprocessing:
        Images were resized to a standard dimension (e.g., 128x128 pixels) to ensure uniformity across the dataset.
        Normalization was applied to scale pixel values to the range [0, 1].
        Masks for tumor regions were created, providing a binary representation of the tumor and non-tumor areas.

U-Net Model Architecture

    Model Selection: The U-Net architecture was chosen for its effectiveness in image segmentation tasks, particularly in medical imaging, where it excels in delineating structures from complex backgrounds.
    Architecture Design:
        The U-Net consists of a contracting path (encoder) that captures context through convolutional layers and pooling operations, followed by an expanding path (decoder) that enables precise localization through upsampling and skip connections.
        The model architecture included:
            Encoder blocks with convolutional layers, ReLU activation, and batch normalization.
            Max pooling layers for downsampling.
            Decoder blocks with transposed convolutions for upsampling and concatenation of features from the encoder path.
            A final output layer producing a binary segmentation map with a sigmoid activation function.

Model Training

    Training Setup:
        The model was compiled using the Adam optimizer and binary cross-entropy loss function, suitable for the segmentation task.
        Performance metrics included accuracy, precision, recall, and Dice coefficient to assess the model's ability to segment tumor regions accurately.
    Training Process: The U-Net model was trained using a GPU, employing techniques such as data augmentation (random flips, rotations, and shifts) to improve robustness. The training involved a batch size of 16 and a defined number of epochs.

Results

    High Accuracy: The model achieved an accuracy of over 97% on the validation dataset, demonstrating its effectiveness in accurately segmenting brain tumors.
    Visualization: Sample results displayed the original MRI images alongside the predicted segmentation masks, illustrating the model's ability to capture tumor regions accurately.
