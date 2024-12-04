# Cybersecurity Events Analysis

## Authors

- [@kevint4890](https://www.github.com/kevint4890)
- [@gavin-bulthuis](https://www.github.com/gavin-bulthuis)
- [@ivanfierros](https://github.com/ivanfierros)
- [@hamzaabdul23](https://github.com/hamzabdul23)

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
- **XGBoost**: A powerful gradient-boosting model known for its efficiency in classification tasks.
- **kNN**: A simple yet effective non-parametric classification algorithm that relies on feature similarity.
- **Random Forest**: An ensemble-based model that combines multiple decision trees to improve predictive performance.

Model Descriptions

## Results Summary
- **XGBoost:**
  - Training Accuracy: 97.28%
  - Test Accuracy: 89.73%
  - F1 Score: .90

- **kNN:**
  - Training Accuracy: 97.42%
  - Test Accuracy: 82.70%
  - F1 Score: .83

- **Random Forest:**
  - Training Accuracy: 99.58%
  - Test Accuracy: 88.28%
  - F1 Score: 0.88

## Data Preprocessing
The data preprocessing steps involved several key transformations to ensure data consistency and improve model performance:

  1. Removal of Unnecessary Columns:
      - Dropped columns like id (unique identifier) and attack_cat (secondary label) which were not required for modeling.
  2. Outlier Handling:
      * Clamped extreme values in numerical columns at the 95th percentile if they exceeded a threshold (10× median and >10).
  3. Log Transformation:
      * Applied log transformation to numeric columns with high cardinality to reduce skewness.
  4. Categorical Simplification:
      * Simplified categorical columns by grouping rare categories into a placeholder ('-').
  5. Encoding:
      * One-hot encoding was applied to categorical variables (proto, service, state) to convert them into numerical format.
  6. Feature Selection:
      * Used Chi-Square statistics to select the top 20 most important features for the pipeline.

## Model Evaluation
Models are evaluated using several metrics:
  * Confusion Matrix:
    * Visual representation of true positives, true negatives, false positives, and false negatives.
  * Accuracy:
    * Measures the overall correctness of the model.
  * Precision, Recall, and F1 Score:
    * Precision: Measures the proportion of correctly predicted positive observations.
    * Recall: Measures the ability of the model to capture all positive observations.
    * F1 Score: Harmonic mean of Precision and Recall, balancing both metrics.

## Conclusion
The results indicate that XGBoost outperformed the other models in terms of test accuracy and F1 Score, making it the most suitable model for this dataset. Random Forest also demonstrated strong performance but was slightly overfit on the training data. kNN, while simpler, had lower accuracy and F1 Score, likely due to its sensitivity to high-dimensional data.
