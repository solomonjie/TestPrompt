# Install Embedding Service:  
**Command:** docker run -p 8080:80 --name embeddingservice --pull always ghcr.io/huggingface/text-embeddings-inference:cpu-1.7 --model-id BAAI/bge-large-en-v1.5  
**Model Name:** BAAI/bge-large-en-v1.5  
**Inference Service:** ghcr.io/huggingface/text-embeddings-inference:cpu-1.7  
**Support Model URL:** https://huggingface.co/docs/text-embeddings-inference/supported_models  

# Test Via HttpRequest
![image](https://github.com/user-attachments/assets/527a6d14-e982-487b-b85e-4f68b1990e08)

# Python Code:  
You can install it via pip as pip install --upgrade --quiet huggingface_hub, and then run:
```
from huggingface_hub import InferenceClient  
client = InferenceClient()  
embedding = client.feature_extraction("What is deep learning?", model="http://localhost:8080/embed")  
print(embedding)
```
