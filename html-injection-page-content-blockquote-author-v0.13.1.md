# HTML Injection in Author for a Blokquote in enhavo 0.13.1

**Software link**: Enhavo 0.13.1 [https://www.enhavo.com]

**@author**: Daniel Puente

**@description**: HTML Injection vulnerability in the field `Author` from the panel new `Page` -> `Content`-> `Blockquote`, of Enhavo v0.13.1 allow attackers to deface the webpage HTML via a crafted payload injected into `Author` field.

---
# PoC

1. A page is added or is just edited, when editing its content, we need to create a new blockquote, where a crafted payload is given in the `Àuthor` field.
![image](https://github.com/dd3x3r/enhavo/assets/74184545/16e0d4f5-2153-4e76-9aff-806bb01b7b5c)
![image](https://github.com/dd3x3r/enhavo/assets/74184545/0564e7c4-bd36-48fb-86bf-5befa6f401b9)

2. As a result, when saved and previewed, the HTML Injection becomes visible.
![image](https://github.com/dd3x3r/enhavo/assets/74184545/8a4d7246-c43f-465b-a358-7e5823311664)


3. If accessed without the need of login (at the time of writing - 11/03/2023 - is published in [https://demo.enhavo.com/14]) it will be shown.
![image](https://github.com/dd3x3r/enhavo/assets/74184545/8fa76bba-402a-4a4d-be96-7e6b54e98ee5)
