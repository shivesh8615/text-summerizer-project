# text-summerizer-project
This is an end to end nlp project to summerize text. This is a project build for DockerCon hackathon.
# Text Summarization Project

Sure, here is the README file in text file:


## Text Summarization Project

This project is a text summarizer using natural language processing (NLP) and the Hugging Face Transformers library. It is deployed using a Docker container and FastAPI.

### Requirements

* Python 3.7+
* Docker
* FastAPI

### Installation

1. Clone the project repository:

git clone https://github.com/shivesh8615/text-summerizer-project.git

2. Install the project dependencies:

cd text-summarizer-project
pip install -r requirements.txt

3. Build the Docker image:

docker build -t text-summarizer .

4. Run the Docker container:

docker run -p 8000:8000 text-summarizer

### Usage

To summarize a text, send a POST request to the `/summarize` endpoint with the following JSON body:

json
{
  "text": "The text to be summarized."
}
```

The API will return a JSON response with the following fields:

```json
{
  "summary": "The summarized text."
}
```

### Example

```python
import requests

response = requests.post(
  "http://localhost:8000/summarize",
  json={"text": "This is the text to be summarized."}
)

summary = response.json()["summary"]

print(summary)
```

### Output

```
This is the summarized text.
```

### Deployment

To deploy the project to production, you can use the following steps:

1. Build the Docker image:

docker build -t text-summarizer .

2. Push the Docker image to a Docker registry:

docker push <docker-registry>/text-summarizer

3. Deploy the Docker image to a production environment:

docker run -d -p 80:80 <docker-registry>/text-summarizer

Once the project is deployed, you can access the API at the following URL:

http://<host-address>:80/summarize

### Contributing

If you would like to contribute to this project, please feel free to open a pull request.

### License

This project is licensed under the MIT License.
```
# End to end Text-Summarizer-Project

## Workflows
1. Update config.yaml
2. Update params.yaml
3. Update entity
4. Update the configuration manager in src config
5. update the conponents
6. update the pipeline
7. update the main.py
8. update the app.py 
