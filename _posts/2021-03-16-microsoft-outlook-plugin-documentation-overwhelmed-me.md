---
layout: post
title: Microsoft Outlook Plugin's Documentations Overwhelmed Me 
comments: true
categories: Linux|Systems
location: DUET, Bangladesh
---

I started making a plugin for Microsoft Outlook desktop client and for the Web Outlook as well. My client organization receives a lot of spam emails and they were trying to report them to their sysadmin. "Phish alert" or similiar kind of a plugin they wanted, which will forward the current email to their sysadmin, in one click.


![Single Click PhishMe](/post_images/2021/Mar/single_click_PhishMe.png){:.center-image}
<center> <small>Single Click PhishMe Outlook Desktop Client Addon</small> </center> <br>

However, there are two API endpoints to access and work with user emails. 
- MS Office API (Deprecating)
- MS Graph API (Recommended)

I built my addon with **MS Office API** first. Then I needed to send email threads as attachments which I could't find any documentations within MS Office API, it was doable, but needed to hit **MS Graph API** endpoint. For some reason, **MS Graph API** authentication as developer seemed hectic and the whole task made me overwhelmed to say the least. 

You can checkout the repository at <a href="https://github.com/ovebepari/PhishMe">PhishMe at Github<a/>.