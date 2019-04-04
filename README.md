# PeerServer for Heroku

This is a forked version of PeerServer from [PeerJS](https://peerjs.com/).
This repo contains minor changes (i.e. environment variables) and steps to deploy private PeerJS broker to Heroku app.

# Prerequisite

Make sure you have the `heroku-cli` installed and configured.

# Deploy to heroku

```bash
git clone https://github.com/kfwong/peerjs-server-heroku.git
heroku git:remote -a <your-heroku-app-id>
git push heroku master
```

Connecting to the server from PeerJS:

```html
<script>
    const peer = new Peer('someid', {
        host: '<your-heroku-app-domain>',
        port: 443,
        path: '/myapp',
        secure: true,
    });
</script>
```
