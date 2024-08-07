# Budget Allocation and Tracking Using Blockchain
This is the blockchain based project which is used to do budget allocation and tracking.
You can search with purpose and details of transaction.

# SetUp Locally
1. Clone the repository by running ```git clone https://github.com/shandli123/budget-allocation-and-tracking```
2. Create and activate virtual env using
   ```
   python3 -m venv path/to/venv

   for Mac
   source path/to/venv/bin/activate

   for Windows
   venv\Scripts\activate
   ```
5. ```pip install flask, matplotlib, requests, mysql, mysql-connector-python, bitcoin, ecdsa.```
6. ```pip install -upgrade setuptools```
7. Set up your mysql creds here on line #138 in blockchain.py and node_5001.py
  ```
mydb = mysql.connector.connect(
      host="127.0.0.1",
      port = 3306,
      user="abc",
      passwd="****",
      database="blockchain"
  )
````
6. Run one node on port 5000 and other on 5001
  ```
    flask --app blockchain.py run 
    flask --app node_5001.py run --port 5001
 ```
7. You can also add node by adding it in nodes.json and add file for every added node change
   the port address in the file as well.
8. visit ```http://127.0.0.1:5000/home```

# Functionality

You can Login or Sign up on the portal, once done you must copy your private key to sign any transaction (**Keep safely**).
You can add transaction and then mine the block we use **proof of work** consensus mechanism to mine the block and add it to
the blockchain.You can view the transactions uptil now we only keep the longest chain if different nodes have different chains.
You can also track and visualize all the transactions using the search functionality. 
