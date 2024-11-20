<a name="oben"></a>

<div align="center">

|[:skull:ISSUE](https://github.com/frankyhub/Raspi-TensorFlow/issues?q=is%3Aissue)|[:speech_balloon: Forum /Discussion](https://github.com/frankyhub/Raspi-TensorFlow/discussions)|[:grey_question:WiKi](https://github.com/frankyhub/Raspi-TensorFlow/wiki)||
|--|--|--|--|
| | | | |
|![Static Badge](https://img.shields.io/badge/RepoNr.:-%2089-blue)|<a href="https://github.com/frankyhub/Raspi-TensorFlow/issues">![GitHub issues](https://img.shields.io/github/issues/frankyhub/Raspi-TensorFlow)![GitHub closed issues](https://img.shields.io/github/issues-closed/frankyhub/Raspi-TensorFlow)|<a href="https://github.com/frankyhub/Raspi-TensorFlow/discussions">![GitHub Discussions](https://img.shields.io/github/discussions/frankyhub/Raspi-TensorFlow)|<a href="https://github.com/frankyhub/Raspi-TensorFlow/releases">![GitHub release (with filter)](https://img.shields.io/github/v/release/frankyhub/Raspi-TensorFlow)|
|![GitHub Created At](https://img.shields.io/github/created-at/frankyhub/Raspi-TensorFlow)| <a href="https://github.com/frankyhub/Raspi-TensorFlow/pulse" alt="Activity"><img src="https://img.shields.io/github/commit-activity/m/badges/shields" />| <a href="https://github.com/frankyhub/Raspi-TensorFlow/graphs/traffic"><img alt="ViewCount" src="https://views.whatilearened.today/views/github/frankyhub/github-clone-count-badge.svg">  |<a href="https://github.com/frankyhub?tab=stars"> ![GitHub User's stars](https://img.shields.io/github/stars/frankyhub)|
</div>



# Raspi-TensorFlow
Objekterkennung mit TensorFlow 

## Story
TensorFlow ist ein Framework mit dem u. a. auch Objekterkennung möglich ist. Das Repo eschreibt den Aufbau mit einem Raspberry Pi 5.

## Hardware

| Anzahl | Bezeichnung | 
| -------- | -------- | 
|  1 | Raspi5 8GB Starter Kid  |
| 1  | Micro SDXC Karte 64GB 140MB/s! (opt.)  |
|  1 |  RASP CAM AI Raspberry Pi - Kamera, KI (AI), 12MP  |
|  1 |  RASP SHD AI 26 Raspberry Pi Shield - AI (KI) 26 TOPS, Raspberry Pi 5 (opt.)  |
| 1  | USB Maus   |
| 1  | USB Tatsatur   |
|  1 |Monitor 10“ mini HDMI Type C   |
|  1 |  HDMI Kabel (mini HDMI Type C Stecker -> micro HDMI (Raspi) Type D Stecker) |
|  1 |   HDMI -> HDMI mini Adapter (opt.) |
| ---  | ---   |

![Bild](/pic/raspi5.png)
### Raspberry Pi 5 mit RASP SHD AI und RASP CAM Ai
---

![Bild](/pic/camera1.png)
### RASP CAM Ai am Raspberry Pi 5
---

![Bild](/pic/hdmi.png)
### HDMI Kabel
---

## Raspi in Betrieb nehmen
Der Raspi wir ohne Betriebssystem geliefert. Der erste Schritt nach den Anschluss von Maus, Tastatur, Bildschirm und Netzteil ist das Aufspielen des Betriebssystems auf die micro SDXC Karte.
Der einfachste Weg ist den Raspi mit dem Router zu verbinden. Der Installationsvorgang startet dann automitisch.

![Bild](/pic/flash1.png)

![Bild](/pic/flash2.png)

Das Raspi Betriebssystem lässt sich auch mit einem Imager istallieren. Dazu wird z.B. der Raspberry Pi Imager verwendet.

https://www.raspberrypi.com/software/

![Bild](/pic/Flash10.png)

![Bild](/pic/Flash11.png)

![Bild](/pic/Flash12.png)

![Bild](/pic/Flash13.png)

![Bild](/pic/Flash14.png)


## Kamera Test

```sh
libcamera-still -o test.jpg
```
---

## TensorFlow object detection von github installieren


```sh
sudo apt -get update
sudo apt -get upgrade

sudo apt install python3-tflite-runtime libatlas-base-dev

mkdir tLite 
cd tLite
ls
git clone https://github.com/tensorflow/examples --depth 1

cd examples
cd lite
cd examples
ls
cd object_detection
cd raspberry_pi
ls                            
sh setup.sh

```

---

<div style="position:absolute; left:2cm; ">   
<ol class="breadcrumb" style="border-top: 2px solid black;border-bottom:2px solid black; height: 45px; width: 900px;"> <p align="center"><a href="#oben">nach oben</a></p></ol>
</div>  

---






