# MLURL Machine Learning Malicious URL Detection
MLURL is a machine learning based URL analyser written in Python3 that can be used to detect malicious URLs.

## Important Information:
* Due to restrictions with access to Google Safebrowsing API, please do not run the mlurl.py with the -g (generate dataset) option during evaluation. The API only allows for a maximum of 10,000 requests per 24 hours. 
* Using mlurl.py with the -g option will take approximately between 2-3 hours due to feature extraction.
* mlurl.py -g can be used if you sign up to Google Cloud and use your own API key. 

## Features:
* Analyses and Extracts features from URLs to determine if a file is malicious or not.
* Features include: Entropy, Bag Of Words, Contain IP address, URL Length, Special Characters, Suspicious Strings, Number Of Digits, Populatiry and Google Safebrowsing verdict.
* The selected features are both static and external.   
* Cross-Analyse results with Virus Total.

## Install:
```
git clone https://github.com/callumlock/MLRD-Machine-Learning-Ransomware-Detection.git

cd MLRD-Machine-Learning-Ransomware-Detection

sudo pip3 install -r requirements.txt

## Usage

### Basic Usage:
python3 mlrd.py 'FILE TO ANALYSE'

### Usage with Reputation Checking:
python3 mlrd.py 'FILE TO ANALYSE' -v

python3 mlrd.py 'FILE TO ANALYSE ' -t

python3 mlrd.py 'FILE TO ANALYSE' -z

python3 mlrd.py 'FILE TO ANALYSE' -vtz

### Display Extracted Features for Input File:
python3 mlrd.py 'FILE TO ANALYSE' -d

### Open Survey:
python3 mlrd.py -s

### Display Help Information:
python3 mlrd.py -h