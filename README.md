Copyright (C) 2020 - The Evolution X Project

Device tree for the Realme 6 (RMX2001, RMX2002 and RMX2003) - Realme 6S / Realme 6i India / Realme Narzo (RMX2002)
=================================================

The Realme 6 (codenamed _"RMX2001, RMX2002 and RMX2003"_) - Realme 6S / Realme 6i India / Realme Narzo (codenamed _"RMX2002"_) are mid-range smartphones from Realme.
They was released in March, June and July 2020.

This device tree commonize them as Realme G90T series (codenamed _"wasabi"_)

| Basic                   | Spec Sheet                                                                                                                     |
| -----------------------:|:------------------------------------------------------------------------------------------------------------------------------ |
| CPU                     | Octa-core                                                                                                                      |
| Chipset                 | Mediatek Helio G90T                                                                                                            |
| GPU                     | Mali-G76 MC4                                                                                                                   |
| Memory                  | 4/6/8 GB RAM                                                                                                                   |
| Shipped Android Version | 10.0                                                                                                                           |
| Storage                 | 64/128 GB                                                                                                                      |
| Battery                 | Non-removable Li-Po 4300 mAh battery                                                                                           |
| Display                 | 1080 x 2400 pixels, 20:9 ratio (~405 ppi density)                                                                              |
| Camera (Back)(Main)     | 64 MP, f/1.8, 26mm (wide), 1/1.72", 0.8µm, PDAF or 48 MP, f/2.0, 26mm (wide), 1/1.72", 0.8µm, PDAF                                                                                |
| Camera (Front)          | 16 MP, f/2.0, 26mm (wide), 1/3.06", 1.0µm                                                                                      |

## Device picture
![wasabi](https://cdn-files.kimovil.com/default/0004/34/thumb_333349_default_big.jpeg)


If built doesn't boot,Try the following steps.
cd frameworks/base/data/etc
nano privapp-permissions-platform.xml

And add the following lines before the last closing tag(</permissions>)

<privapp-permissions package="com.mediatek.ims">
        <permission name="android.permission.READ_PRECISE_PHONE_STATE"/>
        <permission name="android.permission.READ_NETWORK_USAGE_HISTORY"/>
        <permission name="android.permission.NETWORK_SIGNAL_STRENGTH_WAKEUP"/>
        <permission name="android.permission.PACKET_KEEPALIVE_OFFLOAD"/>
        <permission name="android.permission.UPDATE_DEVICE_STATS"/>
</privapp-permissions>
