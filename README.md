# A sentiment analysis API

The application has been deployed as an API using heroku. It takes in a statement from the user and returns either of two values. Positive or negative.

Website link: https://sentiment-analysis-api-project.herokuapp.com/docs

## How to setup
* Import the libraries from requirements.txt <br />
It can be done by writing the following comand in the terminal <br />
```pip install -r requirements.txt```
* Run the main.py file to get the model and the tokenizer, one can tune the hyper-parameters as one wishes.
* Open the app.py file and run the following command in the CLI
```python -m uvicorn app:app --reload``` 
after which the application will be hosted on the local system and a URL will be provided 
* One can post the provided URL and observe the results on their own

## Approach
* As this was an NLP task one had to first clean the text and then find a way to embed them
* NLTK and regrex were used to clean the text and end up with the processed text
* The in-built keras tokenizer was used for embedding the words, one-hot encoding, BoW, word2vec were considered but they did not provide the desirable results
* As for the model, a bidirectional lstm model has been built with a dropout layer and a final layer with sigmoid activation for the task of binary classification
* FastAPI was used to make the restful API 
* Heroku was used for deployment 

## Results
* Accuracy -> 0.8939
* Precision -> 0.9007
* Recall -> 0.8874
* F1 score -> 0.8940

## Notes
* tensorflow-cpu has been put in requirements.txt instead of the traditional tensorflow as tensorflow contains packages for both GPU and CPU which causes the slug size to increase by a factor of lot. While running of local system consider installing tensorflow by running the following command ```pip install tensorflow``` if any issues are encountered. 


<footer> Thank you, for giving your valuable time to review my submission. </footer>

