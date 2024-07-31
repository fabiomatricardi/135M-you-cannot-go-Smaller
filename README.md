<img src='https://huggingface.co/datasets/HuggingFaceTB/images/resolve/main/banner_smol.png' width=800>

# 135M-you-cannot-go-Smaller
Repo of the code from the Medium article 135M: you cannot go Smaller



it is tested on Windows 11, with 16 GB RAM. Python 3.11+

#### Create VENV and Install dependencies
```
mkdir HFSmol_LM

cd HFSmol_LM
python -m venv venv

venv\Scripts\activate

deactivate

pip install streamlit==1.36.0 openai tiktoken
```

#### Dowmnload Llamafile
```
wget https://github.com/Mozilla-Ocho/llamafile/releases/download/0.8.12/llamafile-0.8.12 -OutFile llamafile-0.8.12.exe
```

#### Download the model in the `models` subfolder
```
mkdir models
cd models

wget https://huggingface.co/MaziyarPanahi/SmolLM-135M-Instruct-GGUF/resolve/main/SmolLM-135M-Instruct.Q8_0.gguf -OutFile SmolLM-135M-Instruct.Q8_0.gguf
```

### How to run
1. in one terminal window, even withouth the venv activated run
```
.\llamafile-0.8.12.exe --nobrowser --host 0.0.0.0 -m .\models\SmolLM-135M-Instruct.Q8_0.gguf -c 2048
```
2. in another terminal window, with the `venv` active, run
```
streamlit run st-SmoL135M-llamafile.py
```


<img src='https://github.com/fabiomatricardi/135M-you-cannot-go-Smaller/raw/main/smoLM135M.gif' width=800>




   
