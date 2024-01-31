# IAR_Support_For_MSDK
The repository holds all the files necessary to add device specific support into [IAR's Embedded Workbench IDE](https://www.iar.com/products/architectures/arm/).

To add these files to your IAR Embedded Workbench installation, follow these steps:

1. Clone this repository and copy the contents to your IAR installation folder  (The default installation location is C:\Program Files\IAR Systems\Embedded Workbench x.x)
2. Clone the [MSDK repository](https://github.com/Analog-Devices-MSDK/msdk)
3. Open IAR Embedded Workbench
4. Create/Open a workspace within IAR
5. Select **Configure Custom Argument Variables...** from the **Tools** menu
6. Select the **Workspace** tab
7. Click on the **New Group...** button
8. Set the name of the group to **`ADI_VARS`**
9. Click the **OK** button to add the group
10. Click on the **Add Variable...** button
11. Set the **Name** of the variable to **`_MSDK_BOARD_`**
12. Set the **Value** of the variable to match the type of board for which you will be building projects. (Use **EvKit_V1** if uncertain.) The value should match one of the folders found in the _Libraries/Boards/<Part_Name>_ folders of the MSDK repository.  See the [Board Support Packages documentation](https://analog-devices-msdk.github.io/msdk/USERGUIDE/#board-support-packages) for more details.
13. Click the **OK** button to add the variable
14. Select the **Global** tab
15. Click on the **New Group...** button
16. Set the name of the group to **`ADI_VARS`**
17. Click the **OK** button to add the group
18. Click the **Add Variable...** button
19. Set the **Name** of the variable to **`_MSDK_DIR_`**
20. Set the **Value** of the variable to the location where you cloned the MSDK repository in Step 2
21. Click the **OK** button to add the variable
22. Click the **OK** button to dismiss the *Configure Custom Arguments Variables* window

Support for Analog Devices' line of MAX32xxx microcontrollers will now be available in your IAR Embedded Workbench installation.  You will need to add the `_MSDK_BOARD_` variable (steps 5 through 13) for each new workspace you create.  

## Devices Currently Supported
* MAX32690
