# OCR Entity Extraction with BERT

This project combines Optical Character Recognition (OCR) using PaddleOCR with entity extraction via a fine-tuned BERT model. The goal is to extract text from images and classify entities based on that extracted text.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Data Preparation](#data-preparation)
- [Training](#training)
- [Prediction](#prediction)
- [Contributing](#contributing)
- [License](#license)

## Installation

To set up this project, clone the repository and install the required libraries.

```bash
git clone https://github.com/yourusername/repo-name.git
cd repo-name
pip install -r requirements.txt
```

Make sure to have the following installed:

- Python 3.x
- PaddleOCR
- Transformers
- PyTorch
- PIL (Pillow)
- Requests
- Pandas
- NumPy
- Scikit-learn

## Usage

### Extract Text from Images

You can extract text from images using the `extract_text_from_image` function, which takes an image URL as input. Here's a brief example:

```python
from your_module import extract_text_from_image

text = extract_text_from_image('https://example.com/image.jpg')
print(text)
```

### Train the Model

After extracting text, we have trained the BERT model for entity extraction.

```python
# Load your dataset
import pandas as pd
df = pd.read_csv('path/to/your/dataset.csv')

# Training code goes here
```

### Make Predictions

Once the model is trained, we can use it to make predictions on new text:

```python
from your_module import predict

predicted_value = predict(extracted_text, entity_name='item_weight')
print(f"Predicted Entity Value: {predicted_value}")
```

## Data Preparation

Ensure your dataset is formatted correctly. The dataset should contain these major fields:

- `image_link`: URLs of the images to extract text from.
- `entity_name`: Names of the entities you want to classify.
- `entity_value`: The actual values of those entities.

Example CSV format:

```csv
image_link,entity_name,entity_value
https://example.com/image1.jpg,item_weight,3.8g
```

## Training

The BERT model is fine-tuned on the extracted text with entity labels. You can adjust the number of epochs and batch size in the training loop as needed.

## Prediction

To predict entity values after training, use the `predict` function. It takes the extracted text and the entity name as inputs and returns the predicted value.

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
