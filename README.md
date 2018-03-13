# Project 7 -  WordPress vs. Kali

Time spent: **10** hours spent in total

> Objective: Find, analyze, recreate, and document **three to five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) [Stored XSS vulnerability](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-3438)
  - [ ] Summary: 
  By inserting a four bit character into a utf8 column you can force SQL to trunicate the character and everything after. Using this fact in combination with wordpress allowance of HTML tags you can insert an statement that will not properly close the HTML tags. You can then add your own on event elements to the site. 
    - Vulnerability types: Cross Site Scripting (XSS)
    - Tested in version: 3.9
    - Fixed in version: 4.1.2
  - [ ] GIF Walkthrough: ![Gif of exploit](https://github.com/henryjr1/SecureSoftTesting/blob/Week-7/XSS_Attack.gif)
  - [ ] Steps to recreate: 
  1.  Log in as administrator
  2. Create a new post
  3. Insert the following text:
  ```
  xss
  q cite='x onmouseover=alert(1) style=display:block;positions:fixed;width:100%;height:100%;tope:0; 𝌆'>
  ```
  4. Post message
  5. Return to home screen to see the effects
  - [ ] Affected source code:
    - ![Image of affected code](https://github.com/henryjr1/SecureSoftTesting/blob/Week-7/XSS_Attack.PNG)
2. (Required)  Persistent Cross-Site Scripting(https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2015-3440)
  - [ ] Summary: 
    - Vulnerability types: Cross Site Scripting (XSS)
    - Tested in version: 4.0
    - Fixed in version: 4.2.1
  - [ ] GIF Walkthrough: ![Gif of exploit](https://github.com/henryjr1/SecureSoftTesting/blob/Week-7/XSS_Attack2.GIF)
  - [ ] Steps to recreate: 
  1. Create a new comment
  2. Insert the following text:
  ```
  <a title='x onmouseover=alert(1) style=position:absolute;left:0;top:0;width:100%;height:100% [Insert 64 kb of text] '></a>
  ```
  4. Post message
  - [ ] Affected source code:
    - ![Image of affected code](https://github.com/henryjr1/SecureSoftTesting/blob/Week-7/XSS_Attack2.PNG)
3. (Required) Large File Upload XSS (https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-9061)
  - [ ] Summary: 
  When uploading a file larger than Wordpress 2mb limit javascript code can be executed from the filename because the error message interferes with script restrictions
    - Vulnerability types: Cross Site Scripting (XSS)
    - Tested in version: 4.0
    - Fixed in version: 4.7.5
  - [ ] GIF Walkthrough: ![Gif of exploit](https://github.com/henryjr1/SecureSoftTesting/blob/Week-7/XSS_Attack3.GIF)
  - [ ] Steps to recreate: 
  1. Download the [XSS3_Attack3.png]() or create a file larger than 2mb
  2. Ensure that the name is as follows
  ```
  Dinosaurs secret life<img src=x onerror=alert(1)>.png
  ```
  3. Navigate to http://wpdistillery.vm/wp-admin/media-new.php
  4. Drag the file into the upload box
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)

## Assets

Large image file for 3rd exploit ()

## Resources

- https://www.cvedetails.com/cve/CVE-2017-6814/
- https://cedricvb.be/post/wordpress-stored-xss-vulnerability-4-1-2/
- https://www.exploit-db.com/exploits/36844/
= https://hackerone.com/reports/203515

GIFs created with [Snagit](https://www.techsmith.com/screen-capture.html).

## Notes

Describe any challenges encountered while doing the work

