# IAR_Support_For_MSDK
The repository holds all the files necessary to add device specific support into [IAR's Embedded Workbench IDE](https://www.iar.com/products/architectures/arm/).

To add these files to your IAR Embedded Workbench installation, follow these steps:

1. Clone this repository and copy the contents to your IAR installation folder.  (The default installation location is C:\Program Files\IAR Systems\Embedded Workbench x.x.)
2. Clone the [MSDK repository](https://github.com/Analog-Devices-MSDK/msdk).
3. Open IAR Embedded Workbench.
4. Select **Tools->Configure Custom Argument Variables...**.
5. Select the **Workspace** tab.
6. Select **Add Variable...**.
7. Set the **Name** of the variable to **\_MSDK_BOARD\_**.
8. Set the **Value** of the variable to match the type of board for which you will be building projects. (Use **EvKit_V1** if uncertain.) The value should match one of the folders found in the Libraries/Boards/<Part_Name> folders of the MSDK repository.  See the [Board Support Packages documentation](https://analog-devices-msdk.github.io/msdk/USERGUIDE/#board-support-packages) for more details.
9. Select **OK** to add the variable.
10. Select the **Global** tab.
11. Select **Add Variable...**.
12. Set the **Name** of the variable to **\_MSDK_DIR\_**.
13. Set the **Value** of the variable to the location where you cloned the MSDK repository in Step 2.
14. Select **OK** to add the variable.
15. Select **OK** to dismiss the *Configure Custom Arguments Variables* window.

Support for Analog Devices' line of MAX32xxx microcontrollers will now be available in your IAR Embedded Workbench installation.  You will need to add the **_MSDK_BOARD_** variable (steps 4 through 9) for each new workspace you create.  

## Devices Currently Supported
* MAX32690
