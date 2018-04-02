# Project 7 - WordPress Pentesting

Time spent: **11** hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required) Vulnerability Name or ID: Authenticated Stored Cross-Site Scripting(XSS1)
  - [x] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.4
  - [x] GIF Walkthrough: 
    - <img src='XSS2.gif' title='User Enumeration' width='' alt='' />
  - [x] Steps to recreate: 
    - Create a new post, and then put this code ```<a href = "[caption code=">]</a><a title="onmouseover= alert('')" >Link</a>``` in the content link. Finally click link to show message in the preview of post.
  - [x] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/branches/4.2/src/wp-includes/class-wp-editor.php?rev=33361)

2. (Required) Vulnerability Name or ID: User Enumeration
  - [x] Summary: 
    - Vulnerability types: User Enumeration
    - Tested in version: 4.2
    - Fixed in version: 4.2.4
  - [x] GIF Walkthrough: 
    - <img src='UserEnumeration.gif' title='User Enumeration' width='' alt='' />
  - [x] Steps to recreate: 
    - Go to the WordPress login page, when you input admin as username and empty password field, then it shows the error which is the password field is empty. When you input admin as username and randomly input password, then it shows the error which is the password you entered for the username admin is incorrect.  When you randomly input both username and password, then it shows the error which is invalid username.
  - [x] Affected source code:
    - [Link 2](https://www.wpwhitesecurity.com/wordpress-security/wordpress-username-disclosure-vulnerability/)

3. (Required) Vulnerability Name or ID: Unauthenticated Stored Cross-Site Scripting (XSS2)
  - [x] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.4
  - [x] GIF Walkthrough: 
    - <img src='XSS.gif' title='XSS2' width='' alt='' />
  - [x] Steps to recreate: 
    - View a new post, and insert code ```<abbr title='wpdistillery' onmouseover='alert(1)' style='position:fixed;top:0;left:0;width:100%;height:100%'>``` on the comment uder this post. Then it shows 1 when you view the comment of this post in future.
  - [x] Affected source code:
    - [Link 3](https://cedricvb.be/post/wordpress-stored-xss-vulnerability-4-1-2/)




## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Describe any challenges encountered while doing the work

## License

    Copyright [2018] [Yu Xuan Huang]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
