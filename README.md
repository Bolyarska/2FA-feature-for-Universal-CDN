# 2FA feature for Universal CDN
Additional security feature for the login process at Universal CDN

> **Note**: Universal CDN is no longer in operation, but this repository showcases the two-factor authentication feature I developed during my time there. The logic of the feature is written in **PHP**.

The two-factor authentication feature can be used in 2 ways - with an authenticator app or with email. Only 1 of the authentication options can be enabled at a time, but you can switch between them at any time.

When enabled, an additional window shows up after logging in with username and password, where you must enter a 6-digit code.

The app option requires a QR scanning app (such as the Google authenticator). The code there changes every 30 seconds.
The email option works in a similar way, but sends the code to your registered email. The email code expires in 10 minutes.

A code can only be used once.

There's a brute-force defense system implemented. The login process is blocked for 3 minutes on:
- Every 3 unsuccessful login attempts from the same IP in the span of a minute.
- Every 10 unsuccessful login attempts from 10 different IPs in the span of 5 minutes.

  
[2fa_demo.webm](https://github.com/user-attachments/assets/9eae0ab0-b1a4-4f11-9435-da1048b5ba80)
