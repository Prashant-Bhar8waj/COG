
  # Cog: Containers for machine learning

**What is Cog?**

* *It is an open-source tool that lets you package machine learning models in a standard, production-ready container. You can deploy your packaged model to your own infrastructure.

* Cog is a tool in the Machine Learning Tools category of a tech stack.

**Cog Integrations**

[![](images/py.png)](https://stackshare.io/python)
[![](images/docker.png)](https://stackshare.io/docker)
[![](images/redis.png)](https://stackshare.io/redis)
[![](images/amazon.png)](https://stackshare.io/python)
[![](images/linux.png)](https://stackshare.io/linux)
[![](images/macos.png)](https://stackshare.io/macos)

**Cog's Features**

* Docker containers without the pain
* No more CUDA hell
* Define the inputs and outputs for your model with  
* standard Python
* Automatic HTTP prediction server
* Automatic queue worker
* Cloud storage
* Ready for production

## How it works

Define the Docker environment your model runs in with `cog.yaml`:

```yaml
build:
  python_version: "3.10"
  python_packages:
    - torch==1.12.1
    - torchvision==0.13.1
    - timm==0.6.7
predict: "predict.py:Predictor"
```

Now Run
```
cog run python
```

Now, you can run predictions on this model:

```
$ cog predict -i @input.jpg
--> Building Docker image...
--> Running Prediction...
--> Output written to output.jpg
```
