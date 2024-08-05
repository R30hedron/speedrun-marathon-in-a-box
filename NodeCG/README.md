# NodeCG Initial Setup:
The following assumes installing NodeCG onto a Raspberry Pi

1) Set up the Raspberry Pi
2) Install [NodeCG](https://www.nodecg.dev/docs/installing) and the [nodecg-speedcontrol](https://github.com/speedcontrol/nodecg-speedcontrol) bundle

    ```bash
    nodecg setup ^1 #version 1.9.0; speedcontrol throws a fit with v2+ currently
    nodecg install speedcontrol/nodecg-speedcontrol
    ```

3) Install OpenSSL (This will be used for self-signing for Twitch logins)

    ```bash
    sudo apt install openssl
    ```

4) Set up a self-signed certificate using the following tutorial: https://devopscube.com/create-self-signed-certificates-openssl/

5) Add rootCA.crt to the approved certificates on the restream PC (both via Windows and via internet browser (Firefox, Chrome, etc.)

   NOTE: For OBS to see NodeCG, the certificate needs to be placed in the Trusted Root Certification Authorities certificiate store in the import wizard. If you do not trust yourself, who can you trust, right?

7) Add and/or modify `cfg/nodecg.json` with the ssl certificate:

    ```json
    ...
    "ssl": {
        "enabled": true,
        "keyPath": "path/to/server.key",
        "certificatePath": "path/to/server.crt",
    ...
    ```
8) Set up Twitch Integration

    a) [Create an application using the Twitch API](https://dev.twitch.tv/console/apps/create). Use `https://<hostname>:9090/nodecg-speedcontrol/twitchauth` as the OAuth redirect url.

    b) Modify `cfg/nodecg-speedcontrol.json` file with the relevant Twitch API tags:
   ```json
   ...
   "twitch": {
    "enabled": true,
    "clientID": "CLIENT_ID",
    "clientSecret": "CLIENT_SECRET",
    "redirectURI": "https://<hostname>:9090/nodecg-speedcontrol/twitchauth",
    "streamTitle": "Game: {{game}} - Category: {{category}} - Players: {{players}}",
    "streamDefaultGame": "Games + Demos",
    "ffzIntegration": false
  },
   ...
   ```


