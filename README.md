# Seattle_Birds_Classification

## Overview

This project involves training neural networks to identify the sounds of birds common in the Seattle area. The dataset includes spectrograms derived from 10 MP3 sound clips of various lengths for each of 12 bird species. The goal is to build custom neural networks to predict which bird species made which sound based on these spectrograms.

## Project Components

### Data

The dataset for this project is based on bird sound clips from the Birdcall competition, originally sourced from Xeno-Canto, a crowd-sourced bird sound archive. The provided data includes:
- **Spectrograms:** Preprocessed images representing 2-second windows of bird calls, sized at 343 (time) x 256 (frequency) pixels.
- **Sound Clips:** Raw MP3 files of bird calls for 12 species, each with 10 clips of varying lengths.

### Models

1. **Binary Classification Model:** 
    - A neural network designed to classify between two selected bird species.
  
2. **Multi-Class Classification Model:** 
    - A neural network to classify between all 12 bird species in the dataset.
  
3. **Transfer Learning Model (Optional):** 
    - An additional model using transfer learning by adapting a pre-trained neural network for this task. This approach can help improve performance by leveraging pre-learned features from a similar task.

### Preprocessing

The data has been preprocessed to facilitate easier neural network training:
- **Subsampling:** The sound clips were subsampled to a sample rate of 22,050 Hz.
- **Segmentation:** Loud sections of the sound clips (>0.5 seconds) were segmented into 2-second windows where bird calls are detected.
- **Spectrogram Generation:** Each window was converted into a spectrogram, creating an "image" of the bird call.

You can choose to use either the raw sound clips or the preprocessed spectrograms for training your models.

### Discussions

- **Model Performance:** Document and compare the performance of different neural network structures and hyperparameters. Even if a model performs poorly, include comparisons and discussions about what was tried and why.
  
- **Challenges:** Discuss any limitations encountered during the project, such as long training times or difficulties in distinguishing certain bird species. Listen to the bird calls and examine the spectrograms to identify any patterns or characteristics that might explain these challenges.

- **Alternative Models:** Consider other models that could be used for this task and discuss why neural networks are appropriate for this application.

## Usage

To get started with the project:

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/sounds-of-seattle-birds.git
    ```
2. Navigate to the project directory:
    ```bash
    cd sounds-of-seattle-birds
    ```
3. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```
4. Explore the dataset and start training models using the provided Jupyter notebooks.

### Running Models

- **Binary Classification:** Run the binary classification notebook to build a model that classifies between two selected bird species.
  
- **Multi-Class Classification:** Use the multi-class classification notebook to train a model that can distinguish between all 12 bird species.
  
- **Transfer Learning (Optional):** Explore the transfer learning notebook to adapt a pre-trained model to this dataset.

## License

This project is licensed under the MIT License - see the `LICENSE` file for details.

## Acknowledgments

This project was developed as part of a coursework assignment, integrating concepts from a deep learning class. The dataset is derived from the Birdcall competition and Xeno-Canto, with additional preprocessing performed as part of this assignment.
