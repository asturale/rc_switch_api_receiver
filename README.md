At work, where we care for people with mental disabilities and disorders, we use [these wireless buttons](https://seintje.nu/) to allow clients to request help during the night.
They are essentially simple wireless doorbells that operate at 433.92 MHz using OOK (On-Off Keying).
The receivers rely on an outlet for power, which means they cannot be carried around. This is not very practical, so we were looking for a solution that would allow help requests to be received on the professional's smartphone.
That's why I built this. I used ESPHome because it's quicker and easier to set up than developing custom firmware.

I use LoRa sx127x radio modules. I tried cheap 433Mhz receivers but the range was terrible.

## How to use

 - Configure secrets.yaml with Wifi credenials, API endpoint and authentication token
 - Ceck/configure your GPIO pins
 - Check/configure frequency, bandwith and modulation
 - Adjust protocol and code length
 - filter and idle parameters in remote_receiver might use some tweaking depending on your remotes.
 - Run:
```
$ esphome run rc_switch_api_receiver.yaml
```
