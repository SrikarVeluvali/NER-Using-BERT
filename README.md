# OCR Entity Extraction with BERT by Srikar Veluvali

This project implements an Optical Character Recognition (OCR) system combined with a fine-tuned BERT model for entity extraction. The objective is to extract text from images and classify entities within that text, allowing for efficient data extraction from visual sources.

## Overview

The project leverages PaddleOCR for text extraction from images and uses BERT (Bidirectional Encoder Representations from Transformers) for classifying the extracted text into predefined entities. This two-step process enables high accuracy and efficiency in recognizing and categorizing information.

## High-Level Architecture

The architecture consists of the following components:

1. **Image Input**:
   - Users provide images containing text, typically URLs pointing to images.

2. **OCR Processing**:
   - PaddleOCR is utilized to extract text from images. This component handles different orientations and styles of text, making it robust for varied image inputs.

3. **Data Processing**:
   - The extracted text is cleaned and pre-processed to be suitable for training the BERT model. This includes tokenization and alignment with corresponding entity labels.

4. **Entity Classification**:
   - A fine-tuned BERT model is trained on the processed dataset. BERT's architecture allows it to capture context and relationships in the text, enabling accurate classification of entities based on the extracted text.

5. **Output Generation**:
   - The final output includes the predicted entity values associated with the extracted text, allowing for downstream applications like data analysis or integration into larger systems.

## Project Workflow

1. **Data Collection**:
   - A dataset is created containing images and their corresponding entities. This involves manual labeling or using existing datasets.

2. **Text Extraction**:
   - Using PaddleOCR, text is extracted from each image. Error handling ensures robustness in the face of potential issues like network errors or image quality problems.

3. **Model Training**:
   - The extracted text, along with entity labels, is fed into a BERT model for training. The model learns to associate text patterns with specific entity classes through supervised learning.

4. **Evaluation and Fine-Tuning**:
   - The model's performance is evaluated using metrics such as accuracy and F1-score. Fine-tuning is performed based on these evaluations to improve results.

5. **Deployment**:
   - The final model is saved and can be deployed to make predictions on new images, providing a pipeline for ongoing entity extraction tasks.

## Challenges and Solutions

- **Image Quality**: Low-resolution images can hinder text extraction. The system was designed to handle various image qualities, with pre-processing techniques employed to enhance readability.
  
- **Entity Classification Complexity**: Different entities can have similar textual representations. BERT's contextual understanding helps mitigate this issue, but careful dataset preparation and model tuning were essential for optimal results.

## Future Work

Future iterations of this project could include:

- Expanding the dataset for more diverse entity recognition.
- Implementing additional features such as real-time processing of images via a web interface.
- Enhancing the model's capabilities with more complex entity types or multi-lingual support.

## Conclusion

This project demonstrates the powerful combination of OCR technology and advanced NLP models like BERT for effective entity extraction. It lays the groundwork for applications across various domains, such as data entry automation, document analysis, and more.

