# Fine-Tuning a Pretrained LLM Model

## Introduction

### What is Fine-Tuning?
**Fine-tuning** is the process of taking a pre-trained language model and making it more specialized by training it further on a specific dataset. This allows the model to better understand and respond to the types of queries or tasks relevant to the new data. While preparing the dataset can be challenging, the actual fine-tuning process is relatively straightforward.

## Dataset Collection

For this project, I collected a public dataset from the **Correctional Service Department (CSD) of Hong Kong**. The dataset was formatted into structured data that the language model can train on, such as Question and Answer pairs.

## Fine-Tuning Process

I used the **LLaMA3** model and the **Unsloth** library to fine-tune the model. All the necessary code and explanations are available in my Google Colab notebook. [[Link to Google Colab](https://colab.research.google.com/drive/1QIFZjDFZUzxDt09uA-ZrwYCMmKNDcBv0?usp=drive_link))]

**Tools Used:**
- **LLaMA3**: A powerful language model for fine-tuning.
- **Unsloth**: A library to facilitate the fine-tuning process.

## Installation and Running the Model Locally

### Step 1: Install Git LFS
First, install Git LFS if havn't, just Google Git LFS and see how to install it.

After installation is installed, run the following code in the Directory where you installed Git LFS.
```bash
git lfs install
```
Then it should display:
```bash
Git LFS initialized
```

### Step 2: Git LFS Clone the model
Enter the following command to clone the model from hugging face.
```bash
git lfs clone https://huggingface.co/ZEGMEG/llama3-8b-qna-f16-gguf model
```
It will take a while.

### Step 3: Install Ollama and Create Model
If havn't installed Ollama yet, you can install Ollama on their webiste: https://ollama.com/

After installation, you can enter the following command to check installation is complete.
```bash
ollama -v
```

After installing Ollama, enter the following command to create the model.
```bash
ollama create llama3qna -f modelfile.txt
```
The modelfile.txt file can be found in the repository.

After creation is complete, you can see the newly created model by entering:
```bash
ollama list
```
And you should be able to see the model name "llama3qna".

### Step 4: Run the model
After all installation is done, we can now run the model by entering:
```bash
ollama run llama3qna
```
