# Incorrect File URI Returned by Expo DocumentPicker on Android

This repository demonstrates a bug in the Expo DocumentPicker API on Android where the returned file URI is incorrect, preventing file access.

## Bug Description
When using `DocumentPicker.getDocumentAsync` on Android, the returned URI may not accurately reflect the file's location on the device's filesystem. This leads to errors when trying to access the file's contents, particularly when working with other libraries or APIs that expect a valid file path.

## Reproduction
1. Clone this repository.
2. Run the app on an Android device.
3. Select a file using the DocumentPicker.
4. Observe that attempting to access the file using the returned URI results in an error.

## Solution
The provided solution uses the `react-native-fs` library to obtain a valid file path from the URI returned by DocumentPicker. This allows for proper access and processing of the selected file.

## Technologies Used
* Expo
* React Native
* react-native-fs