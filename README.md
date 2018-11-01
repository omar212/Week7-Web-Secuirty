# Week7-Web-Secuirty
# Project 7 - WordPress Pentesting

Time spent: **6** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) Vulnerability Name or ID: Authenticated Stored Cross-site scripting
  - [x] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: N/A
  - [x] GIF Walkthrough: 
     - <img src='Challenge 1 Video.gif' title='XSS' width='' alt='' />
  - [x] Steps to recreate: 
      - Create a new post called example, and then put the code```<a onmouseover= "alert('Gotta catch them all !')" >Click Me</a>``` in           the content link. Finally click link to show message in the preview of post. 
  - [x] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
2. (Required) Vulnerability Name or ID: Authenticated Stored Cross-Site Scripting via Image Filename
  - [x] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: N/A
  - [x] GIF Walkthrough: 
     - <img src='Challenge2 Video.gif' title='XSS' width='' alt='' />   
  - [x] Steps to recreate: 
      Go to create a new media, upload a picture from your laptop. Then copy & paste the following code
        ```
           filename<img src=a onerror=alert(1)>.png
        ```
  - [x] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
3. (Required) Vulnerability Name or ID: User Enumeration
  - [x] Summary: this vulnerablility will remote attackers to create a crafted image file name that will inject arbitrary web script. 
    - Vulnerability types: User Enumeration 
    - Tested in version: 4.2
    - Fixed in version: N/A
  - [x] GIF Walkthrough: 
    - <img src='Challenge 4 Video.gif' title='XSS' width='' alt='' />  
  - [x] Steps to recreate: 
       Go to the WordPress login page, first, check the input for admin with empty password,
       then it shows the error because the password is empty.Second, when you input admin as    username, and put password randomly.It            shows the password for admin is incorrect. When you put other name (ex.user), and random password, it shows error. 
  
  - [x] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
  4. 3. (Optional)Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeds
  - [x] Summary: This vulnerablity allows remote attackers to inject arbitrary web script or HTML via video URL in YouTube emebeds.
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.7.3
  - [x] GIF Walkthrough:

     <img src='Challenge 4 Video.gif' title='youtube video' alt='Youtube Video' />

  - [x] Steps to recreate: Create a new page and place the following code in the body:

    ```
    [embed src='https://youtube.com/embed/5678\x3csvg onload=alert(1)\x3e'][/embed]
    ```

    When the page is viewed, the injected code is executed.


## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [2018] [Omar Elnagdy]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
