English-to-Spanish Neural Machine Translation

A neural machine translation model using an encoder-decoder LSTM architecture built with Keras to translate English sentences into Spanish using the Tatoeba dataset.

Project Structure





spa.txt : Dataset containing English-Spanish sentence pairs



translation_model.ipynb : Jupyter Notebook with full code



README.md : Project documentation

Dataset





Source: Tatoeba



Format: Tab-separated values (TSV)



Columns:





English sentence



Spanish translation



Metadata/comments



Notes: Used 124,596 pairs for training and 13,844 pairs for testing (total: 138,440 pairs)

Libraries Used





pandas



numpy



matplotlib



re



string



scikit-learn



tensorflow

Note: Keras is included in TensorFlow, so installing TensorFlow is sufficient.

Preprocessing Steps





Convert text to lowercase



Remove punctuation and digits



Normalize whitespace



Add special tokens: START_ and _END to Spanish sentences

Model Architecture





Type: Encoder-Decoder



Framework: TensorFlow (Keras)

Encoder





Embedding layer (dimension: 256)



Three stacked LSTM layers (each with 256 units)

Decoder





Embedding layer (dimension: 256)



One LSTM layer (256 units)



Dense layer with softmax activation

Notes:





Trained using teacher forcing



Uses padded sequences (max length: 70) and vocabulary indexing

Usage

Setup

pip install pandas numpy matplotlib scikit-learn tensorflow

Running the Notebook





Ensure spa.txt is in the project directory.



Open and run translation_model.ipynb cells in order.



Train the model from scratch or load pre-trained weights.



Use the prediction cells to translate sentences, ensuring vocabulary alignment and handling of START_ and _END tokens.

Corrections to Original README.md

Overview

The original README.md contained inaccuracies, particularly in the dataset size and model architecture details. These have been corrected based on the attached Jupyter Notebook to ensure accuracy and clarity for users.

Detailed Corrections

Dataset





Original: Used 50,000 pairs for training and testing



Correction: Used 124,596 for training, 13,844 for testing (138,440 total)



Explanation: The notebook shows the dataset is split into 124,596 training pairs and 13,844 testing pairs, totaling 138,440 pairs, not 50,000.

Model Architecture





Original: Encoder: Embedding layer, LSTM layer; Decoder: Embedding layer, LSTM layer, Dense layer



Correction: Encoder: Embedding layer (256), Three stacked LSTM layers (256 each); Decoder: Embedding layer (256), One LSTM layer (256), Dense layer



Explanation: The notebook specifies three stacked LSTM layers in the encoder and one in the decoder, with embedding dimensions of 256.

Libraries Used





Original: Includes separate install for keras



Correction: Note added: Keras included in TensorFlow, updated pip command



Explanation: Keras is part of TensorFlow, so installing TensorFlow is sufficient. The pip command was updated to exclude keras for clarity.

Usage





Original: Only pip install command



Correction: Added detailed instructions for running the notebook and predictions



Explanation: Expanded usage section to include steps for running the notebook, training, and making predictions, ensuring users can easily follow the process.

Summary of Changes







Section



Original Content



Correction/Change





Dataset Notes



Used 50,000 pairs for training and testing



Used 124,596 for training, 13,844 for testing (138,440 total)





Model Architecture



Encoder: Embedding layer, LSTM layer



Encoder: Embedding layer (256), Three stacked LSTM layers (256 each)





Model Architecture



Decoder: Embedding layer, LSTM layer, Dense layer



Decoder: Embedding layer (256), One LSTM layer (256), Dense layer





Libraries Used



Includes separate install for keras



Note added: Keras included in TensorFlow, updated pip command





Usage



Only pip install command



Added detailed instructions for running the notebook and predictions

Conclusion

The corrected README.md now accurately reflects the project's details as implemented in the notebook, addressing discrepancies in dataset size, model architecture specifics, and usage instructions. This ensures users have a clear and correct understanding of the project setup and execution.





Tatoeba Language Learning Platform
