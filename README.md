Netgear RAX120v2 5G Aquantia firmware

* AQR-G3_v4.3.C-AQR_DNI_DR-EQ35AX8-R-prov1_ID23888_VER1311.cld

    firmware found in Netgear stock firmware V1.2.8.40 under '/lib/firmware/'. Suitable for
    loading using a linux usermode tool, e.g. [aq-fw-download](https://github.com/robimarko/nss-packages/tree/main/firmware/aq-fw-download)

* aqr_v4.3.C.mbn

    above *.cld file converted to be suitable for loading from u-boot. Converted calling the following:

    ```
    python2 mkheader.py 0x44000000 0x13 AQR-G3_v4.3.C-AQR_DNI_DR-EQ35AX8-R-prov1_ID23888_VER1311.cld aqr_4.3.C.mbn
    ```

* mkheader.py

    ```
    python 2 script to convert the stock firmware (TODO: where got it from?)
    ```
