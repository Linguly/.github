# Setup Ollama for BasicModel

One of the easiest way to host an open source model and connect to Linguly is to host a model from Ollama library in Coolify.

## How to?

### 1. Download and Run a Model Using Ollama

1. Add ollama-with-open-webui in Coolify resources to a docker network same as your Linguly service.
1. Go to the terminal and connect to ollama api
1. Use the following command to download a desired model: `ollama pull llama3.2:3b`
    1. To check the result you can use `ollama list`
    1. If you want to run and test the model in terminal: `ollama run llama3.2:3b`


## For Local Tests

You can install ollama locally from [here](https://ollama.com/download) and then `pull` a model similarly.
