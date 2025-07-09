# Day 15: WebRTC

## Introduction to WebRTC
WebRTC enables real-time communication between browsers.

### Basic WebRTC Setup
```javascript
// Create RTCPeerConnection
const pc = new RTCPeerConnection();

// Add local stream
navigator.mediaDevices.getUserMedia({
    video: true,
    audio: true
}).then(stream => {
    pc.addStream(stream);
});

// Handle incoming streams
pc.onaddstream = event => {
    const remoteVideo = document.getElementById('remote-video');
    remoteVideo.srcObject = event.stream;
};

// Create offer
pc.createOffer().then(offer => {
    return pc.setLocalDescription(offer);
}).then(() => {
    // Send offer to other peer
});

// Handle incoming offer
pc.setRemoteDescription(offer).then(() => {
    return pc.createAnswer();
}).then(answer => {
    return pc.setLocalDescription(answer);
}).then(() => {
    // Send answer to other peer
});
```

### WebRTC Features
- Video chat
- Audio chat
- Data channels
- Screen sharing
- Peer-to-peer communication

## Exercise
Create a real-time communication application that:
1. Implements video chat
2. Handles audio communication
3. Uses data channels
4. Implements signaling server
5. Handles multiple peers

Save your work as `exercise.html` in this folder.
