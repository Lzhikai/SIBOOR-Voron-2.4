# Orange Pi 3 LTS Flashing Tutorial

## Requirements
1. Orange Pi 3 LTS
2. Balena Etcher ([available here](https://www.balena.io/etcher#download-etcher))
3. 16GB MicroSD Card
4. MicroSD Card Reader
5. The Siboor / 3D Geek Station Orange Pi Image ([available here](https://drive.google.com/drive/folders/1JxFueRhtbZx-joOI689f__3X_PxoVJvA?usp=sharing))

## Tutorial

### Flash the Micro SD Card

1. Install Balena Etcher and run the application as an administrator. Insert the MicroSD card into the MicroSD Card Reader.

2. Once open, Select "Flash from file"

    ![Balena Etcher 1!](https://github.com/Lzhikai/siboor-voron/blob/main/accessories/flashing%20OrangePi3%20LTS/images/Picture1.png "Balena Etcher 1")

3. Select the Siboor / 3D Geek Station Image file (1) and select `Open` (2)

    ![Balena Etcher 2!](https://github.com/Lzhikai/siboor-voron/blob/main/accessories/flashing%20OrangePi3%20LTS/images/Picture2.png "Balena Etcher 2")

4. After selecting the image, the image name will be displayed. Click `Select Target` in order to select the memory card to be burned. 

    ![Balena Etcher 3!](https://github.com/Lzhikai/siboor-voron/blob/main/accessories/flashing%20OrangePi3%20LTS/images/Picture3.png "Balena Etcher 3")

5. Select the memory card you want to burn the image too, it is imporant you pay attention at this point, if you select the wrong drive data may be irecoverable. Once the drive has been selected (1) press `Select (1)` (2)

    ![Balena Etcher 4!](https://github.com/Lzhikai/siboor-voron/blob/main/accessories/flashing%20OrangePi3%20LTS/images/Picture4.png "Balena Etcher 4")

6. Click the `Flash` Button.    
    
    ![Balena Etcher 5!](https://github.com/Lzhikai/siboor-voron/blob/main/accessories/flashing%20OrangePi3%20LTS/images/Picture5.png "Balena Etcher 5")

7. Your Micro SD card will start to Flash, it will display `Flashing...` followed by the percentage it is through the process. 

    ![Balena Etcher 6!](https://github.com/Lzhikai/siboor-voron/blob/main/accessories/flashing%20OrangePi3%20LTS/images/Picture6.png "Balena Etcher 6")

7. Once it has finished flashing, it will Validate the Flash was a success, it is advisable to let this process complete rather than pressing `Skip`. 

    ![Balena Etcher 7!](https://github.com/Lzhikai/siboor-voron/blob/main/accessories/flashing%20OrangePi3%20LTS/images/Picture7.png "Balena Etcher 7")

7. Once complete, it will say Flash Complete, you can now eject the Micro SD Card from the Micro SD Card Reader.  

    ![Balena Etcher 8!](https://github.com/Lzhikai/siboor-voron/blob/main/accessories/flashing%20OrangePi3%20LTS/images/Picture8.png "Balena Etcher 8")

8. Insert the MicroSD Card into your Orange Pi 3 LTS.

### Flash the MicroSD to the Orange Pi 3 LTS' Internal Flash (Optional)


1. If you need to write the system onto the onboard EMMC Flash on the Orange Pi 3 LTS. SSH into the Orange Pi 3 LTS, to do this you will need to know the Orange Pi 3 LTS' IP address, this is usually easiest to find by going to your router management page. 

    User: `klipper`  
    Password: `Klipper`

2. Enter the following command
    ```shell
    sudo nand-sata-install
    ```
    The following screen will load up  

    ![Balena Etcher 9!](https://github.com/Lzhikai/siboor-voron/blob/main/accessories/flashing%20OrangePi3%20LTS/images/Picture9.png "Balena Etcher 9")

    Enter your password `klipper`    
    
    ![Balena Etcher 10!](https://github.com/Lzhikai/siboor-voron/blob/main/accessories/flashing%20OrangePi3%20LTS/images/Picture10.png "Balena Etcher 10")

3.  nand-sata-install will open, select insure the option `2 - Boot from eMMC - system on eMMC` is selected and press enter. 

    ![Balena Etcher 11!](https://github.com/Lzhikai/siboor-voron/blob/main/accessories/flashing%20OrangePi3%20LTS/images/Picture11.png "Balena Etcher 11")

4.  Select `Yes`, Press Enter. 

    ![Balena Etcher 12!](https://github.com/Lzhikai/siboor-voron/blob/main/accessories/flashing%20OrangePi3%20LTS/images/Picture12.png "Balena Etcher 12")

5.  Select `Ext4`, Press Tab, Select `OK`, Press Enter. 

    ![Balena Etcher 13!](https://github.com/Lzhikai/siboor-voron/blob/main/accessories/flashing%20OrangePi3%20LTS/images/Picture13.png "Balena Etcher 13")

6.  Wait for the progress bar to finish.  

    ![Balena Etcher 14!](https://github.com/Lzhikai/siboor-voron/blob/main/accessories/flashing%20OrangePi3%20LTS/images/Picture14.png "Balena Etcher 14")
    ![Balena Etcher 15!](https://github.com/Lzhikai/siboor-voron/blob/main/accessories/flashing%20OrangePi3%20LTS/images/Picture15.png "Balena Etcher 15")

7. Once the progress bar has finsihed, you will be prompted to power off the Orange Pi 3 LTS, select `Power Off` and once the Orange Pi has powered down, remove the Micro SD card.   

    ![Balena Etcher 16!](https://github.com/Lzhikai/siboor-voron/blob/main/accessories/flashing%20OrangePi3%20LTS/images/Picture16.png "Balena Etcher 16")  
    
### If this process has been successful, the next time you boot your Orange Pi 3 LTS, it will boot directly into the image. 
