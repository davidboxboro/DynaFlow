# DynaFlow

This repository contains the code and data set for the defense described in the following paper:

[DynaFlow: An Efficient Website Fingerprinting Defense Based on Dynamically-Adjusting Flows](http://people.csail.mit.edu/devadas/pubs/wpes18.pdf)

David Lu, Sanjit Bhat, Albert Kwon, Srinivas Devadas 

### Setup  
1. Clone this repo: ```git clone https://github.com/davidboxboro/DynaFlow```
2. Inside, make sub-directories called ```choices``` and ```batches```.
3. Inside ```batches```, run 
   ```shell
   wget "http://people.csail.mit.edu/kwonal/batch-primes.zip"
   unzip batch-primes.zip
   ```
   to download our data set and unzip it to the folder ```batch-primes``` inside ```batches```.  

### Usage
1. To re-create the defense results of our paper, run ```python dynaflow.py```. This will run all the configurations of the defense in both the open- and closed-world, creating the defended traces. The condensed version of each defended trace will be saved to the ```choices``` folder. The defense results will be saved to ```dynaflow.results```.
2. Run ```python optimal_closed.py``` and ```python optimal_open.py``` to attain the metrics of the optimal attacker on each defended data set. 
4. To run Wang et al.'s [k-NN](https://www.cse.ust.hk/~taow/wf/attacks/) and Hayes et al.'s [k-FP](https://github.com/jhayes14/k-FP), download their attacks and follow their documentation.  
5. To run other configurations of your choice, change the parameters at the bottom of ```dynaflow.py```. Make sure the paths at the bottom of ```optimal_closed.py``` and ```optimal_open.py``` correspond with those found in ```dynaflow.py```. 

## Contact
davidlu (at) mit.edu

sanjit.bhat (at) gmail.com

kwonal (at) mit.edu

Any discussions, suggestions, and questions are welcome!
