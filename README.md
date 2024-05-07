# Set up steps ---->



Using custom embedding model
Have this values in `app/config/db_config.yaml`

```yaml
embedding_model:
  model_name: "BAAI/bge-large-en" # model name here : Optional if not given by default `all-MiniLM-L6-v2` will be used
  # model_dimensions: 1000 # optional: you can set it to anything, if not given application will use models default embedding dimention
```

## Qdrant server local set up

Pull the image: docker pull qdrant/qdrant

Run the image : docker run -p 6333:6333 qdrant/qdrant

UI of the created collections can be seen at : http://127.0.0.1:6333/dashboard

More info : https://qdrant.tech/documentation/guides/installation/

## MySQL local development setup

Download the XAMPP control panel and start the mysql server

Go to app/config/database.py and comment line 10 and uncomment line 7

## FastAPI setup

1. Create a virtualenv with requirements.txt
2. To run fastapi server locally type in the terminal

```
cd app
uvicorn main:app --reload
```
