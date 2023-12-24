# 4dmGTFO
simple gtfo bins searching in the terminal

## install
```
git clone https://github.com/aslam4dm/4dmGTFO.git
pip install -r requirements.txt
```

## ease of use
```
chmod u+x
sudo cp 4dmgtfo.py /bin/4dmgtfo
```
now you can run `4dmgtfo` from any path

## usage
find if specified suid binaries can be leveraged to perform privilege escalation

### Single binary
```
python3 4dmgtfo.py --binary-name mount
python3 4dmgtfo.py -bn mount
```

### Binary list (in a file)
note: on a target machine, you can run the following command to find SUID files on the system: `find / -type f -perm -u=s -exec basename {} \; 2>/dev/null | sort`. Simply copy the results to a file on your local machine, then run `4dmgtfo`
```
python3 4dmgtfo.py --binary-file bins.txt
python3 4dmgtfo.py -bf bins.txt
```
