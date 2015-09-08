nosnoop location tracker
=======================

A location tracker for devices of the privacy-conscious. Using P2P technology to ensure no central authority has access to anything and strong encryption
Stores encrypted device information in a peer-to-peer blockchain to prevent snooping by anyone; private investigators, Google, and the NSA included.

Client Node
----------

 - monitors status and ensures running properly
 - hides in **background** and stays invisible
   - cloak traffic as coming from something else?
 - registers message in blockchain periodically
   - every 5 minutes?
- use diffs
  - keep messages small
  - reject messages if no new data; add timestamp and empty message
  - calculate if it's about to be over the data limit and drop a message, if so, put the latest data in for those lost values as well
 - this client just has a basic api for control, via key-based commands. so you send a binary command to it, encrypted using the computer's pub key and signed using the controller private key

Web UI
------

 - runs completely in browser
 - local storage for data
 - give private key and unlock to start using

Key Server
----------

 - lastpass model
 - password to unlock account
 - send encrypted bundle (keys) to client
 - hash password + salt to unlock encrypted bundle
 - use password to unlock bundle
