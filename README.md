# Neural Style Transfer (NST)

## NST task

> เหมือนการใส่ฟิลเตอร์รูป(content)ให้เป็นลายเส้นแบบที่ต้องการ(style)

- input คือรูป 2 ใบ ได้แก่ Content และ Style
- output คือรูปที่ถูกสร้างออกมา Generated

![style_transfer](./README_img/style_transfer.png)

## NST ประวัติ

- Leon Gatys et al ปี **2015**
- การนำ content ออกมาจาก CNN
- **VGG-19** CNN

## Content Representation

- output ของ แต่ละ conv layer เรียกว่า **feature map**
- ใช้ CNN extract feature(content) ออกจากภาพที่ต้องการได้
  - edge, รูปร่าง

## Style Representation

- **Gram Matrix**

## หลักการ NST

- สุ่มรูปมั่วๆ (รูป Generated, output) ป้อนเข้า CNN
- หา feature map ของรูปนั้น
  - หาจาก layer ลึกๆ
  - เราหวังว่า output จะเหมือนกับ content
  - **Content Loss** = ความต่างระหว่าง Generated_feature กับ Content_feature
  - ถ้าเรา train ส่วนนี้ ก็จะแปลงจากรูปสุ่มๆ ให้เป็น content ได้
- ทำกับ style ด้วย
  - **Style Loss**
- **Loss** = a*Content_loss + b*Style_loss

## References

- Deep Learning (Andrew Ng)
- The AI Epiphany (https://www.youtube.com/watch?v=B22nIUhXo4E)
- A neural Algorithm of Artistic Style (Leon Gatys et al 2015)
- The AI Epiphany Github Repository (https://github.com/gordicaleksa/pytorch-neural-style-transfer)