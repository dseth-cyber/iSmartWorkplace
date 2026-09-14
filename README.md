# iSmart Workplace 3.6.0

เพิ่มแชท LAN แบบผสม: Directory Server ดูแลรายชื่อและกลุ่ม ส่วนข้อความและไฟล์ส่งตรงแบบเข้ารหัสระหว่างเครื่อง ดู [คู่มือตั้งค่า LAN และข้อจำกัด](LAN-CHAT-GUIDE.md) ก่อนใช้งาน รุ่นนี้ยังคงกฎ Backup เดิมและข้อมูลในโฟลเดอร์ BackupKeeper เดิม

ไฟล์ผู้ใช้ `iSmartWorkplace.exe`, ตัวติดตั้ง `iSmartWorkplace-Setup.exe`, เครื่อง Server ใช้ `iSmartWorkplace-Server.exe` รุ่น 3.1 ค้นหาและเชื่อมต่อ Server ใน LAN โดยอัตโนมัติ ผู้ใช้ทั่วไปไม่ต้องกรอก IP / SHA-256 / รหัสเชิญ ใช้ Server รุ่น 3.1 ด้วย และเลือกโหมด --require-invite หากไม่ต้องการให้เครื่องใน LAN เข้าร่วมอัตโนมัติ


## รุ่น 3.6.0: ปรับปรุงระบบแชท

คลิกขวาที่ข้อความ ไฟล์แนบ หรือสติกเกอร์ในบทสนทนาเพื่อเปิดเมนู **ตอบกลับ / คัดลอก / แชร์ / ยกเลิกข้อความ (เฉพาะข้อความตัวเอง) / ลบ** แทนปุ่มลอยใต้บับเบิล ตอบกลับจะแนบข้อความอ้างอิงย่อไปกับข้อความใหม่ แชร์คือส่งต่อเนื้อหาเดิมไปยังบุคคล/กลุ่มอื่น ลบคือเอาออกจากเครื่องนี้เครื่องเดียว ส่วนยกเลิกข้อความทำงานข้ามเครื่องแบบเข้ารหัส P2P เหมือนสถานะอ่านแล้ว (แทนที่เนื้อหาทั้งสองฝั่ง) คลิกขวารายชื่อแชท**ทั้งฝั่งซ้ายและฝั่งผู้ติดต่อออนไลน์**เพื่อ **แยกแชทเป็นหน้าต่างแยก** ดับเบิลคลิกก็แยกได้ทันทีเช่นกัน ("ลบแชทในเครื่องนี้…" อยู่ที่เมนู ⋮ ของห้องอย่างเดียว ลบเฉพาะฝั่งเราเสมอ) เลือกสติกเกอร์หรือ Emoji/ข้อความด่วนแล้วส่งทันทีโดยไม่ต้องกดส่งซ้ำ รูปภาพที่ส่ง (ไม่ใช่สติกเกอร์) แสดงเป็นภาพย่อในแชท คลิกดูรูปใหญ่ เลื่อนดูรูปถัดไป/ก่อนหน้า บันทึกรูปเดียวหรือบันทึกทั้งชุดได้ รูปหลายรูปที่ส่งพร้อมกันจะรวมเป็นตารางย่อในบับเบิลเดียว แถบคิวไฟล์แสดงครึ่งความกว้างชิดฝั่งคนส่ง และเรียงตามเวลาจริงปนกับข้อความแทนที่จะค้างอยู่ล่างสุดเสมอ ขนาดไฟล์แนบสูงสุดต่อไฟล์เพิ่มจาก 20 MB เป็น **50 MB** (ทั้งสองฝั่งต้องอัปเดตเป็น 3.6.0 ขึ้นไป มิฉะนั้นฝั่งเก่าจะปฏิเสธไฟล์ที่เกิน 20 MB หรือปฏิเสธข้อความทั้งก้อนหากเกินขนาดที่ฝั่งรับรับได้)

Popup แจ้งเตือนใกล้ Tray แสดงรูปโปรไฟล์ผู้ส่ง ไอคอน Tray ขึ้นตัวเลขข้อความที่ยังไม่อ่าน (เกิน 99 แสดง 99+) กดตอบกลับประกาศจะพาไปแชทตรงกับผู้ส่งแทนห้อง "ทุกคน" หากไม่ใช่แอดมิน ห้องที่ปิดแจ้งเตือนมีไอคอนลำโพงคาดที่รูปห้อง รายชื่อออนไลน์ด้านข้างตัดคำว่า "ออนไลน์/ออฟไลน์" ออก เหลือจุดสีเขียว/เทาและแผนก หัวห้องแชทแสดงสถานะส่วนตัว (ตัดที่ 15 ตัวอักษร) และหัวข้อผู้ติดต่อแสดงจำนวนออนไลน์รวม รายชื่อแชทด้านซ้ายแสดงเฉพาะห้องที่เคยมีประวัติสนทนาแล้วเท่านั้น องค์กรที่ยังไม่เคยแชทด้วยจะไม่ถูกดึงมาแสดงจนกว่าจะเริ่มผ่าน **+ แชทใหม่** หรือ **+ สร้างกลุ่ม**

Right-click a message, attachment, or sticker for **Reply / Copy / Share / Recall message (own messages only) / Delete** instead of buttons under the bubble. Reply attaches a short quoted reference to the new message; Share forwards the same content to another person or group; Delete removes it from this device only; Recall replaces it on both sides, encrypted peer-to-peer like read receipts. Right-click a conversation — in the list on the left or in the online contacts panel — to **open it in a separate window**; double-click does the same instantly. Local chat deletion stays in the room's ⋮ menu only, and always removes your own copy alone. Picking a sticker or an emoji/quick reply now sends it immediately, no extra Send click. Photos (not stickers) now render as inline thumbnails — click to view full-size, step through with Previous/Next, save one or save the whole batch; photos sent together collapse into one thumbnail grid bubble. File-queue bars are half-width on the sender's side and settle into their real position in the timeline instead of always trailing at the bottom. The per-file attachment limit is raised from 20 MB to **50 MB** (both sides need 3.6.0 or later — an older peer rejects a file over 20 MB, or the whole message if it exceeds what its own receiver accepts). The near-tray notification popup shows the sender's avatar, and the tray icon carries an unread-count badge (99+ past 99). Replying to an announcement now opens a direct chat with the sender instead of the admin-only broadcast room. Muted rooms show a small speaker-mute badge. The presence sidebars drop the "Online/Offline" word in favor of the status dot plus department; the chat header shows the person's status message (truncated at 15 characters) and the contacts panel shows the total online count. The conversation list now only lists rooms with actual history — anyone not yet messaged stays out until you start a chat via **+ New chat** or **+ Create group**.

แนบไฟล์หรือลากวางแล้วส่งทันที ไม่ต้องกดปุ่มส่งซ้ำและไม่มีตัวอย่างค้างให้รอ ไฟล์ที่เกิน 50 MB จะแจ้งเตือนทันทีตอนแนบ พร้อมชื่อไฟล์ที่เกินและไม่ถูกส่ง รองรับส่งวิดีโอ (MP4/MOV/WEBM/MKV) แล้ว หน้าจอเลื่อนลงล่างสุดให้อัตโนมัติทุกครั้งที่ฝั่งเราส่งข้อความ/ไฟล์ (ไม่รบกวนถ้ากำลังเลื่อนอ่านของเก่าอยู่และยังไม่ได้ส่งอะไร) ลดเวลาหน่วงที่ข้อความของตัวเองไปโผล่ในหน้าจอหลังกดส่ง แก้บั๊กที่ทำให้เครื่องอื่นนอกเหนือจาก Server มองไม่เห็นสาขา/กลุ่มที่ยังไม่เคยแชทด้วย (ตอนนี้สาขาและกลุ่มแสดงในทุกเครื่องเสมอเพื่อเลือกส่งได้สะดวก) เพิ่มรูปโปรไฟล์และสถานะส่วนตัวของตัวเองที่หัวหน้าจอแชท คลิกเพื่อแก้ไขได้ทันที และปรับให้สลับห้องแชทที่มีไฟล์แนบเยอะเร็วขึ้นด้วยการแคชภาพย่อที่ถอดรหัสแล้ว

Attaching or dropping a file now sends it immediately — no extra Send click, no staged preview to wait through. A file over 50 MB is flagged the moment it's attached, naming which files were too large and weren't queued. Video (MP4/MOV/WEBM/MKV) can now be sent. The chat view auto-scrolls to the bottom whenever you send a message or file (it leaves your place alone if you're reading older history and haven't sent anything). The delay before your own sent message appears in your own window is reduced. Fixed a bug where devices other than the Server couldn't see branches or groups they hadn't chatted in yet — branches and groups now always show on every device for easy targeting. Added your own profile picture and status to the chat header — click it to edit. Switching to a conversation with many attachments is faster now that decrypted thumbnails are cached instead of reloaded every time.

แก้ดับเบิลคลิกซ้ายที่รายชื่อแชทให้แยกแชทได้จริง — สาเหตุจริงคือคลิกครั้งแรกไปลบและสร้างรายการทั้งหมดใหม่ (เพื่ออัปเดตป้ายยังไม่อ่าน) ทำให้ Qt จับจังหวะดับเบิลคลิกไม่ได้ ตอนนี้เปลี่ยนเป็นอัปเดตรายการเดิมที่มีอยู่แทนการสร้างใหม่ แก้บั๊กเลื่อนดูข้อความล่าสุดแล้วกระโดดขึ้นบนสุดเอง โดยลดความถี่การ re-render ที่ไม่จำเป็น (เดิมสถานะออนไลน์ของใครก็ตามเปลี่ยนจะสั่ง re-render หน้าแชททั้งห้องแม้ไม่เกี่ยวกับคนที่กำลังคุยด้วยเลย) และบังคับเลื่อนไปข้อความล่าสุดทุกครั้งที่สลับห้องแชท สาขาแต่ละสาขาแสดงจำนวนสมาชิกเหมือนกลุ่มแล้ว หน้าต่างแชทแยกมีแถบหัวสีกรมของโปรแกรมเต็มความกว้างแล้ว (เดิมเว้นระยะขอบทำให้ไม่เต็มแถบ) แก้สีตัวอักษรลิงก์ไฟล์แนบและพื้นหลังหน้าตั้งค่าที่ไม่ตรงธีมมืด

Fixed double-left-click on a conversation not detaching it — the real cause was the first click clearing and rebuilding the entire sidebar list (to update the unread badge), which made Qt miss the double-click gesture. Selecting an existing row now updates it in place instead. Fixed the jump back to the top while scrolled to the bottom by cutting unnecessary re-renders (previously, anyone's presence changing re-rendered the open chat even when unrelated to it) and now force the view to the latest message every time you switch conversations. Branches show a member count just like groups. Detached chat windows' navy title bar now spans the full width (it was inset by unset layout margins before). Fixed the attachment-filename link color and the settings page background not following dark mode.

## รุ่น 3.5.0: ภาษาไทย / English

เลือกภาษาที่ **ตั้งค่าและวิธีใช้ → ภาษา / Language** หน้าจอและ Tray เปลี่ยนทันที และจำภาษาเมื่อเปิดครั้งถัดไป โดยไม่เปลี่ยนกฎ คิว หรือตารางเวลา ช่องตัวเลขใช้ 0–9 ทั้งสองภาษา ชื่องานและเส้นทางไม่ถูกแปล รายละเอียด Log เดิมคงข้อความที่บันทึกไว้ ข้อผิดพลาดจากระบบปฏิบัติการอาจใช้ภาษาของระบบ

Choose **Settings and help → ภาษา / Language** to switch immediately between Thai and English. The choice is remembered. Numeric fields always use ASCII digits (0–9). Job names, paths and existing log messages are preserved. Operating-system errors may use the system language.

## คิวงานและตัวติดตั้ง

หน้าตั้งค่างานแสดงเฉพาะรายการที่เกี่ยวข้อง ลบอย่างเดียวไม่มีต้นทาง; Copy มีตัวเลือกไฟล์ซ้ำ; Backup แสดงอายุชุดเมื่อเปิดลบชุดเก่า; Sync แสดงตัวเลือกลบส่วนเกิน ช่องวันและชั่วโมงซ่อนตามความถี่ที่เลือก ค่าที่ไม่เกี่ยวข้องจะไม่ถูกนำไปใช้เมื่อบันทึก

สร้างตัวติดตั้งด้วย Inno Setup 6.4.3: `ISCC.exe installer\BackupKeeper.iss` หลังสร้าง EXE แล้ว ตัวติดตั้งทดสอบติดตั้งและถอนออกในโฟลเดอร์ทดสอบแยก โดยไม่เปิด autostart และไม่แตะข้อมูล Backup จริง

- `iSmartWorkplace.exe` เปิดใช้งานทันที ข้อมูลยังเก็บใน LocalAppData ของผู้ใช้ ไม่ใช่โหมดเก็บข้อมูลข้าง EXE
- `iSmartWorkplace-Setup.exe` ติดตั้งต่อผู้ใช้ใน LocalAppData/Programs พร้อม Start Menu, ทางเลือก Desktop shortcut, ทางเลือกเริ่มใน Tray เมื่อ sign in และรายการถอนการติดตั้ง ไม่ต้องใช้สิทธิ์ Administrator
- สำหรับองค์กรใช้ `/VERYSILENT /SUPPRESSMSGBOXES /NORESTART /TASKS="autostart"` ได้ในบริบทบัญชีผู้ใช้เป้าหมาย หากไม่ต้องการเริ่มพร้อมระบบใช้ `/TASKS=""` ไม่ใช่การติดตั้ง all-users หรือ Windows service
- ใช้โลโก้จากผู้พัฒนา และมีลิงก์ [Chiotron](https://chiotron.com/th) ในแอปและตัวติดตั้ง
- งานที่สั่งเองเข้าคิว FIFO ใน SQLite สูงสุด 100 งาน ปฏิเสธคิวซ้ำ กฎที่แก้ไข/ลบจะยกเลิกสำเนาที่รอไว้ งานตามเวลาจะเลือกเวลาที่ค้างนานที่สุดก่อน
- คิวที่ยังรออยู่จะคงอยู่เมื่อเปิดแอปใหม่ ส่วนงานที่ส่งให้ worker แล้วแต่ถูกขัดจังหวะจะไม่รันซ้ำอัตโนมัติ ให้ตรวจ Log ก่อนสั่งใหม่
- ปุ่มพักตารางเวลาพักเฉพาะงานตามเวลา งานที่ผู้ใช้กดเข้าคิวเองยังทำต่อ ใช้หน้า “ข้อมูล → ยกเลิกงานที่รอทั้งหมด” เพื่อยกเลิกคิว งานปัจจุบันหยุดแยกด้วยปุ่มหยุดงาน
- งานลบอ่านข้อมูลแบบไล่รายการ งานโอนข้อมูลเก็บรายการเพื่อเปรียบเทียบ แต่จำกัดประมาณ 100,000 รายการต่อโฟลเดอร์หลักเพื่อควบคุมหน่วยความจำ หากเกินให้แยกโฟลเดอร์เป็นหลายกฎ
- งานลบมีขีดจำกัด 100,000 รายการต่อรอบ หากถึงขีดจำกัดจะหยุดและแจ้งใน Log ไฟล์ที่ลบสำเร็จก่อนถึงขีดจำกัดไม่ย้อนกลับ การลบโฟลเดอร์ว่างจะถูกข้าม
- อ่าน/คัดลอกเนื้อหาเป็นบล็อก 1 MB ทำทีละงานใน worker แยกจากหน้าจอ ไม่รับประกันว่าเครื่องจะไม่ค้างหรือโปรแกรมไม่ล้มในทุกสถานการณ์ หาก OS/NAS ค้างใน I/O การหยุดงานอาจต้องรอ แอปจะแสดงข้อความเมื่อ worker ไม่เดินหน้ามากกว่า 60 วินาที
- ไม่รันหลัง logout และไม่ใช่ service ตัวติดตั้งไม่เปลี่ยนข้อจำกัดนี้ ยังต้องมีผู้ใช้ sign in และเครื่องไม่หลับ

ตัวติดตั้งยังไม่มีลายเซ็นดิจิทัล และยังต้องทดสอบในสภาพแวดล้อมองค์กรจริงก่อนกระจายวงกว้าง
ค่าที่กรอกถูกต้องสำหรับการเชื่อมต่อแบบ manual (ข้าม VLAN) ที่ใช้งานอยู่ตอนนี้:
- ช่อง	ค่าที่กรอก	ถูกต้องไหม
- IP ของ Server	192.168.x.x	✅
- พอร์ต Server	48731	✅ (ค่ามาตรฐาน)
- SHA-256 ของ Server	93556bb7... (64 ตัวอักษร)	✅
- IP เครื่องนี้	0.0.0.0	✅ (รับทุกการ์ดเครือข่าย)
- พอร์ตรับข้อความ	48733	✅ (ค่ามาตรฐาน)
- ✅ Checkbox ตรวจ SHA	ติ๊กแล้ว	✅

แอปเดสก์ท็อปภาษาไทยสำหรับลบไฟล์เก่า คัดลอก สร้างชุด Backup และ Sync ทางเดียว เปลี่ยนหน้าจอเป็น Qt พร้อมปุ่มโค้งมน กรอบ เงา ไอคอน และการปรับสเกลหน้าจอ

### ติดตั้ง / อัปเดต

1. **เครื่องแม่ Server:** แตกไฟล์ `iSmartWorkplace-3.6.0-Windows-x64.zip` แล้วดับเบิ้ลคลิก `iSmartWorkplace-Server.exe` (ไม่ต้องปิด เปิดทิ้งไว้) แล้วดับเบิ้ลคลิกใช้เลย `iSmartWorkplace.exe` หรือติดตั้งตัว `iSmartWorkplace-Setup` (สำหรับแชทในองค์กร)
2. **เครื่องลูก:** คัดลอก `iSmartWorkplace.exe` ไปไว้ในตำแหน่งถาวร ไม่ต้องติดตั้ง Python ดับเบิ้ลคลิกใช้เลย หรือติดตั้งตัว Setup (สำหรับแชทในองค์กร)
3. **ฟังก์ชั่น Backup:** ดับเบิ้ลคลิกใช้เลย หรือติดตั้งตัว Setup ไม่ต้องทำอย่างอื่น
4. กฎเก่าจะปรากฏในเมนู โฟลเดอร์และตารางเวลา เป็นงานลบอย่างเดียว ใช้เกณฑ์วันที่และสถานะเปิด/ปิดเดิม แนะนำพักตารางเวลาในรุ่นเก่าก่อนอัปเดตเพื่อมีเวลาตรวจสอบ
5. เริ่มด้วยทดลองสแกน ตรวจรายการใน **ประวัติการทำงาน → ดูรายละเอียด / CSV** แล้วจึงเปลี่ยนเป็นทำงานจริงและเปิดตารางเวลา
6. ปิดหน้าต่างเพื่อย่อไป Tray เปิด/พักตารางเวลาและออกจากโปรแกรมได้จากเมนู Tray หากเครื่องไม่มี Tray จะย่อหน้าต่างแทน
7. **ตั้งค่าและวิธีใช้ → เปิดโปรแกรมใน Tray เมื่อเข้าสู่ระบบ Windows:** ใช้กับบัญชีผู้ใช้ปัจจุบัน หากย้าย EXE ไปที่ใหม่ให้ปิดแล้วเปิดตัวเลือกนี้อีกครั้ง

> **EXE ยังไม่มีลายเซ็นดิจิทัล ต้องใช้งานตามนโยบายซอฟต์แวร์ขององค์กร**

## เลือกประเภทงาน

| งาน | พฤติกรรม | การลบของเก่า |
|---|---|---|
| ลบอย่างเดียว | เลือกโฟลเดอร์ อายุ วัน/เดือน/ปี วันที่สร้างหรือ Date modified และรวมโฟลเดอร์ย่อย | ถังขยะหรือลบถาวรตามที่เลือก |
| Copy | คัดลอกทุกชั้น ต้นทางคงอยู่ เลือกข้ามหรือแทนที่ไฟล์ซ้ำ | ไม่ลบส่วนเกิน หากต้องการเก็บหลายรุ่นให้เลือก Backup |
| Backup | สำเนาครบชุดแยกโฟลเดอร์ `BK-วันเวลา-รหัส` ทุกครั้ง | เลือกอายุชุดเก่าได้ ลบถาวรหลังชุดใหม่สำเร็จ เฉพาะชุดของงานนี้ที่ลงทะเบียนไว้ |
| Sync ทางเดียว | ตรวจ SHA-256 และแทนที่ไฟล์ปลายทางเมื่อเนื้อหาต่างกัน | ค่าเริ่มต้นเก็บส่วนเกิน เปิดตัวเลือกลบไฟล์ที่ไม่มีในต้นทางได้โดยยืนยันความเสี่ยง |

สำหรับ Copy/Sync ที่ต้องลบตามอายุแยกต่างหาก สามารถสร้างงานลบอย่างเดียวได้ แต่ควรหลีกเลี่ยงกฎทับซ้อนที่อาจลบไฟล์ซึ่งเพิ่งคัดลอก (เช่น ไฟล์ต้นทางมี Date modified เก่า) ใช้ Backup พร้อมอายุชุดเก่าจะเหมาะกับการเก็บย้อนหลังมากกว่า

## ทดลองก่อนเปลี่ยนข้อมูล

งานใหม่เป็น **ทดลองเท่านั้น** และปิดตารางเวลาไว้ กดทดลองสแกนได้ทุกเมื่อ แม้กฎตั้งเป็นทำงานจริง รายการจะแยกว่า **จะคัดลอก / จะแทนที่ / จะสร้างโฟลเดอร์ / จะลบส่วนเกิน / จะลบชุดเก่า** การทดลองไม่สร้างไฟล์ปลายทาง ผลจริงตรวจใหม่ตอนรัน อาจเปลี่ยนไปตามข้อมูล ณ เวลานั้น

ระบบแสดงรายละเอียดก่อนบันทึก/เปิดงานจริง ก่อนรันเอง ก่อนเปิดตารางเวลาต่อ และก่อนเปิดเริ่มพร้อม Windows สำหรับงานที่เปลี่ยนข้อมูล คำถามเริ่มที่ตัวเลือกปฏิเสธ การลบหรือแทนที่ถาวรต้องพิมพ์ **DELETE** ให้ตรง การยกเลิกหรือพิมพ์ผิดจะไม่ผ่าน หลังยืนยันเปิดตารางเวลาแล้วจะไม่ถามซ้ำแต่ละรอบ

## การปกป้องข้อมูล

- ต้นทางและปลายทางต้องมีอยู่จริง แยกกัน และไม่เป็นที่เดียวกันหรือซ้อนกัน ไม่เลือกทั้งไดรฟ์หรือโฟลเดอร์ระบบ
- Copy/Backup/Sync ไม่ลบต้นทาง คัดลอกผ่านไฟล์ชั่วคราว ตรวจ SHA-256 แล้วจึงนำไปใช้ ไฟล์ที่คัดลอกไม่ครบจะไม่แทนที่ไฟล์เดิม
- การแทนที่ไฟล์ การลบส่วนเกิน และการลบชุด Backup เก่าไม่ผ่านถังขยะ
- พบต้นทาง/ปลายทางอ่านไม่ได้ link/junction ไฟล์ชนิดพิเศษ หรือข้อมูลเปลี่ยนระหว่างงานโอนข้อมูล จะหยุดและบันทึกข้อผิดพลาด ขั้นตอนลบส่วนเกินหรือชุดเก่าจะไม่เริ่มหากการคัดลอก/ตรวจต้นทางไม่สำเร็จ
- ต้นทางว่างจะไม่อนุญาต Sync แบบลบส่วนเกิน หรือ Backup ที่เปิดลบชุดเก่า เพื่อป้องกันกรณีไดรฟ์/โฟลเดอร์ที่ไม่พร้อม
- Copy/Sync สำเร็จเป็นรายไฟล์ หากภายหลังงานล้มเหลว ไฟล์ที่คัดลอกสำเร็จก่อนหน้าไม่ย้อนกลับ ระบบนี้ไม่ใช่ transaction ครอบคลุมทั้งต้นไม้โฟลเดอร์
- Backup ที่ล้มเหลวอาจมี `.bk-incomplete-*` เก็บไว้ตรวจสอบ ไม่ถูกนับเป็นชุดสำเร็จและไม่ลบอัตโนมัติ ชุดที่สร้างเสร็จแต่เครื่องดับก่อนลงทะเบียนก็จะไม่ถูกเก็บกวาดอัตโนมัติ
- ลบ Backup เก่าจากทะเบียนใน SQLite เท่านั้น ไม่ค้นจากชื่อ `BK-*` อย่างเดียว ไม่ลบข้อมูลจากภายนอก ถ้าชุดเก่ามีไฟล์เพิ่ม/หาย/เนื้อหาเปลี่ยนจะเก็บชุดนั้นไว้และแจ้งข้อผิดพลาด
- ชุดที่หยุดระหว่างการลบจะมีสถานะ `deleting` ให้ตรวจเอง ไม่ลบต่อเงียบ ๆ ในรอบหน้า การลบชุดเก่าเป็นรายไฟล์และอาจสำเร็จบางส่วนก่อนเกิดข้อผิดพลาด
- ไม่มี VSS, database-aware backup, การล็อกโฟลเดอร์ต้นทาง หรือการสำรอง ACL/owner/ADS อย่างครบถ้วน เป็นการคัดลอกเนื้อหาและ metadata พื้นฐาน ควรใช้ไฟล์ `.bak` ที่ระบบฐานข้อมูลเขียนเสร็จแล้วและตั้งรอบไม่ชนกับการเขียนข้อมูล
- ตรวจเส้นทางและไฟล์ซ้ำก่อนเปลี่ยนข้อมูล แต่ไม่มีการรับประกันกับโปรแกรมอื่นที่เปลี่ยนต้นไม้โฟลเดอร์พร้อมกัน ควรจำกัดสิทธิ์เขียนให้บัญชีที่เชื่อถือได้

## งานลบอย่างเดียวและโฟลเดอร์ว่าง

ค่าเริ่มต้นใช้วันที่สร้างบนระบบไฟล์ปลายทาง วันที่นี้อาจเปลี่ยนเมื่อคัดลอก เลือก **วันที่แก้ไขล่าสุด (Date modified)** ได้ ไม่อ่านวันที่จากชื่อไฟล์ ถ้าอ่านวันที่สร้างไม่ได้จะข้ามพร้อม Log ไม่ใช้วันที่อื่นแทนโดยเงียบ ๆ

อายุต้องเก่ากว่าเกณฑ์จริง ไม่รวมเวลาเท่ากันพอดี เดือน/ปีคำนวณตามปฏิทิน ถังขยะที่ใช้ไม่ได้ (เช่น บาง NAS) จะเกิดข้อผิดพลาด ไม่มีการเปลี่ยนไปลบถาวร

เลือกลบโฟลเดอร์ย่อยที่ว่างทุกชั้นได้ ปิดเป็นค่าเริ่มต้น รวมที่ว่างอยู่แล้วทุกอายุและไม่ใช้วันที่โฟลเดอร์ตัดสิน ลบโฟลเดอร์ว่างถาวรแม้ส่งไฟล์ลงถังขยะ เก็บโฟลเดอร์หลักไว้ หากมีไฟล์ใหม่เข้ามา โฟลเดอร์นั้นจะลบไม่ได้ หากสแกนมีข้อผิดพลาดหรือหยุดงานจะข้ามขั้นตอนนี้

## ตารางเวลา / สถานะ

แต่ละงานเลือกทุกวัน ทุกสัปดาห์ หรือทุก N ชั่วโมง แยกกันได้ ใช้เวลาท้องถิ่นของเครื่อง ชั่วโมงเริ่มนับเมื่อบันทึก/เปิดงาน การแก้ไขจะคำนวณรอบใหม่

ต้องเปิดแอปค้างไว้ เครื่องต้องเปิดและไม่หลับ ไม่ใช่ Windows service และไม่ทำงานหลัง logout รอบที่พลาดจะรันหนึ่งครั้งเมื่อแอปกลับมา งานรันเรียงกันครั้งละหนึ่งงาน ปุ่มพักตารางเวลาหยุดเฉพาะการเริ่มงานใหม่ ปุ่มหยุดงานปัจจุบันหยุดเมื่อพ้นขั้นตอนที่กำลังดำเนินอยู่ (I/O เครือข่ายอาจต้องรอ)

Tray และ popup ขึ้นกับระบบแจ้งเตือนของ OS เปิดได้หนึ่ง instance ต่อบัญชีผู้ใช้ ควรใช้บัญชีเดียวดูแลโฟลเดอร์ชุดเดียวกัน

## ข้อมูลและ Log

- Windows: `%LOCALAPPDATA%\BackupKeeper`
- macOS: `~/Library/Application Support/BackupKeeper`
- Linux: `$XDG_DATA_HOME/BackupKeeper` หรือ `~/.local/share/BackupKeeper`

`keeper.sqlite3` เก็บกฎ ประวัติ และทะเบียนชุด Backup สำคัญต่อการลบชุดเก่า ปิดแอปก่อนสำรองฐานข้อมูลหรือย้ายเครื่อง กฎเก่ายังใช้ได้ แต่ไม่ควรเปิดรุ่น 1.x หลังสร้างงานชนิดใหม่ในรุ่น 2.0

ประวัติแสดง 500 งานล่าสุด รายละเอียดแสดง 5,000 รายการแรก ส่งออก CSV ได้ทั้งหมด Log ไม่ลบอัตโนมัติ `pending` หมายถึงผลยังไม่ยืนยันหากงานถูกขัดจังหวะ ตรวจไฟล์จริงด้วย `application.log` เก็บข้อผิดพลาดของแอปและหมุนเวียนไฟล์เอง

ถอนการใช้งานโดยปิดตัวเลือกเริ่มพร้อม Windows ออกจากโปรแกรม แล้วลบ EXE ฐานข้อมูลยังอยู่จนกว่าจะลบด้วยตนเอง

## OS และข้อจำกัดการทดสอบ

สร้างและทดสอบบน Windows 10 x64 build 19045 เป้าหมาย EXE นี้คือ Windows 10/11 x64 โดย Qt 6.8 ระบุ Windows 10 1809 ขึ้นไปใน [แพลตฟอร์มที่รองรับ](https://doc.qt.io/qt-6.8/windows.html)

Windows Server, NAS/UNC, macOS และ Linux ยังไม่ได้ทดสอบจริง ต้องทดสอบกับรุ่น OS/สิทธิ์/ระบบไฟล์ของเครื่องปลายทางก่อนเปิดงานจริง ไม่รองรับ Server Core ที่ไม่มีหน้าจอในรุ่นนี้ ซอร์สใช้ Qt และ Python ที่นำไป build แยก OS ได้ แต่ Windows EXE ใช้ข้าม OS ไม่ได้

## Build / ตรวจสอบ

Python 3.10+ พร้อม dependencies ใน `requirements-dev.txt`:

```powershell
python -m pip install -r requirements-dev.txt
python -m pytest -q
python tools/render_ui.py
python -m PyInstaller --noconfirm --clean --onefile --windowed --distpath dist/v3.6.0 --name BackupKeeper --collect-submodules send2trash --exclude-module numpy --exclude-module tkinter main.py
```

หรือรัน `build-windows.ps1` ซึ่งสร้าง virtual environment แล้วทดสอบก่อน build ไม่ต้องใช้สิทธิ์ Administrator ซอร์ส Tkinter รุ่นก่อนเก็บไว้สำหรับการทดสอบย้อนหลัง แต่ EXE 3.6.0 ใช้ `backup_cleaner/qt_app.py` เท่านั้น ภาพหน้าจอจาก Qt อยู่ใน `artifacts/screenshots`
