# Cybersecurity Events Analysis

## Authors

- [@kevint4890](https://www.github.com/kevint4890)
- []
- []
- []

## Data source

- [Kaggle UNSW_NB15](https://www.kaggle.com/datasets/mrwellsdavid/unsw-nb15/data?select=UNSW_NB15_training-set.csv)
  id: A unique identifier for each record.
  dur: Duration of the connection or session (in seconds or milliseconds).
  proto: Protocol used in the communication (e.g., TCP, UDP, ICMP).
  service: Type of network service accessed (e.g., HTTP, FTP, DNS).
  state: Connection state (e.g., INT for internal, FIN for finished, etc.).
  spkts: Number of source packets sent during the session.
  dpkts: Number of destination packets received during the session.
  sbytes: Total bytes sent by the source.
  dbytes: Total bytes received by the destination.
  rate: Data transfer rate (in bytes per second or packets per second).
  sttl: Source Time-to-Live value (network layer hop count limit).
  dttl: Destination Time-to-Live value.
  sload: Source load (e.g., bits per second sent).
  dload: Destination load (e.g., bits per second received).
  sloss: Number of packets lost by the source.
  dloss: Number of packets lost by the destination.
  sinpkt: Time between two packets sent by the source.
  dinpkt: Time between two packets received by the destination.
  sjit: Jitter in packet delivery from the source.
  djit: Jitter in packet delivery to the destination.
  swin: Source TCP window size.
  stcpb: Source TCP sequence number.
  dtcpb: Destination TCP sequence number.
  dwin: Destination TCP window size.
  tcprtt: TCP round-trip time.
  synack: Time between SYN and ACK packets.
  ackdat: Time between ACK and data packets.
  smean: Mean packet size sent by the source.
  dmean: Mean packet size received by the destination.
  trans_depth: Depth of the HTTP request/response transaction.
  response_body_len: Length of the HTTP response body.
  ct_srv_src: Count of connections to the same service from the source.
  ct_state_ttl: Count of connections with the same state and TTL.
  ct_dst_ltm: Count of connections to the same destination in the last minute.
  ct_src_dport_ltm: Count of connections from the same source and destination port in the last minute.
  ct_dst_sport_ltm: Count of connections to the same destination port in the last minute.
  ct_dst_src_ltm: Count of connections between the same source and destination in the last minute.
  is_ftp_login: Binary indicator (0/1) of whether the session included an FTP login.
  ct_ftp_cmd: Count of FTP commands during the session.
  ct_flw_http_mthd: Count of HTTP methods used during the session.
  ct_src_ltm: Count of connections from the same source in the last minute.
  ct_srv_dst: Count of connections to the same service at the destination.
  is_sm_ips_ports: Binary indicator (0/1) of whether source and destination ports are the same.
  attack_cat: Categorical label indicating the type of attack (e.g., Normal, DoS, Probe, etc.).
  label: Binary label (0 = Normal, 1 = Malicious) indicating whether the session was part of an attack.


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

