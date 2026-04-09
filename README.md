# Blockchain Explorer Application

This is the enhanced source code for a custom blockchain application complete with an interactive Web UI, wallet tracking, and transaction validations with fees.

## Recent Enhancements

* **Web UI Dashboard:** An interactive Web UI built with Flask and Bootstrap 5 to view blocks and mempool.
* **Wallet Balances:** Tracks wallet balances dynamically while factoring in pending and confirmed transactions.
* **Transaction Validation:** Rejects outgoing transactions if the sender has insufficient funds.
* **Mining & Fees:** Transactions now support fees (`fee`). Miners are rewarded with the block base reward **plus** all transaction fees inside the mined block.

## Installation

1. Make sure [Python 3.6+](https://www.python.org/downloads/) is installed. 
2. Install [pipenv](https://github.com/kennethreitz/pipenv). 

```
$ pip install pipenv 
```
3. Install requirements  
```
$ pipenv install 
``` 

4. Run the server:
    * `$ pipenv run python blockchain.py` 
    * `$ pipenv run python blockchain.py -p 5001`
    * `$ pipenv run python blockchain.py --port 5002`

5. **Access the Web UI**: Once the application is running, open your web browser and navigate to exactly what port the application is running on (e.g. `http://localhost:5000` or `http://localhost:5001`). You can view the chain, check your balance, submit transactions with fees, and trigger the block mining directly from the browser!
    
## Docker

Another option for running this blockchain program is to use Docker.  Follow the instructions below to create a local Docker container:

1. Clone this repository
2. Build the docker container

```
$ docker build -t blockchain .
```

3. Run the container

```
$ docker run --rm -p 80:5000 blockchain
```

4. To add more instances, vary the public port number before the colon:

```
$ docker run --rm -p 81:5000 blockchain
$ docker run --rm -p 82:5000 blockchain
$ docker run --rm -p 83:5000 blockchain
```

## Installation (C# Implementation)

1. Install a free copy of Visual Studio IDE (Community Edition):
https://www.visualstudio.com/vs/

2. Once installed, open the solution file (BlockChain.sln) using the File > Open > Project/Solution menu options within Visual Studio.

3. From within the "Solution Explorer", right click the BlockChain.Console project and select the "Set As Startup Project" option.

4. Click the "Start" button, or hit F5 to run. The program executes in a console window, and is controlled via HTTP with the same commands as the Python version.


## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

