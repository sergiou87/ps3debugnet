DEBUGNET FOR PS3
=================
 
 What does this do?
===================
 
  debugnet is a PS3 small library to debug your homebrew code over udp, it's based on debugnet for [PS Vita from bigboss](https://github.com/psxdev/debugnet).
  
  How do I use it?
==================

 1) Compile and install library and include file

  
  ```
  cd libdebugnet
  make
  make install
  ```
  
 2) Compile sample
  
  
  ```
  cd sample
  edit main.c and change your server ip and port to listen udp messages from PlayStation Vita
  make
  ```

 3) Open a terminal and execute (change port if you don't use 18194). It can be in osx, linux or if you have socat like tool on windows
   
  ```
  socat udp-recv:18194 stdout 
  ```
  
 4) Run debugnetsample.elf in your PS3 using ps3load and `make run`
 
 You will see in socat terminal window output from your PlayStation 3:
 
 ```
 debugnet initialized
 Copyright (C) 2010,2015 Antonio Jose Ramos Marquez aka bigboss @psxdev
 Copyright (C) 2020 Sergio Padrino Recio aka sergiou87
 This Program is subject to the terms of the Mozilla Public
 License, v. 2.0. If a copy of the MPL was not distributed with this
 file, You can obtain one at http://mozilla.org/MPL/2.0/.
 ready to have a lot of fun...
 [PS3][DEBUG]: Test debug level 1
 [PS3][ERROR]: Test error level 1
 [PS3][INFO]: Test info level 1
 ```
 
 5) ready to have a lot of fun :P


  Credits
===========================
  
  Special thanks goes to:
  
  - bigboss for doing debugnet for vita, and everyone else who made that possible
  
