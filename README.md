# Struts2-RCE
A Burp Extender for checking for struts 2 RCE vulnerabilities.

# Description

This burp extension helps identifying Struts2 remote code execution vulnerabilities in struts2 web application. This Burp extension detects following 18 RCEs and they are 

* S2-001 
* S2-007
* S2-008
* S2-012
* S2-013
* S2-014
* S2-015
* S2-016
* S2-019
* S2-029
* S2-032
* S2-033
* S2-037
* S2-045
* S2-048
* S2-053
* S2-057
* S2-DevMode

## Loading the extension

```bash
Burp Suite->Extender->Add->Select the Struts.jar file->Next.
```
Once loaded without any error a new tab will popup within existing burp instance.

## Usage

A single HTTP request can be scanned just by Right clicking on the selected request and click on 'Check for Struts RCE'.


Scanning multiple requests or scanning a complete application requires a complete crawl of the application. Note, this extension will not attempt to find any new parameter rather it will target only the existing parameters.

```bash
Burp->Target->Site map->Contents->Select all the URLs to be scanned->Right click->'Check for Struts RCE'.
```

If the URL or any parameter is prone to any Struts2 vulnerabilities it will populate under the “Struts Finder” tab. If not vulnerable, no data will reflect.

**Note:** Make sure **Extender** is checked under **Session Handling Rules**.
```bash
Burp->Project options->Session Handling Rules->Click on Edit->Scope->Tools Scope->Check mark Extender->Save.
```

**Credits**

* Prakhar Athreya
