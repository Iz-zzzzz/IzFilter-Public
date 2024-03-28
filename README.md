English version (Jun 16, 2023) click  [here](https://github.com/Iz-zzzzz/IzFilter-Public/blob/main/README_Eng.md)

<img alt="GitHub commit activity" src="https://img.shields.io/github/commit-activity/m/Iz-zzzzz/IzFilter-Public"> <img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/Iz-zzzzz/IzFilter-Public"> <img alt="GitHub contributors" src="https://img.shields.io/github/contributors/Iz-zzzzz/IzFilter-Public">

# Iz's Addon Filter Public Version

- เน้นไปที่การบล็อกให้ครอบคลุมมากที่สุด
- เจาะจงมากที่สุด และที่จำเป็นเท่านั้น
- มีผลกระทบต่อ performance น้อยที่สุด
- <details><summary>จุดประสงค์ของ filter list นี้ คือ</summary>

  - บล็อกโฆษณาทุกชนิด [^3][^6][^4]
    - script โฆษณา
    - โฆษณาประจำเว็บ (ไม่รวมถึงโฆษณาประจำเว็บที่ไม่ได้การสนับสนุนจากภายนอก)
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
      - cookie network request rule
    - ป้องกันการคลิกขวา
    - ป้องกันลากคลุมข้อความ
    - เว็บมี css บัค
  - ความเป็นส่วนตัว [^3][^6]
    - analytics
    - telemetry
    - network request parameter ที่ไม่จำเป็น
    - script หรือ element ไม่จำเป็น (ไม่รวม back to top button)
    - parameter
  - บล็อกเว็บอันตราย เช่น spam ใน Facebook(เมื่อกดคลิกลิงก์ไปจะมีข้อความเตือน), ลิงก์ Phishing [^6]
    - เว็บอันตรายประเภท frame ที่แฝงภายในเว็บ
  - พยายามให้สามารถทำงานได้ดีที่สุด แม้ไม่ได้เปิดใช้งาน cosmetic filter [^6]
  - unblock rules ที่ไม่จำเป็นของ filter list อื่นๆ ทำให้ performance ดีขึ้น เช่น facebook.com, twitter.com, instagram.com, youtube.com เป็นต้น [^1] [^3]
  - พยายามใช้ HTML Filtering เมื่อใช้ได้ [^5] [^6]
  - สามารถใช้ร่วมกับ extension [Dark Reader](https://github.com/darkreader/darkreader) ได้ และช่วยแก้บาง element ที่ทำให้เป็น dark mode ไม่สำเร็จด้วย [^6]
  - หากเป็นชาวต่างชาติ(ไม่เข้าเว็บภาษาไทย) แล้วใช้ filter list นี้ จะได้ประโยชน์จากการ rule ที่เพิ่มเติมในเว็บ international และ unblock rules ที่ไม่จำเป็นของ filter list อื่นๆ
</details>

> [!IMPORTANT]
> <details><summary>Filter list นี้เป็นเพียงแค่ Add-On ดังนั้น "ควร"ใช้งานร่วมกับ filter ข้างล่างนี้ เพื่อให้สามารถบล็อกได้ครอบคลุมมากที่สุดนี้ คือ</summary>
>
> - AdGuard Filter
> - AdGuard – Cookie Notices
> - AdGuard Tracking Protection
> - AdGuard URL Tracking Protection
> - AdGuard – Mobile Ads
> - EasyList
> - Easylist Cookie List
> - Easy Privacy 
>
> ถ้าใช้ uBlock Origin ก็ควรเปิด uBlock filters – Ads, uBlock filters – Privacy และ uBlock filters – Annoyances ด้วย
</details>

> [!IMPORTANT]
> <details><summary> ไม่ควรใช้ร่วมกับ EasyList Thailand เพราะ </summary>
>
> 1. [EasyList Thailand](https://github.com/easylist-thailand/easylist-thailand) อาจไม่ได้มีการ maintenance บ่อยนัก ทำให้ filter ส่วนใหญ่ใช้ไม่ได้ หรือไม่ก็มีบางส่วนซ้อนทับกันกับ filter นี้ โดยไม่จำเป็น
> 2. จุดประสงค์หลักที่ต่างกันของ filter และทำเพื่อ platform ที่ต่างกัน (filter list นี้เน้นรองรับ uBO, AdGuard, Brave เป็นหลัก) จึงอาจทำให้ filter บางส่วนขัดแย้งกันหรือใช้ได้ไม่เต็มประสิทธิภาพ
> 3. filter list นี้ทำมาครอบคลุมกว่า [EasyList Thailand](https://github.com/easylist-thailand/easylist-thailand)

<details><summary>วิธีเพิ่ม Filter List ลง AdBlock ของคุณ
</summary>

- [AdGuard extension](https://adguard.com/en/adguard-browser-extension/overview.html) [^1]
  - กด[ที่นี่](https://subscribe.adblockplus.org/?location=https%3A%2F%2Fraw.githubusercontent.com%2FIz-zzzzz%2FIzFilter-Public%2Fmain%2FIz's%20Addon%20Filter%20Public%20Github.txt&title=Iz's%20Addon%20Filter%20Public%20Github) > กด Next > (ทำหรือไม่ก็ได้ มีผลเล็กน้อย) ติ๊กถูก Trusted > กด Subscribe
- [uBlock Origin extension](https://github.com/gorhill/uBlock)
  - กด[ที่นี่](https://subscribe.adblockplus.org/?location=https%3A%2F%2Fraw.githubusercontent.com%2FIz-zzzzz%2FIzFilter-Public%2Fmain%2FIz's%20Addon%20Filter%20Public%20Github.txt&title=Iz's%20Addon%20Filter%20Public%20Github) > กด Subscribe ที่มุมขวาบน
- Brave Browser (built-in AdBlock) [Windows, iOS, iPadOS, macOS, Android, Linux](https://brave.com/) [^2]
  - ไปที่การตั้งค่าของ Brave browser > Shields > Content filtering > ตรงหมวด Add custom filter lists > ให้ใส่ Url นี้ `https://raw.githubusercontent.com/Iz-zzzzz/IzFilter-Public/main/Iz's%20Addon%20Filter%20Public%20Github.txt` > กด Add
- AdGuard Application: [Windows](https://adguard.com/en/adguard-windows/overview.html) [^1], [Android app](https://adguard.com/en/adguard-android/overview.html) [^1], [iOS, iPadOS](https://apps.apple.com/us/app/adguard-adblock-privacy/id1047223162) [^1], [Mac](https://adguard.com/en/adguard-mac/overview.html) [^1]
  - ให้หาในหมวด Custom filter แล้วใส่ Url นี้ `https://raw.githubusercontent.com/Iz-zzzzz/IzFilter-Public/main/Iz's%20Addon%20Filter%20Public%20Github.txt` > (ทำหรือไม่ก็ได้ มีผลเล็กน้อย) ติ๊กถูก Trusted > กด Subscribe
- อื่นๆ
  - ให้หา menu ที่บอกถึง custom filter lists แล้วนำลิงก์ไปใส่ด้วยตัวเอง
> ทั้งนี้ filter นี้ทำมาเพื่อรองรับ platform ด้านบนเป็นหลัก
> - ไม่แนะนำให้ใช้ด้วย AdBlock extension ใน Safari เพราะ Safari API limit มาก ทำให้ AdBlock ไม่สามารถทำงานได้อย่างที่ควรจะเป็นแบบใน platfrom อื่นๆ

> Chromium กำลังจะปิด Manifest V2 (API หลักของ AdBlock) ในอนาคต แนะนำให้หลีกเลี่ยง Chromium-based browser อื่นๆ ไปใช้ Brave, Firefox หรือ AdGuard Application แทน [^7]

> ทั้งนี้อย่าลืมเปิดให้ AdBlock ทำงานด้วย ทั้งส่วนแยกของแต่ละเว็บ, Whilelist และ Allow list ทั้งหลาย
</details>

## Iz's Filter Public Version ผิดพลาด หรือบล็อกไม่ครบ
### รายงานปัญหาให้แก้ไข
กรุณารายงานปัญหา[ที่นี้](https://github.com/Iz-zzzzz/IzFilter-Public/issues) 

### หากรู้วิธีแก้ไขปัญหาเอง

กรุณาเพิ่ม Pull request เอง [ที่นี้](https://github.com/Iz-zzzzz/IzFilter-Public/pulls)

## อื่นๆ

- This filter list may contain other filter lists. I already commented the sources.

#### Documents ที่เป็นประโยชน์
- [uBlock Origin filter wiki](https://github.com/gorhill/uBlock/wiki/Static-filter-syntax)
- [Adguard filter syntax](https://kb.adguard.com/en/general/how-to-create-your-own-ad-filters)
- [Adguard's compatibility-table](https://github.com/AdguardTeam/Scriptlets/blob/master/wiki/compatibility-table.md)
- [W3 School DOM Event object](https://www.w3schools.com/jsref/dom_obj_event.asp)

#### Filter list นี้สานต่อจาก
- [EasyList Thailand](https://github.com/easylist-thailand/easylist-thailand)
- [thai-ads-filter](https://github.com/adblock-thai/thai-ads-filter)

## หมายเหตุ

[^1]: Filter list นี้ทำให้ uBlock Origin เป็นหลัก ดังนั้น rules ที่ถูกปรับแต่งให้ทำงานไวขึ้นทั้งหมด(มีไม่กี่ rules เช่น ใน facebook.com, instagram.com, twitter.com)จะใช้ไม่ได้ใน AdGuard และ Brave แต่ AdGuard ก็มี rules ของตัวเองที่ดีอยู่แล้ว

[^2]: Brave built-in AdBlock ไม่ได้รองรับทุก syntax ที่ AdGuard และ uBlock Origin รองรับ จะมีบางเว็บที่ element ซับซ้อน เช่น facebook.com, instagram.com ที่ไม่สามารถบล็อกได้ (youtube.com บล็อกได้)

[^3]: เพิ่มเติมจากที่ AdGuard Base Filter, AdGuard – Cookie Notices, EasyList, Easylist Cookie List ที่ไม่ได้ครอบคลุมส่วนนี้

[^4]: filter list นี้บล็อกโษณาที่ผิดกฏหมายหรือไม่เป็นธรรมเป็นหลัก กรุณาสนับสนุนเว็บที่โฆษณาอย่างถูกกฏหมายและเป็นธรรมด้วยการเพิ่มเว็บนั้นลง Whitelist หรือ Allow list หรือ Trust sites.

[^5]:  HTML filtering ทำงานใน uBO and AdGuard extension ใน Gecko based browser และ stand alone AdGuard app เท่านั้น. กรุณาดูข้อมูลเพิ่มเติมที่ [uBO wiki](https://github.com/gorhill/uBlock/wiki/Static-filter-syntax#html-filters) หรือ [AdGuard wiki](https://adguard.com/kb/general/ad-filtering/create-own-filters/#html-filtering-rules)

[^6]: ครอบคลุมและมีความผิดพลาดน้อยสุดเท่าที่ผมจะทำได้ (ผมไม่รับประกันและไม่รับผิดชอบถึงความเสียหายที่เกิดขึ้นจากผู้ใช้งานเองทุกกรณี เนื่องด้วยทรัพยากรบุคคลที่จำกัด)

[^7]: https://chrome-stats.com/manifest-v3-migration
