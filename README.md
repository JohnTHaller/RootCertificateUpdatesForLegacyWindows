# Root Certificate Updates For Legacy Windows (Vista, XP, 2000)

![GitHub Release](https://img.shields.io/github/v/release/JohnTHaller/RootCertificateUpdatesForLegacyWindows)
![GitHub Downloads (all assets, all releases)](https://img.shields.io/github/downloads/JohnTHaller/RootCertificateUpdatesForLegacyWindows/total)
![GitHub License](https://img.shields.io/github/license/JohnTHaller/RootCertificateUpdatesForLegacyWindows)
![GitHub Repo stars](https://img.shields.io/github/stars/JohnTHaller/RootCertificateUpdatesForLegacyWindows)

Older versions of Windows no longer update their Trusted Root Certification Authorities, resulting in HTTPS connection errors in browsers and applications. This project allows a user to manually update the root and intermediate certificates to the current versions used in modern Windows to fix these errors. The certificates for [Let's Encrypt](https://letsencrypt.org/) are also included. The package will be updated about every 3 months.
## Downloading the Certificates
Head to this project's [Releases](https://github.com/JohnTHaller/RootCertificateUpdatesForLegacyWindows/releases) and download WindowsRoot.sst and WindowsIntermediate.sst from the most current release. Save them to your Desktop or Downloads directory for use in the next step.
## Installing the Certificates
1. Open your Control Panel in Windows. This is within the Start Menu on Windows XP and Vista. It's within the Start Menu's settings section on Windows 2000.
2. Open Internet Options. If you have the newer friendly style Control Panel enabled, click Network and Internet and then Internet Options.
3. Open the Certificates window by selecting the Content tab and then clicking the Certificates button.
4. Select the Trusted Root Certification Authorities tab. You may have to use the left and right arrow buttons to see all tabs.
5. Click Import, click the Next button, click Browse and browse to the directory you saved your certificates to.
6. Change the file filter in the lower right of the window from X.509 or similar to Microsoft Serialized Certificate Store and then select the WindowsRoot.sst file and click OK.
7. Click Next, then Next, then Finish.
8. Click OK to each warning for each certificate and then OK again once the import was successful.
9. Select the Intermediate Certification Authorities tab in the Certificates window
10. Click Import, click the Next button, click Browse and browse to the directory you saved your certificates to.
11. Change the file filter in the lower right of the window from X.509 or similar to Microsoft Serialized Certificate Store and then select the WindowsIntermediate.sst file and click OK.
12. Click Next, then Next, then Finish.
13. Reboot your system just to be safe.

You should now have access to all the standard certificates needed for most apps.

PFX files are also included for use on other operating systems like Android. They are password protected with a password of 12345, the same as on your luggage. (Note that they won't work with super older versions like Android 4.)
