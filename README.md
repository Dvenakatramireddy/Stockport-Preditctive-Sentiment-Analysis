# Stockport-Preditctive-Sentiment-Analysis
### Twitter API
Before running this code, you will need make a devloper account on Twitter to get access to API keys needed to communicate with their API.

### Alpaca API
You will also need to make a stock trading account on Alpaca to get access to API keys needed to communicate to their API. If you want to use fake money, then be sure to make a "paper-trading" account.

### Saving Models and Outputs for Re-use
The program automatically saves the following files after training the model. You will need to generate the following files by initially training the model yourself by inputting "train_new_model" because the files containing my pre-trained models were too large to post on GitHub.

-   Neural network tensors: twitter_sentiment_model.pth   
-   Model outputs and predictions: twitter_sentiment_outcomes.csv   
### Running the Code
Run all cells in jupyter notebook. After training the model yourself for the first time, you may choose to input "p" to use your automartically saved pre-trained model or "train_new_model" to overwrite those files by training it yourself with new parameters.
Next, input whether you are running the code on Google Colab's GPU or locally on your own CPU. Google Colab's GPU is necessary for training the model initially. Subsequent runs can be done on your local CPU using your saved pretrained model. Running on Colab's CPU (instead of GPU) will throw an error, which can be handled by altering the code.

## Directory Structure
The data folder is the only sub-directory, and it contains the stock_data.csv file containing the 5790 tweets with labeled sentiment for training and testing the model.

The stock_trading_decisions.txt and portfolio_performance.txt exist in the folder for keeping track of the stock trades that have occured and the balance of the account.

The api_credentials.py file is where I kept my API credentials for secrecy. Another user can place their credentials in this file or they can instead be placed directly into the code.

The requirements.txt file contains the command line arguments necessary to install all of the necessary packages to run the main program. The main program will automatically read this file and install any packages not already installed on your computer. You do not need to manually install these packages.

The sentiment_model.ipynb is the main file that contains the entire NLP pipeline. It contains approximately 700 lines of code.
