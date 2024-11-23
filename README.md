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
|  -------- | -------- | 
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



|   | Raspberry Pi 4 | Raspberry Pi 5 | 
| -------- | -------- | --------|  	
|CPU	|Broadcom BCM2711|	Broadcom BCM2712|
| | Quad-core|	Quad-core|
| |64-bit @ 1.8 GHz	|64-bit @ 2.4GHz|
|GPU|	VideoCore VI @ 500 MHz|	VideoCore VII @ 800 MHz|
| |OpenGL ES 3.1, Vulkan 1.0	OpenGL ES 3.1, Vulkan 1.2|
|Display output|	2x Micro-HDMI	|2x Micro-HDMI|
| |4K @ 60Hz (single display)	|4K @ 60Hz (dual displays)|
|Memory|	LPDDR4-3200 SDRAM	|LPDDR4X-4267 SDRAM|
| |1GB, 2GB, 4GB or 8GB	|2GB, 4GB or 8GB|
|Network|	Wi-Fi, Bluetooth, Gigabit Ethernet	|Wi-Fi, Bluetooth, Gigabit Ethernet|
| |PoE enabled (with HAT)	|PoE enabled (with HAT)|
|USB ports|	2x USB 2.0|	2x USB 2.0|
| |2x USB 3.0 |	2x USB 3.0 @ 5Gbps|
|Other connectors	|40 pin GPIO header	|40-pin GPIO header|
| |2-lane MIPI DSI display port	|2-lane MIPI DSI display port|
| |2-lane MIPI CSI camera port	|2-lane MIPI CSI camera port|
| |Stereo audio and composite video port	|Stereo audio and composite video port|
|Storage	|Micro-SD card slot|	Micro-SD card slot|
| | |M.2 SSD support (with HAT)|
|Power requirements	|5V/3A via USB-C (15W)|	5V/5A via USB-C (27W)|
|Special features| – |		Power button|
| | | Real-time clock (RTC)|
| | |UART debug port|

			

### HDMI Kabel

Benötigtes HDMI Kabel: micro HDMI (Raspi) Type D -> mini HDMI Type C Stecker (Monitor)

![Bild](/pic/hdmi.png)

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

## Anaconda herunterladen

Versions-Kontrolle: https://repo.anaconda.com/archive/
 
```sh
mkdir tmp
cd /tmp
wget https://repo.anaconda.com/archive/Anaconda3-2024.10-1-Linux-aarch64.sh
```

## Anaconda installieren

```sh
bash Anaconda3-2024.10-1-Linux-aarch64.sh
```

Folge den Anweisungen auf dem Bildschirm (meistens mit Enter bestätigen und am Ende den Lizenzbedingungen mit yes zustimmen). 
Der Standardinstallationspfad ist normalerweise in deinem Home-Verzeichnis (/home/pi/anaconda3).

## Anaconda aktivieren

```sh
source ~/.bashrc
```

## Eine virtuelle Umgebung erstellen

```sh
export PATH="/home/raspberrypi/Anaonda3/bin:$PATH" to .bashrc
conda create --name tflite1 python=3.11.2
conda activate tflite1
```

## Installiere TensorFlow Lite

```sh
mkdir tfLite 1
cd tfLite1
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

## OpenCV installieren

```sh
sudo apt install python3-opencv
```


## Testen der Installation

Um sicherzustellen, dass TensorFlow Lite korrekt installiert wurde, kannst du ein einfaches Python-Skript verwenden, um die Installation zu überprüfen:

  ```sh
python

import tflite_runtime.interpreter as tflite

interpreter = tflite.Interpreter(model_path="dein_model.tflite")

interpreter.allocate_tensors()

print("TensorFlow Lite Interpreter wurde erfolgreich geladen!")

```



## Deaktivieren der Umgebung

```sh
conda deactivate
```

## Beispiele

https://github.com/sglvladi/TensorFlowObjectDetectionTutorial/tree/master/docs/source/auto_examples

---

<div style="position:absolute; left:2cm; ">   
<ol class="breadcrumb" style="border-top: 2px solid black;border-bottom:2px solid black; height: 45px; width: 900px;"> <p align="center"><a href="#oben">nach oben</a></p></ol>
</div>  

---






