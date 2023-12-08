# RecketDroid: Red Packet Fraud Detection for Android Apps

## About
This repository stores our experimental code and datasets for the paper "RecketDroid: Red Packet Fraud Detection for Android Apps".
RecketDroid is the approach we proposed in this paper for automatically identifying red packets and detecting red packet fraud in Android apps. 

## Datasets
In the evaluation experiment, we use about 400 Android apps from Tencent Myapp Market, Anzhi Market and Google Play, of which 144 contain red packets.
In the wild experiment, we use over 1,000 Android apps from 7 app markets, including Google Play.
We provide these datasets in the "datasets" folder.

## Prerequisite

1. `Python` (2 or 3)
2. `Android SDK`
3. `Fiddler` (need to configure FiddlerScript)
4. `Baidu OCR API Key` (need to sign up)
5. `Virustotal API Key` (need to sign up)


## How to use

1. Connect a mobile device to your host machine via `adb`.

2. Configure the environment for `Fiddler` and your `mobile device` to listen to the app.

3. Configure `FiddlerScript` and run `Fiddler` tool in the background in advance.

4. Execute `loader_batch.py` file to dynamically explore the UI states and identify red packets.

5. Execute `detect_fraud.py` file in the `DetectFraud` directory to detect red packet frauds.

**Notice**
1. The `ExploreRecket/input` directory stores `.apk` files of the apps you want to analyze.
2. The `ExploreRecket/output` directory outputs the UTGs of apps, the generated network traffic and the downloaded apps.

## Acknowledgement

1. [Droidbot](https://github.com/honeynet/droidbot)