# MBS

this bash script perform mint, burn and send automatically.<br>
[donations are welcome](https://cyberomanov.tech/WTF_donate), if you find this tool helpful.

## Installation

### One-line

1. Run the commands:
```
apt update && \
apt install bc wget -y && \
wget -O mbs.sh https://raw.githubusercontent.com/cyberomanov/ironfish-mbs/main/mbs.sh && \
chmod u+x mbs.sh
```
### Step-by-step

1. Install dependencies:
```
apt update && apt install bc wget -y
```
2. Download the script:
```
wget -O mbs.sh https://raw.githubusercontent.com/cyberomanov/ironfish-mbs/main/mbs.sh
```
3. Edit script permissions:
```
chmod u+x mbs.sh
```

## Execute

> You can open the code with `nano mbs.sh` and insert your email for future faucet requests. 
1. Run the script manually:
```
./mbs.sh
```
2. Be happy:
```
root@cyberomanov:~# ./mbs.sh 

Enter your email to stay updated with Iron Fish: test@gmail.com

faucet just added your request to the queue.

Creating the transaction: [████████████████████████████████████████] 100% s

/////////////////// [ MINT [ 3234 ] | SUCCESS | #1 ] ///////////////////

hash: 49dffa000b75389d578e2857ba3493624cf009abe73a698f58f96586efd2602e, status: pending.
hash: 49dffa000b75389d578e2857ba3493624cf009abe73a698f58f96586efd2602e, status: pending.
hash: 49dffa000b75389d578e2857ba3493624cf009abe73a698f58f96586efd2602e, status: unconfirmed.
hash: 49dffa000b75389d578e2857ba3493624cf009abe73a698f58f96586efd2602e, status: unconfirmed.
hash: 49dffa000b75389d578e2857ba3493624cf009abe73a698f58f96586efd2602e, status: confirmed.

Creating the transaction: [████████████████████████████████████████] 100% s

/////////////////// [ BURN [ 49% of 3325 = 1617 ] | SUCCESS | #1 ] ///////////////////

hash: eca1685af2673bf39305937cfb93f69792effaff58f98ea9e4ee7a01b90869ef, status: pending.
hash: eca1685af2673bf39305937cfb93f69792effaff58f98ea9e4ee7a01b90869ef, status: pending.
hash: eca1685af2673bf39305937cfb93f69792effaff58f98ea9e4ee7a01b90869ef, status: unconfirmed.
hash: eca1685af2673bf39305937cfb93f69792effaff58f98ea9e4ee7a01b90869ef, status: unconfirmed.
hash: eca1685af2673bf39305937cfb93f69792effaff58f98ea9e4ee7a01b90869ef, status: confirmed.

Creating the transaction: [████████████████████████████████████████] 100% s

/////////////////// [ SEND [ 95% of 1708 = 1615 ] | SUCCESS | #1 ] ///////////////////

hash: b461acfb72a81ecfa7c791f853be8acf8a61c1dc2f50e5acc7136cadfccfa0e4, status: pending.
hash: b461acfb72a81ecfa7c791f853be8acf8a61c1dc2f50e5acc7136cadfccfa0e4, status: pending.
hash: b461acfb72a81ecfa7c791f853be8acf8a61c1dc2f50e5acc7136cadfccfa0e4, status: unconfirmed.
hash: b461acfb72a81ecfa7c791f853be8acf8a61c1dc2f50e5acc7136cadfccfa0e4, status: unconfirmed.
hash: b461acfb72a81ecfa7c791f853be8acf8a61c1dc2f50e5acc7136cadfccfa0e4, status: confirmed.

assetId: c9b46622e3de4d46aaeda9610a98db8cbcc5e5596a19793f10eb41ae0824c712.

balance of $IRON: 4.99999978.
balance of $cyberomanov: 838.00000000.

with love by @cyberomanov.
```

## Crontab
1. Update crontab:
```
apt update && apt install cron --reinstall
```
2. Open crontab editor:
```
crontab -e
```
3. Set one of rules or create your own. Use [crontab.guru](https://crontab.guru/), if you like one-liners:
> With this settings script will be executed twice a day at 06:10 and 18:10 o'clock and all output will be logged into `/root/mbs.log`.
```
10 6,18 * * * bash /root/mbs.sh >> /root/mbs.log
```
