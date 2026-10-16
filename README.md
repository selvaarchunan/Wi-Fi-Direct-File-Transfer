# Wi-Fi Direct File Transfer

A lightweight browser based file sharing application for transferring files between connected devices using PeerJS and WebRTC.

## Overview

Wi-Fi Direct File Transfer provides a simple interface for connecting two browser sessions and sharing files without uploading them to a conventional file hosting service.

The application includes device pairing, drag and drop file selection, chunk based transfers, progress indicators and file downloads.

Demo-https://selvaarchunan.github.io/Wi-Fi-Direct-File-Transfer/

## Features

- Peer to peer browser connections using PeerJS
- Short device IDs for pairing
- Drag and drop file selection
- Support for different file types
- Chunk based file transfers using 64 KB chunks
- Real time sending and receiving progress
- Download links for received files
- Dark interface with responsive styling
- No application backend required for file storage

## Technologies Used

- HTML5
- CSS3
- JavaScript
- PeerJS
- WebRTC DataChannels
- Browser File API and Blob API

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/wifi-direct-file-transfer.git
```

### 2. Open the project

```bash
cd wifi-direct-file-transfer
```

### 3. Run the application

Open `index.html` in a modern browser, or serve it through a local HTTP server:

```bash
python -m http.server 8000
```

Visit `http://localhost:8000`.

Open the application on two devices or in two browser sessions, enter the receiving device's ID and connect before sending files.

## Deployment

You can publish the static application using GitHub Pages.

1. Push the project to GitHub.
2. Open the repository settings.
3. Select Pages.
4. Choose the deployment source and branch.
5. Save the settings and open the published URL.

## Important Notes

- PeerJS uses a signalling service to establish connections. An internet connection is generally required for the default configuration.
- Direct peer to peer data transfer does not mean the application works exclusively over Wi-Fi or requires no internet.
- Network restrictions and firewall settings may affect connectivity.
- Large file transfers consume browser memory because the current receiver stores chunks until the file is complete.
- The current implementation should be tested and hardened before production use, especially for connection failures, large files and untrusted incoming filenames.

## Future Improvements

- Multiple file selection
- Multiple simultaneous transfers
- Improved large file handling
- Transfer cancellation and retry support
- Connection error handling
- Stronger pairing and peer validation
- Transfer history and clearer status messages

## Licence

Choose an appropriate open source licence before distributing or modifying this project. See the `LICENSE` file for the terms that apply.

## Disclaimer

This project is intended for learning, experimentation and personal file sharing. Review the security and reliability of the implementation before using it with sensitive data.
