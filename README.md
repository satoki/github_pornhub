# github_pornhub
👻 Phishing vulnerability in Android GitHub app.

![files/logo.png](files/logo.png)  
This page is a joke, but the vulnerability is real.  
The Android GitHub app can lead users to phishing sites.  
  
**This article has been published after getting permission from GitHub.**  

## Vulnerability

**🐛Android app (GitHub 1.12.0)**  
Since the URL of "Issue" has not been confirmed correctly, the link destination is different between the Android app and others.
It works fine when the user accesses the link on a non-Android device.
The user now trusts the link.
Links that users already trust when using the Android app act as evil links.
Attackers can direct users to phishing sites.

## PoC


**PoC is [https://github.com/satoki/github_pornhub/issues/1](https://github.com/satoki/github_pornhub/issues/1).**  

Browser -> GitHub login page  
Android app -> Pornhub login page  

```markdown

[Is it linked to the GitHub login page?](www.pornhub.com/../../../../../../../../../../login)

```

## Demo

### Browser -> GitHub login page
<img src="files/01.gif" alt="files/01.gif" width="378" height="798">  

### Android app -> Pornhub login page
<img src="files/02.gif" alt="files/02.gif" width="378" height="798">  
