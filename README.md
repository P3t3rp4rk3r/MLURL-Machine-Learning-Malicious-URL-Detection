# MLURL Machine Learning Malicious URL Detection
MLURL is a machine learning based URL analyser written in Python3 that can be used to detect malicious URLs.

## Evaluate using survey here:
https://www.surveymonkey.de/r/GNYBKM6

## Important Information:
* Due to restrictions with access to Google Safebrowsing API, please do not run mlurl.py with the -g (generate dataset) option during evaluation. The API only allows for a maximum of 10,000 requests per 24 hours. 
* Using mlurl.py with the -g option will take approximately between 2-3 hours due to feature extraction.
* mlurl.py -g can be used if you sign up to Google Cloud and use your own API key. 

## Features:
* Analyses and Extracts features from URLs to determine if a file is malicious or not.
* Features include: Entropy, Bag Of Words, Contain IP address, URL Length, Special Characters, Suspicious Strings, Number Of Digits, Populatiry and Google Safebrowsing verdict.
* The selected features are both static and external.   
* Correlate results with Virus Total.

## Install:
```
git clone https://github.com/callumlock/MLURL-Machine-Learning-Malicious-URL-Detection.git

cd MLURL-Machine-Learning-Malicious-URL-Detection

sudo pip3 install -r requirements.txt
```
## Usage

### Train Model:
```
python3 mlurl.py -t
```
### Basic Usage:
```
python3 mlurl.py -c 'URL TO ANALYSE'
```

### Usage with Reputation Checking:
```
python3 mlurl.py -c 'URL TO ANALYSE' -v
```

### Usage with new URL lists:
Update benign URL dataset.
```
python3 mlurl.py -b
```
Update malicious URL dataset.
```
python3 mlurl.py -m
```
### Usage to generate new dataset using updated URL lists.

Please read the important information section before using this option.
```
python3 mlurl.py -g
```
### Open Survey:
```
python3 mlurl.py -s
```

### Display Help Information:
```
python3 mlurl.py -h
```
## Test Data:
The program is trained using malicious URLs and URLs that have specifically been linked to ransomware.

Test data for the program can be found here:
* https://openphish.com/feed.txt
* https://ransomwaretracker.abuse.ch/blocklist/
* https://www.phishtank.com/
