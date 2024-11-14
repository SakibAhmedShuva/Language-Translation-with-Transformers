# Language Translation with Transformers

This repository demonstrates how to perform language translation using Hugging Face's Transformers library. The implementation showcases translation between English and multiple target languages using pre-trained models.

## Overview

The project utilizes state-of-the-art transformer models to perform neural machine translation. Currently, it supports:
- English to German translation (using Google T5)
- English to Arabic translation (using Helsinki-NLP's OPUS-MT)

## Prerequisites

- Python 3.7+
- transformers library
- torch (PyTorch)

## Installation

1. Clone this repository:
```bash
git clone https://github.com/SakibAhmedShuva/Language-Translation-with-Transformers.git
cd Language-Translation-with-Transformers
```

2. Install required packages:
```bash
pip install transformers torch
```

## Usage

The main implementation is in the `translation_tf.ipynb` notebook. You can run it using Jupyter Notebook or Google Colab.

Example usage:
```python
from transformers import pipeline

# English to German translation
en_de_translator = pipeline('translation_en_to_de', model="google-t5/t5-base")
result = en_de_translator("Hello, my name is Jose. What is your name?")

# English to Arabic translation
en_ar_translator = pipeline('translation_en_to_ar', model="Helsinki-NLP/opus-mt-en-ar")
result = en_ar_translator("Hello, my name is Jose. What is your name?")
```

## Models Used

1. **Google T5 Base**
   - Task: English to German translation
   - Model ID: `google-t5/t5-base`

2. **Helsinki-NLP OPUS-MT**
   - Task: English to Arabic translation
   - Model ID: `Helsinki-NLP/opus-mt-en-ar`

## Features

- Easy-to-use interface using Hugging Face pipelines
- Support for multiple language pairs
- Jupyter notebook implementation
- Efficient translation using pre-trained models

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Hugging Face Transformers](https://huggingface.co/transformers/)
- [Google T5](https://github.com/google-research/text-to-text-transfer-transformer)
- [Helsinki-NLP](https://github.com/Helsinki-NLP)
