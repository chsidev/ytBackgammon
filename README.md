[! [a] (docs / ytBackgammon-demo-4boards.png)] (https://www.ytani.net/ytbackgammon/movies/ytBackgammon-demo-4boards.mp4)

# ytBackgammon --Network Shared Backgammon Board

http://www.ytani.net:8080/ytbackgammon/

## Features

Unlike regular online battles and apps ...

Create an atmosphere like having a backgammon party at a cafe
I am aiming to reproduce it on the net.

Even with existing competition sites and apps
Can be displayed in 3D
Watching games
Chat
You can, but
I feel like I'm staying in a closed room
It's hard to get an atmosphere where everyone can enjoy playing together.
(Personal impression)

Therefore,
nearby
"Can you make others feel like they are playing?"
I thought.

At the same time, connect by video chat / voice chat,
Please enjoy while chatting.

* Multiple battles can be played on multiple boards at the same time.
* You can see and operate all the boards at the same time.
* Regarding operability, rather than strict rule check and efficiency
I intend to emphasize the reproduction of the usability of the actual board.
* You can rotate the board to see it from the perspective of either player.
* There is a mode that allows you to move freely, ignoring the rules. (For education / examination)
* You can "return" and "redo" as much as you like.
* You can change the design of the board.


## Operating environment

### Client: Web app

* Chrome browser for smartphones and PCs
(Please use the latest version as much as possible)

* Please use a network that is as fast and stable as possible.
(Video conferencing can be done without stress)

#### Precautions

* A time lag may occur due to the following factors.
  --Line quality
  --Performance of PC and smartphone
  --Chrome version
  
* If the display is corrupted, try reloading the browser.

### Server

* OS: FreeBSD, Linux
* Python3, flask, flask_socketio


## Usage

### 1. New game

[! [a] (docs / ytBackgammon-opening.png)] (https://www.ytani.net/ytbackgammon/movies/ytBackgammon-opening.mp4)


### 2. Doubling

#### 2.1 Double-> Take

[! [a] (docs / ytBackgammon-double.png)] (https://www.ytani.net/ytbackgammon/movies/ytBackgammon-double-accept.mp4)


#### 2.2 Double-> Resign

[! [a] (docs / ytBackgammon-double.png)] (https://www.ytani.net/ytbackgammon/movies/ytBackgammon-double-resign.mp4)


## 3. Score

The score is calculated automatically,
If you want to reset or fix it, you can do it manually.
! [score] (docs / ytbg-score1.png)


## ytBackgammon server

### 1. Install

Follow the steps below to copy "ytbg.sh" to $ {HOME} / bin.

1. Create Python3 venv directly under your home directory
`` `bash
user @ host: .... $ cd ~
user @ host: ~ $ python3 -m venv env1
`` ```

2. Create a git clone in env1
`` `bash
user @ host: ~ $ cd env1
user @ host: ~ / env1 $ git clone https://www.github.com/ytani01/ytBackgammon.git
`` ```

3. Run the installation script
`` `bash
user @ host: ~ / env1 $ cd ytBackgammon
user @ host: ~ / env1 / ytBackgammon $ ./setup.sh
`` ```

### 2. ytBackgammon server usage

`` `bash
ytbg.sh ~ / env1 -p {port number} -i {image directory name} {server ID}
`` ```

Port number: 5000 by default
Image directory name: relative pathname from `` static``
Server ID: A string to distinguish when multiple servers are started


### 3. Board Design

You can make your own design.
Please download the following file and refer to it.

* [Design template file (ZIP format)] (docs / images0.zip)

Image file save destination: `` ~ / env1 / ytBackgammon / static / `` directly under the directory


## A. References

### A.1 Flask + Webscoket

* [Flask-Socket-IO] (https://github.com/miguelgrinberg/Flask-SocketIO)
  -[WebSocket application with Flask-Socket IO] (https://qiita.com/nanakenashi/items/6497caf1c56c36f47be9)
  

### A.2 Javascript socket.io

* https://cdnjs.com/libraries/socket.io


### A.3 CSS

* [Easy with just CSS! How to make a hamburger menu] (https://saruwakakun.com/html-css/reference/nav-drawer)