# XSS in Create Tag in enhavo 0.13.1

**Software link**: Enhavo 0.13.1 [https://www.enhavo.com]

**@author**: Daniel Puente

**@description**: Cross-site scripting (XSS) vulnerability in the functionality `Create Tag` from the panel `New/Edit Article`,  of Enhavo v0.13.1 allow attackers to execute arbitrary web scripts or HTML via a crafted payload injected into `Create Tag` field.
After that, every time an article is open for review/edit will execute the payload, making it a stored XSS.

---
# PoC

1. An article is added or is just edited, in the field to add a new tag, we need to create a new one, where a crafted payload is given.
![Crafted Payload](https://github.com/dd3x3r/enhavo/assets/74184545/a64e5406-344b-4b76-b3e4-55a087c59977)

2. As a result, when saved, the XSS is executed.
![image](https://github.com/dd3x3r/enhavo/assets/74184545/2f81fe6f-ea28-4f3f-bbcf-76764da69efd)

3. If selected from the dropdown list in another article or the same, it will execute without the need for saving the changes.
![image](https://github.com/dd3x3r/enhavo/assets/74184545/b4ad5796-6201-478c-bb42-30438334fcf3)

4. If accessed the article for further review/edit, the payload will execute before the article loads.
![image](https://github.com/dd3x3r/enhavo/assets/74184545/f0f914c0-a3dd-4657-adcd-44ea13d75717)
