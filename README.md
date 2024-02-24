# m3e-small-api

m3e-small Embeddings api by FastAPI

> Refer to **bge-api**


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
