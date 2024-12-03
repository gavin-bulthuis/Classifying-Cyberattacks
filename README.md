# Cybersecurity Events Analysis

## Authors

- [@kevint4890](https://www.github.com/kevint4890)
- [@gavin-bulthuis]
- []
- []

## Data source

- [Kaggle UNSW_NB15](https://www.kaggle.com/datasets/mrwellsdavid/unsw-nb15/data?select=UNSW_NB15_training-set.csv)
  * srcip: Source IP address
  * sport: Source port number
  * dstip: Destination IP address
  * dsport: Destination port number
  * proto: Transaction protocol
  * state: Indicates the state and its dependent protocol (e.g., ACC, CLO, CON, ECO, ECR, FIN, INT, MAS, PAR, etc.)
  * dur: Record total duration
  * sbytes: Source to destination transaction bytes
  * dbytes: Destination to source transaction bytes
  * sttl: Source to destination time-to-live value
  * dttl: Destination to source time-to-live value
  * sloss: Source packets retransmitted or dropped
  * dloss: Destination packets retransmitted or dropped
  * service: Type of service (e.g., http, ftp, smtp, ssh, dns, ftp-data, irc, or "-" for less common services)
  * sload: Source bits per second
  * dload: Destination bits per second
  * spkts: Source to destination packet count
  * dpkts: Destination to source packet count
  * swin: Source TCP window advertisement value
  * dwin: Destination TCP window advertisement value
  * stcpb: Source TCP base sequence number
  * dtcpb: Destination TCP base sequence number
  * smeansz: Mean of the flow packet size transmitted by the source
  * dmeansz: Mean of the flow packet size transmitted by the destination
  * trans_depth: Represents the pipelined depth into the connection of HTTP request/response transaction
  * res_bdy_len: Actual uncompressed content size of the data transferred from the server's HTTP service
  * sjit: Source jitter (in milliseconds)
  * djit: Destination jitter (in milliseconds)
  * stime: Record start time
  * ltime: Record last time
  * sintpkt: Source inter-packet arrival time (in milliseconds)
  * dintpkt: Destination inter-packet arrival time (in milliseconds)
  * tcprtt: TCP connection setup round-trip time (sum of synack and ackdat)
  * synack: TCP connection setup time (time between SYN and SYN_ACK packets)
  * ackdat: TCP connection setup time (time between SYN_ACK and ACK packets)
  * is_sm_ips_ports: Indicates if source and destination IP addresses and port numbers are the same (1 if true, otherwise 0)
  * ct_state_ttl: Count of connections for each state according to specific TTL ranges
  * ct_flw_http_mthd: Count of flows using HTTP methods such as GET and POST
  * is_ftp_login: Indicates if the FTP session includes user and password authentication (1 if true, otherwise 0)
  * ct_ftp_cmd: Count of flows with an FTP command in the session
  * ct_srv_src: Count of connections with the same service and source address in the last 100 connections
  * ct_srv_dst: Count of connections with the same service and destination address in the last 100 connections
  * ct_dst_ltm: Count of connections with the same destination address in the last 100 connections
  * ct_src_ltm: Count of connections with the same source address in the last 100 connections
  * ct_src_dport_ltm: Count of connections with the same source address and destination port in the last 100 connections
  * ct_dst_sport_ltm: Count of connections with the same destination address and source port in the last 100 connections
  * ct_dst_src_ltm: Count of connections with the same source and destination addresses in the last 100 connections
  * attack_cat: Name of each attack category (e.g., Fuzzers, Analysis, Backdoor, etc.)
  * label: Binary label indicating whether the record is normal (0) or part of an attack (1)


## Overview


The main models implemented are:
- **Model**
- **Model**
- **Model**

Model Descriptions

## Results Summary
- **Model:**
  - Training Accuracy: 
  - Test Accuracy: 
  - F1 Score: 
  - 

- **Model:**
  - Training Accuracy: 
  - Test Accuracy: 
  - F1 Score: 
  - 

- **Model:**
  - Training Accuracy: 
  - Test Accuracy:
  - F1 Score: 
  - 

## Data Preprocessing
- 

## Features
- **Feature:**
  - 
- **Feature:**
  - 
- **Feature:**
  - 

## Model Evaluation
Models are evaluated using several metrics:
- Accuracy: Measures how often the model is correct.
- F1 Score: Balances precision and recall, useful for handling imbalanced data.
- ROC AUC: Assesses the model's ability to distinguish between classes.

## Conclusion

