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
  4. Post Message
  5. Return to home screen to see the effects
  - [ ] Affected source code:
    - ![Image of affected code](https://github.com/henryjr1/SecureSoftTesting/blob/Week-7/XSS_Attack.PNG)
1. (Required) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Required) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php) 

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [yyyy] [name of copyright owner]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
