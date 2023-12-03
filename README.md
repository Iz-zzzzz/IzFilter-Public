English version (Jun 16, 2023) click  [here](https://github.com/Iz-zzzzz/IzFilter-Public/blob/main/README_Eng.md)

<img alt="GitHub commit activity" src="https://img.shields.io/github/commit-activity/m/Iz-zzzzz/IzFilter-Public"> <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/Iz-zzzzz/IzFilter-Public"> <img alt="GitHub contributors" src="https://img.shields.io/github/contributors/Iz-zzzzz/IzFilter-Public">

# Iz's Addon Filter Public Version
- ควรใช้ใน
  - Extension: [uBlock Origin](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm), [AdGuard](https://chrome.google.com/webstore/detail/adguard-adblocker/bgnkhhnnamicmpeenaelnjfhikgbkllg)
  - AdGuard Application: [Windows](https://adguard.com/en/adguard-windows/overview.html) [1](https://github.com/Iz-zzzzz/IzFilter-Public#%E0%B8%AB%E0%B8%A1%E0%B8%B2%E0%B8%A2%E0%B9%80%E0%B8%AB%E0%B8%95%E0%B8%B8), [Android app](https://adguard.com/en/adguard-android/overview.html) [1](https://github.com/Iz-zzzzz/IzFilter-Public#%E0%B8%AB%E0%B8%A1%E0%B8%B2%E0%B8%A2%E0%B9%80%E0%B8%AB%E0%B8%95%E0%B8%B8), [iOS, iPadOS](https://apps.apple.com/us/app/adguard-adblock-privacy/id1047223162) [1](https://github.com/Iz-zzzzz/IzFilter-Public#%E0%B8%AB%E0%B8%A1%E0%B8%B2%E0%B8%A2%E0%B9%80%E0%B8%AB%E0%B8%95%E0%B8%B8), [Mac](https://adguard.com/en/adguard-mac/overview.html) [1](https://github.com/Iz-zzzzz/IzFilter-Public#%E0%B8%AB%E0%B8%A1%E0%B8%B2%E0%B8%A2%E0%B9%80%E0%B8%AB%E0%B8%95%E0%B8%B8).
  - Brave built-in AdBlock: [Windows, iOS, iPadOS, macOS, Android, Linux](https://brave.com/) [2](https://github.com/Iz-zzzzz/IzFilter-Public#%E0%B8%AB%E0%B8%A1%E0%B8%B2%E0%B8%A2%E0%B9%80%E0%B8%AB%E0%B8%95%E0%B8%B8)

  **program อื่นๆ อาจจะสามารถใช้ได้ แต่แค่ยังไม่ได้ลอง

- การสร้าง rules ใน filter list นี้จะเน้นไปที่การบล็อกให้ครอบคลุมมากที่สุด, เจาะจงมากที่สุด และที่จำเป็นเท่านั้น เพื่อไม่ทำให้ performance drop มากเกินความจำเป็น
- จุดประสงค์ของ filter นี้ คือ 
  - บล็อกโฆษณาทุกชนิด รวมถึงเว็บพuัuด้วย [3](https://github.com/Iz-zzzzz/IzFilter-Public#%E0%B8%AB%E0%B8%A1%E0%B8%B2%E0%B8%A2%E0%B9%80%E0%B8%AB%E0%B8%95%E0%B8%B8)
  - บล็อก annoyances elements [3](https://github.com/Iz-zzzzz/IzFilter-Public#%E0%B8%AB%E0%B8%A1%E0%B8%B2%E0%B8%A2%E0%B9%80%E0%B8%AB%E0%B8%95%E0%B8%B8)
  - unblock rules ที่ไม่จำเป็น ทำให้ performance ดีขึ้น เช่น facebook.com, twitter.com, instagram.com, youtube.com เป็นต้น [1](https://github.com/Iz-zzzzz/IzFilter-Public#%E0%B8%AB%E0%B8%A1%E0%B8%B2%E0%B8%A2%E0%B9%80%E0%B8%AB%E0%B8%95%E0%B8%B8) [3](https://github.com/Iz-zzzzz/IzFilter-Public#%E0%B8%AB%E0%B8%A1%E0%B8%B2%E0%B8%A2%E0%B9%80%E0%B8%AB%E0%B8%95%E0%B8%B8)
- หากเป็นชาวต่างชาติ(ไม่เข้าเว็บภาษาไทย) แล้วใช้ filter list นี้ อาจจะได้ประโยชน์จากการบล็อกเว็บ international และ unblock rules ที่ไม่จำเป็นใน filter list นี้

`Filter list นี้เป็นเพียงแค่ Add-On ดังนั้น "ควร"ใช้งานร่วมกับ AdGuard Base Filter, AdGuard – Cookie Notices, EasyList, Easylist Cookie List เพื่อให้สามารถบล็อกได้ครอบคลุมมากที่สุด`

`ถ้าใช้ uBlock Origin ก็ควรเปิด uBlock filters – Ads และ uBlock filters – Privacy ด้วย`

`Filter list นี้เป็นส่วนหนึ่งของ Iz's Addon Filter Full ที่บล็อกได้ครอบคลุมและอัพเดตบ่อยกว่ามาก แต่อันนั้นไม่ได้เปิดเป็นสาธารณะเพราะมันดีเกินไป`

## วิธีเพิ่ม Filter
- AdGuard extension ไปที่แถบ Filters > กด Custom ด้านล่างสุด > กดปุ่ม Add Custom filter > ใส่ [Url นี้](https://raw.githubusercontent.com/Iz-zzzzz/IzFilter-Public/main/Iz's%20Addon%20Filter%20Public%20Github.txt) > (ไม่จำเป็น) ติ๊ก Trusted > กดปุ่ม Subscribe
- uBlock Origin ไปที่แถบ Filter lists > เลื่อนลงสุด > ติ๊ก Import > ใส่ [Url นี้](https://raw.githubusercontent.com/Iz-zzzzz/IzFilter-Public/main/Iz's%20Addon%20Filter%20Public%20Github.txt) > กดปุ่ม Apply changes
- Brave built-in AdBlock ไปที่การตั้งค่าของ browser > Shields > Content filtering > ตรงหมวด Add custom filter lists > ให้ใส่ [Url นี้](https://raw.githubusercontent.com/Iz-zzzzz/IzFilter-Public/main/Iz's%20Addon%20Filter%20Public%20Github.txt) > กด Add
ทั้งหมดนี้อย่าลืมเปิดให้ AdBlock ทำงานด้วย ทั้งส่วนแยกของเว็บ Whilelist, Allow list ทั้งหลาย

## ต้องการทำให้ Iz's Filter Public Version ดีขึ้นหรือไม่
### รายงานปัญหาให้แก้ไข
กรุณารายงานปัญหา[ที่นี้](https://github.com/Iz-zzzzz/IzFilter-Public/issues) โดยให้รายละเอียดดังนี้ :
- URL ที่ครบถ้วนของเว็บไซต์ที่พบปัญหา
- Screenshot พร้อมวงจุดที่คิดว่าผิดพลาดให้ชัดเจน
- Filter อื่นๆ ที่ใช้งาน ขณะพบปัญหา
- Extension/Application AdBlock ที่ใช้งาน
- (ถ้าใช้ AdGuard) Stealth mode options ที่ใช้
- ปัญหาที่พบ

### หากรู้วิธีแก้ไขปัญหาเอง
กรุณาเพิ่ม Pull request [ที่นี้](https://github.com/Iz-zzzzz/IzFilter-Public/pulls)

## Disclaimer
- This filter may contain other's filter. I already commented the sources.

## หมายเหตุ
1: Filter นี้ทำให้ uBlock Origin เป็นหลัก ดังนั้น rules ที่ถูกปรับแต่งให้ทำงานไวขึ้นทั้งหมด(มีไม่กี่ rules เช่น ใน facebook.com, instagram.com, twitter.com)จะใช้ไม่ได้ใน AdGuard และ Brave แต่ AdGuard ก็มี rules ของตัวเองที่ดีอยู่แล้ว

2: Brave built-in AdBlock ไม่ได้รองรับทุก syntax ที่ AdGuard และ uBlock Origin รองรับ จะมีบางเว็บที่ element ซับซ้อน เช่น facebook.com, instagram.com ที่ไม่สามารถบล็อกได้ แต่ youtube.com บล็อกได้

3: เพิ่มเติมจากที่ AdGuard Base Filter, AdGuard – Cookie Notices, EasyList, Easylist Cookie List ที่ไม่ได้ครอบคลุมส่วนนี้
