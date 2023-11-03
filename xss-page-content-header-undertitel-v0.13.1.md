# XSS in Page Content Titel in enhavo 0.13.1

**Software link**: Enhavo 0.13.1 [https://www.enhavo.com]

**@author**: Daniel Puente

**@description**: Cross-site scripting (XSS) vulnerability in the field `Undertitel` from the panel new `Page` -> `Content`-> `Header`, of Enhavo v0.13.1 allow attackers to execute arbitrary web scripts or HTML via a crafted payload injected into `Undertitel` field.
After that, every time the `page` is accessed, the browser will execute the payload, making it a stored XSS.

---
# PoC

1. It is needed to edit or create a new `Page`, in it in the `Content` tab at the `Header` section, the vulnerable field is `Undertitel` where a crafted payload is given.
![image](https://github.com/dd3x3r/enhavo/assets/74184545/16e0d4f5-2153-4e76-9aff-806bb01b7b5c)
![image](https://github.com/dd3x3r/enhavo/assets/74184545/44d8a6c6-7863-422f-8c7a-4f01ba87ecd5)

2. As a result, when saved and previewed, the XSS is executed.
![image](https://github.com/dd3x3r/enhavo/assets/74184545/5e839962-1f25-474e-a296-242ccedc295a)


3. If accessed without the need of login (at the time of writing - 11/03/2023 - is published in [https://demo.enhavo.com/13]) it will execute.
![image](https://github.com/dd3x3r/enhavo/assets/74184545/f680121a-dac1-4f13-b42a-bf7e2c7736ec)
