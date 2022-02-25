# Intuiface-Badge-Scanning

## Purpose

To provide badge-scanning capability to interactive tradeshow content that allows the retrieval of user data stored on the cloud as well as session tracking for individual users across an Intuiface user experience. 

## Hardware

- Zebra DS457 Barcode Scanner

## Software

- [Intuiface](https://www.intuiface.com/)
- [Zebra DS457 USB CDC Driver](https://www.zebra.com/us/en/support-downloads/software/drivers/usb-cdc-driver.html)
- [Zebra SDK for Windows](https://www.zebra.com/us/en/support-downloads/software/developer-tools/scanner-sdk-for-windows.html)
- [123 Scan Utility](https://www.zebra.com/us/en/support-downloads/software/utilities/123scan-utility.html)

## Resources

- [ExpoTools API Documentation](https://ecomm.expotools.biz/su/api/documentation/expoleadsMobileExhibitor/)
- [Online API Testing](https://reqbin.com/)

## Procedure

### Installation

Install the USB CDC Driver. Then install the Zebra SDK and 123 Scan utility for windows (the SDK is not entirely necessary but it will later provides us with more capabilities under the hood). Run 123 Scan Utility and update the barcode scanner.

### Configuration

To keep the device from incorrectly scanning barcodes that are irrelevant, use 123 Scan Utility to create a new configuration for the device so that it only recognizes the symbology 'PDF417'. After saving the configuration, load to the device.

### Testing

You can use the Scan Utility or one of the SDK sample apps to scan a sample badge. Once the badge is scanned, the badge ID (typically at the beginning of the data) can be parsed and added to a get request with the Device ID and the Token to retrieve the user data connected to the device scanned.
