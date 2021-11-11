# docker-home
Files relating to docker services for home automation (and adjacent) services.


## MQTT Debugging
In some cases, you may need to sniff MQTT messages for debugging.
Pop a shell on the mosquitto container and use `mosquitto_sub`:

    docker exec -it mosquitto /bin/sh
    mosquitto_sub -t 'zigbee2mqtt/#' -v


## Secrets
Some files in this repository are GPG encrypted upon commit with `git-crypt`.
After cloning, use `git-crypt unlock` and enter the GPG key passphrase to decrypt.

To decrypt, make sure you've added a GPG key with `git-crypt add-gpg-user <GPG_KEY_ID>`.

More info [here](https://www.guyrking.com/2018/09/22/encrypt-files-with-git-crypt.html).

See `.gitattributes` for files here which are encrypted.  If it's not listed there,
it's fine.
