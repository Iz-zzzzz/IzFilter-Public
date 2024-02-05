English version (Jun 16, 2023) click  [here](https://github.com/Iz-zzzzz/IzFilter-Public/blob/main/README_Eng.md)

<img alt="GitHub commit activity" src="https://img.shields.io/github/commit-activity/m/Iz-zzzzz/IzFilter-Public"> <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/Iz-zzzzz/IzFilter-Public"> <img alt="GitHub contributors" src="https://img.shields.io/github/contributors/Iz-zzzzz/IzFilter-Public">

# Iz's Addon Filter Public Version

- การสร้าง rules ใน filter list นี้จะเน้นไปที่การบล็อกให้ครอบคลุมมากที่สุด, เจาะจงมากที่สุด และที่จำเป็นเท่านั้น เพื่อทำให้ performance drop น้อยที่สุด
- จุดประสงค์ของ filter list นี้ คือ
  - ใช้แทนที่ [EasyList Thailand](https://github.com/easylist-thailand/easylist-thailand) ได้ 100% และ filter นี้ครอบคลุมกว่ามาก
  - บล็อกโฆษณาทุกชนิด [^3][^6][^4]
    - script โฆษณา
    - โฆษณาประจำเว็บ (specific) (ไม่รวมถึงโฆษณาประจำเว็บที่ไม่ได้การสนับสนุนจากภายนอก)
    - โฆษณาประเภทรูป
    - โฆษณาประเภทข้อความ
    - โฆษณาประเภท video  (video ad)
    - โฆษณาประเภทเว็บพuัu
    - โฆษณาทั่วไป (generic ad)
    - advertisement network request
    - popup advertisement
    - popunder advertisement
    - notification advertisement
    - anti-adblock [^4]
    - โฆษณาประเภท frame
  - บล็อกสื่งต่างๆ ที่น่ารำคาญ หรือดึงดูดความสนใจ [^3][^6]
    - paywall ที่ไม่สมเหตุสมผล [^4]
    - cookie consent
      - cosmetics rule
      - network request rule
    - ป้องกันคลิกขวา
    - ป้องกันลากคลุมข้อความ
  - ความเป็นส่วนตัว [^3][^6]
    - analytics
    - telemetry
    - network request parameter ที่ไม่จำเป็น
    - script หรือ element ไม่จำเป็น (ไม่รวม back to top button)
  - บล็อกเว็บอันตราย เช่น spam ใน Facebook(เมื่อกดคลิกลิงก์ไปจะมีข้อความเตือน), ลิงก์ Phishing [^6]
    - เว็บอันตรายประเภท frame ที่แฝงภายในเว็บ
  - พยายามให้สามารถทำงานได้ดีที่สุด แม้ไม่ได้เปิดใช้งาน cosmetic filter [^6]
  - unblock rules ที่ไม่จำเป็นของ filter list อื่นๆ ทำให้ performance ดีขึ้น เช่น facebook.com, twitter.com, instagram.com, youtube.com เป็นต้น [^1] [^3]
  - พยายามใช้ HTML Filtering เมื่อใช้ได้ [^5]
- หากเป็นชาวต่างชาติ(ไม่เข้าเว็บภาษาไทย) แล้วใช้ filter list นี้ จะได้ประโยชน์จากการ rule ที่เพิ่มเติมในเว็บ international และ unblock rules ที่ไม่จำเป็นของ filter list อื่นๆ

> [!IMPORTANT]
> Filter list นี้เป็นเพียงแค่ Add-On ดังนั้น "ควร"ใช้งานร่วมกับ filter ดังนี้
> - AdGuard Filter
> - AdGuard – Cookie Notices
> - AdGuard Tracking Protection
> - AdGuard URL Tracking Protection
> - AdGuard – Mobile Ads
> - EasyList
> - Easylist Cookie List
> - Easy Privacy 
>
> เพื่อให้สามารถบล็อกได้ครอบคลุมมากที่สุด

> [!IMPORTANT]
>  ไม่ควรใช้ [EasyList Thailand](https://github.com/easylist-thailand/easylist-thailand) เพราะ [EasyList Thailand](https://github.com/easylist-thailand/easylist-thailand) ไม่ได้มีการ maintenance มากนัก ทำให้ filter ส่วนใหญ่ใช้ไม่ได้แล้ว และ filter list นี้ครอบคลุมกว่ามาก

> ถ้าใช้ uBlock Origin ก็ควรเปิด uBlock filters – Ads, uBlock filters – Privacy และ uBlock filters – Annoyances ด้วย

> Filter list นี้เป็นส่วนหนึ่งของ Iz's Addon Filter Full ที่บล็อกได้ครอบคลุมและอัพเดตบ่อยกว่า แต่อันนั้นไม่ได้เปิดเป็นสาธารณะเพราะมันมีข้อผิดพลาดเยอะมาก

## วิธีเพิ่ม Filter List ลง AdBlock ของคุณ

- AdGuard extension
  - กด[ที่นี่](https://subscribe.adblockplus.org/?location=https%3A%2F%2Fraw.githubusercontent.com%2FIz-zzzzz%2FIzFilter-Public%2Fmain%2FIz's%20Addon%20Filter%20Public%20Github.txt&title=Iz's%20Addon%20Filter%20Public%20Github) > กด Next > (ทำหรือไม่ก็ได้ มีผลเล็กน้อย) ติ๊กถูก Trusted > กด Subscribe
- uBlock Origin extension
  - กด[ที่นี่](https://subscribe.adblockplus.org/?location=https%3A%2F%2Fraw.githubusercontent.com%2FIz-zzzzz%2FIzFilter-Public%2Fmain%2FIz's%20Addon%20Filter%20Public%20Github.txt&title=Iz's%20Addon%20Filter%20Public%20Github) > กด Subscribe ที่มุมขวาบน
- Brave built-in AdBlock
  - ไปที่การตั้งค่าของ Brave browser > Shields > Content filtering > ตรงหมวด Add custom filter lists > ให้ใส่ Url นี้ `https://raw.githubusercontent.com/Iz-zzzzz/IzFilter-Public/main/Iz's%20Addon%20Filter%20Public%20Github.txt` > กด Add
- อื่นๆ : ให้หา menu ประมาณ custom filter lists แล้วนำลิงก์ไปใส่ด้วยตัวเอง

> เมื่อเพิ่ม filter list แล้ว AdBlock ของคุณจะดาวโหลดข้อมูล filter list นี้เป็นระยะๆ โดยอัตโนมัติ

> ทั้งหมดนี้อย่าลืมเปิดให้ AdBlock ทำงานด้วย ทั้งส่วนแยกของแต่ละเว็บ, Whilelist และ Allow list ทั้งหลาย

#### ควรใช้ใน
  - Browser Extension: [uBlock Origin](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm), [AdGuard](https://chrome.google.com/webstore/detail/adguard-adblocker/bgnkhhnnamicmpeenaelnjfhikgbkllg) [^1]
  - AdGuard Application: [Windows](https://adguard.com/en/adguard-windows/overview.html) [^1], [Android app](https://adguard.com/en/adguard-android/overview.html) [^1], [iOS, iPadOS](https://apps.apple.com/us/app/adguard-adblock-privacy/id1047223162) [^1], [Mac](https://adguard.com/en/adguard-mac/overview.html) [^1].
  - Brave built-in AdBlock: [Windows, iOS, iPadOS, macOS, Android, Linux](https://brave.com/) [^2]

  **program อื่นๆ อาจจะสามารถใช้ได้ แต่แค่ยังไม่ได้ลอง

## Iz's Filter Public Version ผิดพลาด หรือบล็อกไม่ครบ
### รายงานปัญหาให้แก้ไข
กรุณารายงานปัญหา[ที่นี้](https://github.com/Iz-zzzzz/IzFilter-Public/issues) 
โดยให้รายละเอียดดังนี้ :
- URL ของไซต์ที่พบปัญหา(ขอแบบเป๊ะ)
- (ควรจะมี) Screenshot พร้อมวงจุดที่คิดว่าผิดพลาดให้ชัดเจน
- Filter list อื่นๆ ที่ใช้งานด้วยกัน ขณะพบปัญหา
- Extension/Application AdBlock ที่ใช้งาน ขณะพบปัญหา
- (ถ้าใช้ AdGuard) ระบุ Stealth mode options ที่ใช้
- ปัญหาที่พบ

### หากรู้วิธีแก้ไขปัญหาเอง

กรุณาเพิ่ม Pull request เอง [ที่นี้](https://github.com/Iz-zzzzz/IzFilter-Public/pulls)

## อื่นๆ

- This filter list may contain other filter lists. I already commented the sources.
- The reason why I have not pull request to EasyList Thailand repository is EasyList contains only basic syntax. But this filter list contains a lot of extended syntax.

## หมายเหตุ

[^1]: Filter list นี้ทำให้ uBlock Origin เป็นหลัก ดังนั้น rules ที่ถูกปรับแต่งให้ทำงานไวขึ้นทั้งหมด(มีไม่กี่ rules เช่น ใน facebook.com, instagram.com, twitter.com)จะใช้ไม่ได้ใน AdGuard และ Brave แต่ AdGuard ก็มี rules ของตัวเองที่ดีอยู่แล้ว

[^2]: Brave built-in AdBlock ไม่ได้รองรับทุก syntax ที่ AdGuard และ uBlock Origin รองรับ จะมีบางเว็บที่ element ซับซ้อน เช่น facebook.com, instagram.com ที่ไม่สามารถบล็อกได้ (youtube.com บล็อกได้)

[^3]: เพิ่มเติมจากที่ AdGuard Base Filter, AdGuard – Cookie Notices, EasyList, Easylist Cookie List ที่ไม่ได้ครอบคลุมส่วนนี้

[^4]: filter list นี้บล็อกโษณาที่ผิดกฏหมายหรือไม่เป็นธรรมเป็นหลัก กรุณาสนับสนุนเว็บที่โฆษณาอย่างถูกกฏหมายและเป็นธรรมด้วยการ Whitelist หรือ Allow list.

[^5]:  HTML filtering ทำงานใน uBO and AdGuard extension ใน Gecko based browser และ stand alone AdGuard app เท่านั้น. กรุณาดูข้อมูลเพิ่มเติมที่ [uBO wiki](https://github.com/gorhill/uBlock/wiki/Static-filter-syntax#html-filters) หรือ [AdGuard wiki](https://adguard.com/kb/general/ad-filtering/create-own-filters/#html-filtering-rules)

[^6]: ครอบคลุมเท่าที่ผมจะได้
