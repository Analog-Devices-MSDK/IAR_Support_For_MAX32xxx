# IAR_Support_For_MSDK
The repository holds all the files necessary to add device specific support into IAR's Embedded Workbench IDE.

To add these files to your IAR Embedded Workbench installation, follow these steps:

1. Clone this repository and copy the contents to your IAR installation folder.  (The default installation location is C:\Program Files\IAR Systems\Embedded Workbench x.x.)
2. Clone the MSDK repository.
3. Open IAR Embedded Workbench.
4. Select Tools->Configure Custom Argument Variables...
5. Select the Global tab.
6. Select Add Variable...
7. Set the Name of the variable to "MSDK_PATH".
8. Set the Value of the variable to the location where you cloned the MSDK repository in Step 2.
9. Select OK to add the variable.
10. Select OK to dismiss the Configure Custom Arguments Variables window.

Support for Analog Devices line of MAX32xxx microcontrollers will now be available in your IAR Embedded Workbench installation.
