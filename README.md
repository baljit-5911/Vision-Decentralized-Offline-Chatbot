# RAG-Based Offline Multi-Model Vision Chatbot with Decentralized Data

![first_screen](https://github.com/jot-s-bindra/Vision-Decentralized-Offline-Chatbot/assets/112833146/a2a65527-dfcc-4a6a-a037-8e7f75d48291)
![inference](https://github.com/jot-s-bindra/Vision-Decentralized-Offline-Chatbot/assets/112833146/20866aa0-2c67-4426-8f8c-8b6bcab0ed05)<!-- Add an image to represent your project -->

## Overview

This project hosts a fully offline multiModel -chatbot built on the Retrieval-Augmented Generation (RAG) model that even runs on CPU. It incorporates blockchain technology for decentralized data storage, enabling secure and private interactions. The bot is designed to accept text prompts and images, utilizing a multimodal architecture to enhance language understanding.

Main feature is we havent used vision LLM but used multiple models which have allowed us to do this image task with text llm too,Multimodel architecture is shown in the photo given below.

Used thresholding to guide and manage multiple Models

## Multi-Model Architecture
![chatbot](https://github.com/jot-s-bindra/Vision-Decentralized-Offline-Chatbot/assets/112833146/19271f00-8d8a-437f-b967-9ebc02b83625)
## Features

- **Offline Chatbot**: Utilizes the RAG architecture for conversational AI.
- **Blockchain Data Storage**: Ensures decentralized and secure data handling.
- **Vision Integration**: Accepts images as prompts for interactions.Used MultiModel approach to include images as well in the prompt
- **Fine-Tuning**: Its easier to fine tune as you can fine tune or apply the vgg model only for your suitable task which is a lot easier and computationally inexpensive than fine tuning LLM.
- **Parameters**: Despite Using Multiple Models,Parameters are still lowers 7.6B model comprising all parameters of all the models .
- **Streamlit Hosted**: The bot is deployed using Streamlit for easy access.

## Architecture

The chatbot employs a multimodal architecture, harnessing the capabilities of various models:
- **LLama2-7b-chat-ggml**: Enhances language understanding.
- **VGG16 Fine-tuned on RAG Data**: Enables vision-based interactions.
- **Salesforce/blip-image-captioning-large**: Facilitates image captioning.
- **CLIP-ViT-L-14**: Encoder to map both image and text to same vector space.


## Setup

### Clone Repository and Install Dependencies

1. Clone the repository:

    ```bash
    git clone https://github.com/your-username/your-repo.git
    cd your-repo
    ```

2. Install dependencies:

    ```bash
    pip install -r requirements.txt
    ```
  ### Pull Docker Image

  Alternatively, you can pull the Docker image from [jotsbindra/offlinemultimodelvisionchatbot](https://hub.docker.com/r/jotsbindra/offlinemultimodelvisionchatbot):

```bash
docker pull jotsbindra/offlinemultimodelvisionchatbot
```

### Download Required Models

1. Download the `llama2-7b-chat-ggml` model.[Download llama-2-7b-chat.ggmlv3.q8_0.bin](https://huggingface.co/TheBloke/Llama-2-7B-Chat-GGML/blob/main/llama-2-7b-chat.ggmlv3.q8_0.bin)

2. Run the `VGGTransferLearning.ipynb` notebook to generate `vgg16.h5`.

3. Place both the `llama2-7b-chat-ggml` model and `vgg16.h5` inside a folder named `models` in the root directory of the project.

### Run the Streamlit App

After downloading the necessary models:

```bash
streamlit run app.py
```

## Contributing

Contributions are welcome! If you want to contribute to this project, follow these steps:
1. Fork this repository.
2. Create a new branch (`git checkout -b feature/improvement`).
3. Make modifications and commit changes (`git commit -am 'Add feature/improvement'`).
4. Push the changes to your branch (`git push origin feature/improvement`).
5. Create a pull request.

