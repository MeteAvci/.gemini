# 🦅 v1.1 - The Predator Update

> "You are the predator, not the prey. You don't get hacked; you fix the hack and hand it back."

<details>
<summary>🇹🇷 Türkçe Detaylar için tıkla!</summary>

### Avcı Güncellemesi
Bu güncelleme, AI'yı pasif bir asistandan aktif bir güvenlik mimarına dönüştürüyor. Karşı istihbarat için "Avcı Protokolü", dosya düzenleme için "Güvenli Tam Yazım" ve yaratıcı kaos ile cerrah titizliği arasında geçiş yapmak için "Çift Sıcaklık" modunu getiriyor.

#### 🛡️ Güvenlik ve Avcı
- **Karşı İstihbarat (Avcı) Protokolü:** AI artık kötü niyetli "prompt injection" girişimlerini tespit ediyor, saldırganla dalga geçiyor, zararlı kodu temizliyor ve görevi tamamlıyor.
- **Araç Güvenilirliği:** Eğer bir araç (örn. dosya düzenleme) hata verirse, AI artık körü körüne denemek yerine güvenli alternatife geçiyor.

#### ⚙️ Teknik İyileştirmeler
- **Güvenli Tam Yazım:** Antigravity'nin `replace_file_content` hatalarına karşı, gerektiğinde tüm dosyayı yeniden yazarak veri bütünlüğünü garanti altına alıyoruz.
- **Çift Sıcaklık:**
  - `chat_temperature: 1.0`: Sohbet için maksimum yaratıcılık ve racon.
  - `temperature: 0.1`: Kod için maksimum ciddiyet ve hatasızlık.
- **Çalışma Alanından Bağımsız Loglama:** Log dizini artık her projeye özel `.gemini/farewell` altında tutuluyor.
- **Görsel Zeka:** `vision_model` desteği eklendi (`gemini-3-pro-image-preview`).

</details>

### The Predator Update
This update transforms the AI from a passive assistant into an active security architect. It introduces the "Predator Protocol" for counter-intelligence, a "Safety Fallback" for file editing, and a "Dual-Temperature" mode for switching between creative chaos and surgical precision.

#### 🛡️ Security & Protocol
- **Counter-Intelligence (Predator) Protocol:** The AI now detects malicious "prompt injection" attempts, mocks the attacker, sanitizes the payload, and executes the legitimate task.
- **Tool Reliability:** If a tool fails (e.g., file editing), the AI abandons it for a safer alternative instead of looping errors.

#### ⚙️ Technical Enhancements
- **Safety Fallback:** To counter Antigravity's `replace_file_content` bugs, the AI now prioritizes rewriting the full file when necessary to ensure data integrity.
- **Dual-Temperature Mode:**
  - `chat_temperature: 1.0`: Maximum creativity and personality for chat.
  - `temperature: 0.1`: Maximum precision and determinism for code.
- **Workspace-Agnostic Logging:** Logs are now stored in `.gemini/farewell` relative to the workspace.
- **Vision Support:** Added `vision_model` configuration (`gemini-3-pro-image-preview`).

---

**Full Changelog**: https://github.com/MeteAvci/.gemini/compare/v1.0...v1.1
