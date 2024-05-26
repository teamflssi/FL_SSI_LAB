# Secure and Authenticated Federated Learning-based intelligent NIDS for smart healthcare 

The aim of this project is to propose an intrusion detection approach based on federated learning, fog computing and blockchain (in particular, self-sovereign identities). Stakeholders (local nodes and FogServer) are all registered on a blockchain where each receives a DID identifier.


I- Authentication phase


The blockchain issues credentials for local nodes, which are then verified by the FogServer, which acts as a verifier.



II- Model building


Once authentication has been successfully completed, the dataset is shared between the various nodes and a machine learning model is chosen. Each node performs the learning operations on its dataset locally and produces a submodel.


Finally, the Fog Server aggregates all the sub-models into a single model, which can then be deployed for production.

# requirements

- Ubuntu 18.04 LTS

- Docker

- Docker-compose

- Python 3.6.9



# Setup 


1- sudo iptables -I INPUT 4 -i docker0 -j ACCEPT


2- sudo firewall-cmd --permanent --zone=public --add-rich-rule='rule family=ipv4 source address=172.27.0.0/16 accept'



3- sudo firewall-cmd --permanent --zone=public --add-rich-rule='rule family=ipv4 source address=173.17.0.0/24 accept'



4- sudo firewall-cmd --reload

# run

1- Unzip 'sr1' and 'sr2' into 'src'

2- Copy the site-packages folder into the src_server folder


3- cd src/von-network



4- ./manage build



5- ./manage up 



6- cd src/src_server


7- add pour dataset (csv file) in "DatasetSource" folder 


8- docker-compose up


7- cd src/demo



8- ./run_simulation


NB: To change the model: 


Go to the src/demo/runners and src/src_server folders, edit the "load.py" file and uncomment the desired model;
Taking care to comment on those that are not being used (use only one model at a time).


# Google Colab



You can also enjoy the FL results on Google Colab. Here are the steps:


1- Unzip ipynb file 


2- Run


# Datasets

https://drive.google.com/file/d/1SrZWCqGB-2er3hYnD-lms8Xiyvf_3Cbl/view?usp=drive_link
https://drive.google.com/file/d/1MM93nkUFFv2aW58fZLynFiYy6wsJfB4T/view?usp=drive_link
https://drive.google.com/file/d/1-1ixx747opm1Km4xnbmml5i_jRpM7RAH/view?usp=drive_link
https://drive.google.com/file/d/1ik0Nf94siXtkg2Gc_ELJI2wGMgr8s_ah/view?usp=drive_link





The project uses the following resources:



VON Network (https://github.com/bcgov/von-network.git)



Hyperledger Aries Cloud Agent - Python  (https://github.com/hyperledger/aries-cloudagent-python.git)
