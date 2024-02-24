# m3e-small-api

m3e-small Embeddings api by FastAPI

> Refer to **bge-api**

## Quick Start

### CPU

```sh
docker run -d --name bge-large-api -p 6008:6008 jokerwho/bge-large-api:latest
```

### GPU

> required nvidia-docker2

```sh
docker run -d --name bge-large-api --gpus all -p 6008:6008 jokerwho/bge-large-api:latest
```

## Test

```sh
curl --location --request POST 'http://127.0.0.1/v1/embeddings' \
--header 'Authorization: Bearer sk-aaabbbcccdddeeefffggghhhiiijjjkkk' \
--header 'Content-Type: application/json' \
--data-raw '{
  "model": "m3e-small",
  "input": ["github是什么"]
}'
```

## Develop

```python
from huggingface_hub import snapshot_download
snapshot_download(repo_id="BAAI/m3e-small",cache_dir="./cache", local_dir="models/m3e-small")
print("======download successful=====")
```


```sh
pip install -r requirements.txt
python main.py
```
