# m3e-small-api

m3e-small Embeddings api by FastAPI

> Refer to **bge-api**


## 1. 拉取模型

```python
python
>>>from huggingface_hub import snapshot_download
>>>snapshot_download(repo_id="moka-ai/m3e-small",cache_dir="./cache", local_dir="models/m3e-small")
```
## 2. 选择1：本地运行
```sh
pip install -r requirements.txt
python main.py
```
## 2. 选择2：构建Docker镜像
```sh
docker build -t bge-m3-api .
```
CPU
```sh
docker run -d --name m3e-small-api -p 6008:6008 m3e-small-api
```
GPU
```sh
# required nvidia-docker2
docker run -d --name m3e-small-api --gpus all -p 6008:6008 m3e-small-api
```
