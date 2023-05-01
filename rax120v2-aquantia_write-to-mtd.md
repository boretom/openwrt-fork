- find ETHPHYFW partition (expected: /dev/mtd25)

    ```
    $ fgrep -i 'ethphyfw' /proc/mtd
    mtd25: 00080000 00020000 "ethphyfw
    ```

- copy aqr-v4.3.C.mbn to /tmp folder on OpenWrt router:

    ```
    $ scp aqr-v4.3.C.mbn 192.168.1.1:/tmp/
    ```

- write mbn file to appropriated mtd partition

    ``` 
    $ mtd write /tmp/aqr_v4.3.C.mbn /dev/mtd25
    Unlocking /dev/mtd25 ...

    Writing from /tmp/aqr_v4.3.C.mbn to /dev/mtd25 ...
    ```

