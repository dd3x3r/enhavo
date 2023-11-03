# XSS in Page Content Titel in enhavo 0.13.1

**Software link**: Enhavo 0.13.1 [https://www.enhavo.com]

**@author**: Daniel Puente

**@description**: Cross-site scripting (XSS) vulnerability in the field `Titel` from the panel new `Page` -> `Content`-> `Header`, of Enhavo v0.13.1 allow attackers to execute arbitrary web scripts or HTML via a crafted payload injected into `Titel` field.
After that, every time the `page` is accessed, the browser will execute the payload, making it a stored XSS.

---
# PoC

1. An article is added or is just edited, in the field to add a new tag, we need to create a new one, where a crafted payload is given.
![image](https://github.com/dd3x3r/enhavo/assets/74184545/16e0d4f5-2153-4e76-9aff-806bb01b7b5c)
![image](https://github.com/dd3x3r/enhavo/assets/74184545/9c368650-f05f-4148-865d-6e2fcf049be3)

2. As a result, when saved, the XSS is executed.
![image](https://github.com/dd3x3r/enhavo/assets/74184545/af3d0a59-d7e4-4bc8-927d-4152c41f8a20)


3. If accessed without the need of login (at the time of writing - 11/03/2023 - is published in [https://demo.enhavo.com/12]) it will execute.
![image](https://github.com/dd3x3r/enhavo/assets/74184545/edef1440-9247-46f2-8660-7c68719d66bb)
