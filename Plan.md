# Plan

The goal of this is to generate an OpenSource equivalent to something like the [BearTooth(http://beartooth.com)

## OSI Layers

Layer 1/2

    SDR
      - CDMA Data:
        - Wifi: https://github.com/bastibl/gr-ieee802-11
	- FHSS/DSSS: https://github.com/DaulPavid/gr-spread
      - Location:
        - GPS: 
        - Plane location: Mode-S/ADS-B radio
        - Other?

Layer 2/3

    IPv6 (Neighbor Discovery using zeroconf)
    Meshed VPN
        tinc
            - tinc 1.1 Parameters: Ed25519 crypto public/private keypair, Neighbors
    MANET / OLSR
         - ProjectSPAN: https://github.com/ProjectSPAN
    mdns Neighbor Discovery?
        avahi (mdns zeroconf)

Layer 4/5

    Neighbor Discovery and Crypto
        Peergos w/ipfs.io: https://github.com/Peergos/Peergos/blob/master/README.md
            - Parameters: public/private keypair, unique random namespace

Layer 7

    Android
        Web (Cordova)
            - Map with self and neighbor location
                -  https://github.com/digidem/osm-p2p-db
            - WebRTC
                - Communicate with neighbors using text, voice, video
                - https://github.com/crosswalk-project/cordova-plugin-crosswalk-webview

## Hardware

For full-duplex SDR, the two primary contenders are:

 - Nuand BladeRF: https://github.com/Nuand/bladeRF
 - LimeSDR: http://www.limemicro.com/

Of these, LimeSDR looks like it will not ship in time (end of this month).

I have two Nuand BladeRF devices for developing and testing SDR. One with the amplifier, one without.
