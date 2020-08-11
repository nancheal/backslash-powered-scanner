# backslash-powered-scanner
This extension complements Burp's active scanner by using a novel approach capable of finding and confirming both known and unknown classes of server-side injection vulnerabilities. Evolved from classic manual techniques, this approach reaps many of the benefits of manual testing including casual WAF evasion, a tiny network footprint, and flexibility in the face of input filtering.

For more information, please refer to the whitepaper at http://blog.portswigger.net/2016/11/backslash-powered-scanning-hunting.html

The code can be found at https://github.com/portswigger/backslash-powered-scanner Contributions and feature requests are welcome.

# Changelog
**self 20200811**
 - burp\DiffingScan.java:487 File add 
    - 1.Path Manipulation(doubleDotSlash) - https://portswigger.net/web-security/file-path-traversal/lab-sequences-stripped-non-recursively
    - 2.File Path Manipulation(urlEncodeDotSlash) - https://portswigger.net/web-security/file-path-traversal/lab-superfluous-url-decode
    - 3.File Path Manipulation(pathDotSlash) - https://portswigger.net/web-security/file-path-traversal/lab-validate-start-of-path
    - 4.File Path Manipulation(pathDoubleDotSlash) - 1+3
 
**1.03 20190814**
 - Detect path normalization exploits based on Orange Tsai's research
 
**1.02 20180606**
 - Add MD5/SHA-1 lax comparison to magic value attacks
 - Misc bugfixes
 
**1.01 20180509**
 - Add 'COM1' Windows reserved filename to magic value attacks
 - Support custom magic value attacks
 - Don't attempt filepath related attacks in the request path
 
**1.0 20180214**
 - Provide a configuration dialog

**0.91 20170612**
 - Detect alternative code paths triggered by keywords like 'null', 'undefined' etc
 
**0.9 20170520**
 - Detect JSON Injection and escalate into RCE where possible
 - Detect Server-Side HTTP Parameter Pollution
 - Support bruteforcing backend parameter names
 - Improve evidence clarity and reduce false positives
 - Find vulnerabilities with subtler evidence
 - Detect escape sequence injection
 - Improve LFI detection
 - Misc tweaks, bugfixes and efficiency improvements
 
**0.86 20161004**
 - First public release

# Installation
This extension requires Burp Suite Pro 1.7.10 or later. To install it, simply use the BApps tab in Burp.

If you want to manually build/install it from source, you'll need to add the following JAR to your libraries: https://commons.apache.org/proper/commons-lang/download_lang.cgi

