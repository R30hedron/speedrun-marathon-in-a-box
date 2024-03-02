# NodeCG Initial Setup:
The following assumes installing NodeCG onto a Raspberry Pi

1) Set up the Raspberry Pi
2) Install [NodeCG](https://www.nodecg.dev/docs/installing) and the [nodecg-speedcontrol](https://github.com/speedcontrol/nodecg-speedcontrol) bundle

```
nodecg setup ^1 #version 1.9.0; speedcontrol throws a fit with v2+ currently
nodecg install speedcontrol/nodecg-speedcontrol
```

3) Install OpenSSL (This will be used for self-signing for Twitch logins)
