# mq2-sensor-basic
ตัวอย่างโค้ดอ่านค่า **MQ-2 (LPG/Smoke)** ด้วย **ESP32 (ADC1)** พร้อมกรองสัญญาณ (Moving Average) และ **Hysteresis** เพื่อลดอาการไฟกระพริบ/สัญญาณไม่นิ่ง

# ESP32 + MQ-2 Basic Alarm (Deva DIY)

ตัวอย่างโค้ดอ่านค่า **MQ-2 (LPG/Smoke)** ด้วย **ESP32 (ADC1)** พร้อมกรองสัญญาณ (Moving Average) และ **Hysteresis** เพื่อลดอาการไฟกระพริบ/สัญญาณไม่นิ่ง

- ใช้ขา `GPIO34` (ADC1) เพื่อหลีกเลี่ยงปัญหาชนกับ Wi-Fi
- ปรับ `analogSetAttenuation(ADC_11db)` เมื่อเอาต์พุตเซนเซอร์อยู่ในช่วง 0–3.3V
- มี `GAS_TH_HI / GAS_TH_LO` สำหรับ hysteresis

👉 **Full tutorial (ภาษาไทย):** [อ่านบทความฉบับเต็มที่ DevaDIY](https://www.devadiy.com/esp32-mq2/)  
(อธิบายการต่อวงจร, การตั้งค่า, คาลิเบรต, FAQ ครบ)

## Wiring
| MQ-2 Module | ESP32        |
|-------------|--------------|
| AO (Analog) | GPIO34 (ADC1)|
| VCC         | 5V* หรือ 3.3V** |
| GND         | GND          |

\* โมดูล MQ-2 หลายรุ่นใช้ฮีตเตอร์ 5V แต่เอาต์พุตสัญญาณอาจเกิน 3.3V → **ต้องมีตัวแบ่งแรงดัน** ถ้าอ่านเข้าขาอนาล็อก ESP32  
\** หากเป็นบอร์ดที่ออกแบบให้รองรับ 3.3V เต็มระบบ ให้ดูสเปกผู้ผลิตอีกครั้ง

## Build
- Board: `ESP32 Dev Module`
- Upload Speed: 921600 (แนะนำ)
- Arduino IDE หรือ PlatformIO ได้ทั้งคู่

## License
MIT

---
## 🌱 DevaDIY
เรียนรู้ ESP32 + Smart Farm + IoT เพิ่มเติมได้ที่ [DevaDIY.com](https://devadiy.com)

ติดตามโครงการและโค้ดอื่น ๆ ได้ที่:
- เว็บไซต์: [https://devadiy.com](https://devadiy.com)
- YouTube: [Deva DIY](https://youtube.com/@devadiy)
- TikTok: [@devadiy](https://www.tiktok.com/@devadiy)
