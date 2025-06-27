## Our Code Workflow

Our code operates in the following structured manner:

1. **Use the TAU Urban Acoustic Scenes Dataset**  
   We start by using the [TAU Urban Acoustic Scenes 2022 Mobile Development dataset](https://www.kaggle.com/datasets/beautifulminnd/tau-urban-acoustic-scenes-2022-mobile-development ) from Kaggle.

2. **Generate a Custom Split**  
   Using the [`split25-audio-dataset-generator`](https://www.kaggle.com/code/mahdyr/split25-audio-dataset-generator/ ) notebook, we extract the desired audio split and save it as a new dataset:  
   👉 [DCASE 2025 Task1 Dataset](https://www.kaggle.com/datasets/mahdyr/dcase-2025-task1 )

3. **Convert Audio Files to Mel Spectrograms**  
   With the [`melspec-dataset-generator.ipynb`](https://www.kaggle.com/code/mahdyr/melspec-dataset-generator ) notebook, we convert all audio files into mel spectrograms in one go.

4. **Generate IR-Augmented Audio Samples**  
   In the [`augmented-audio-dataset-generator.ipynb`](https://www.kaggle.com/code/mahdyr/augmented-audio-dataset-generator ) notebook, we use:
   - The dataset created in Step 2 ([DCASE 2025 Task1](https://www.kaggle.com/datasets/mahdyr/dcase-2025-task1 ))
   - And the [MicIRP dataset](https://www.kaggle.com/datasets/mahdyr/micirp )  
   to generate impulse response (IR) augmented audio samples.  
   The resulting dataset is available here:  
   👉 [ImpulseResponse Audio Dataset](https://www.kaggle.com/datasets/hosseinsharify/impulseresponse-audio-dataset )

5. **Convert Augmented Audio to Mel Spectrograms**  
   Using the [`augmented-melspec-dataset-generator.ipynb`](https://www.kaggle.com/code/mahdyr/augmented-melspec-dataset-generator ), we convert all augmented audio files into mel spectrograms and store them in a new dataset:  
   👉 [DCASE 2025 Task1 MelSpecs Augmented](https://www.kaggle.com/datasets/mahdyr/dcase-2025-task1-melspecs-aug )

6. **Train the Models**  
   Finally, we perform model training using the following notebooks:
   - [`train-general-student.ipynb`](https://www.kaggle.com/code/mahdyr/train-general-student )
   - [`train-students.ipynb`](https://www.kaggle.com/code/mahdyr/train-students )
   - [`train-teachers.ipynb`](https://www.kaggle.com/code/mahdyr/train-teachers )  
   These utilize the datasets generated in Steps 3 and 5.
