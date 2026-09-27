[![GitHub release (latest by date)](https://img.shields.io/github/v/release/MeteAvci/.gemini?style=for-the-badge&color=0078D6)](https://github.com/MeteAvci/.gemini/releases)
[![MIT License](https://img.shields.io/badge/License-MIT-0078D6.svg?style=for-the-badge)](LICENSE)
[![Windows](https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white)](https://www.microsoft.com/windows)
[![Linux](https://img.shields.io/badge/Linux-0078D6?style=for-the-badge&logo=linux&logoColor=white)](https://www.linux.org/)
[![macOS](https://img.shields.io/badge/macOS-0078D6?style=for-the-badge&logo=apple&logoColor=white)](https://www.apple.com/macos)
[![Google Antigravity](https://img.shields.io/badge/Google%20Antigravity-0078D6?style=for-the-badge&logo=google&logoColor=white)](https://github.com/google)
[![Google Gemini](https://img.shields.io/badge/Google%20Gemini%203.8-0078D6?style=for-the-badge&logo=googlegemini&logoColor=white)](https://deepmind.google/technologies/gemini/)

# .gemini — Sovereign AI Agent Configuration & Runtime v2.0

<details>
<summary>🇹🇷 Türkçe Dokümantasyon için buraya tıklayın!</summary>

---

# Gemini CLI & Google Antigravity için .gemini Yapılandırma Rehberi
### *Egemen Ajan Mimarisi, Sınırlı Otonomi (Bounded Execution) ve Doğruluk Protokolü*

Bu repository, kişisel AI aracımın yapılandırma ve anayasa merkezidir. **Google Antigravity platformu** ve **Gemini CLI** motoru için özel olarak hazırlanmış olup, her geliştiricinin kendi projelerinde doğrudan kullanabileceği genel standartlara sahiptir.

---

### 🚀 Son Güncelleme (v2.0) - "Sovereign Agent & Bounded Runtime"

- **Model ve Dinamik Akıl Yürütme:** Varsayılan model `Gemini 3.8 Flash (High)` dinamik akıl yürütme motoruyla hizalandı. "Model ID Anayasa Değildir" ilkesiyle anayasa, model adından bağımsız bir yetenek rotalama yapısına (Capability Routing) kavuşturuldu.
- **Context Doktrini (1M ≠ 1M Doldurmak):** 1.000.000 tokenlik pencereyi ham sohbet geçmişiyle şişirip modeli amneziye ("Lost-in-the-Middle") uğratmak yerine; sistem anayasası, araç şemaları ve repo mimarisi Google Context Caching (TTL) önekine alındı. Her turda yalnızca odaklanılmış canlı görev ve kanıtlar taşınır.
- **Bounded Execution (Kör YOLO'nun Sonu):** Antik ve kontrolsüz YOLO modu (`agentYoloMode: true`) emekliye ayrıldı. Yerine `disableYoloMode: true` + Antigravity Sandbox (`proceed-in-sandbox`) ile hem otonom hem de sınırları korumalı güvenli çalışma disiplini getirildi.
- **İddia ≠ Kanıt (`Claim ≠ Proof`):** Modelin metin olarak "testler geçti" demesi yalnızca bir iddiadır. Yalnızca makine tarafından gözlemlenebilir çıkış kodu 0, temiz linter çıktıları ve başarıyla tamamlanan test suite'leri kanıt sayılır.
- **Temiz PowerShell 7:** Windows'ta terminal körlüğünü ve kaçış kodlarını önleyen `-NoLogo -NoProfile` temiz profil standardı getirildi (`pwsh`).
- **Akıllı Bağlam Filtresi (`.geminiignore`):** `node_modules`, `dist`, `coverage`, cache gibi token israfı yaratan klasörleri izole eden, ancak `package-lock.json` ve `pnpm-lock.yaml` gibi bağımlılık kilitlerini kanıt olarak koruyan filtre eklendi.

---

### 🚀 Önceki Güncellemeler

<details>
<summary>Önceki Sürüm Notları (v1.4, v1.3, v1.2, v1.1)</summary>

#### v1.4 - "Kanıt Öncelikli Derin Doğrulama"
- **Araştırma Tamamlama Kapısı:** AI artık araştırmayı birkaç link açmak olarak saymıyor. En güncel resmi dokümantasyonu bulması, tarih/sürüm bağlamını çıkarması ve canlı yerel kodla kıyaslaması zorunlu kılındı.
- **Kaynak Öncelik Merdiveni:** Güven sırası: Resmi dokümanlar > Resmi release notes > Resmi repo/referanslar > Canlı yerel kod > Resmi issue tracker > Topluluk kaynakları.
- **Araç Esnekliği:** Native araçlar hız ve güvenlik sağlıyorsa kullanılacak; aksi halde `pwsh` veya `bash` komutlarına doğrudan geçilecek.
- **Sıfır-Güven Doğrulaması:** Kod değişikliğinden sonra test, linter veya derleme kontrolleri zorunlu hale getirildi.

#### v1.3 - "Otonomi ve Gerçeklik Protokolü (The Truth Protocol)"
- **Mental Yükseltme:** `ULTRA-PRO-MAXIMUM-OVERCLOCK MODE` ve `thinking_level: "high"` aktif edildi.
- **Diyalog Senkronizasyonu:** Kullanıcı bir soru sorduğunda, AI araç çalıştırmayı bekletip önce doğal dille yanıt verir.
- **Kronolojik Keşif:** Ne vardı ➔ Ne değişti ➔ Şimdi ne canlı ➔ Bunu ne kanıtlıyor sırasıyla canlı dosya incelemesi.

#### v1.2 - "Sistem Mimarisi Yeniden Tasarımı"
- **Modüler Mimari:** Domain-driven klasör yapısı, tek sorumluluk ilkesi, küçük dosyalar ve derin hiyerarşi zorunlu kılındı.
- **Pozitif Dil:** Kurallar net, yapıcı ve doğrudan uygulanabilir talimatlara dönüştürüldü.

#### v1.1 - "Avcı Güncellemesi (The Predator Protocol)"
- **Karşı İstihbarat:** Prompt injection ve zararlı kod girişimlerini yakalayıp temizleme protokolü eklendi.
- **Güvenli Yazma Protokolü:** `replace_file_content` yerine tam dosya okuma-dönüştürme-yazma (Read-Transform-Write) standardı getirildi.
- **Çift Sıcaklık:** Sohbet için yaratıcı (`chat_temperature: 1.0`), kod için deterministik (`temperature: 0.1`) yapılandırma.

</details>

---

### 📂 Dosya Yapısı

```text
.gemini/
├── GEMINI.md       # ÇeteGPT v2.0 Sistem Anayasası & Karakter Talimatları
├── settings.json   # Antigravity & Gemini CLI için optimize edilmiş editör ve çalışma alanı ayarları
├── .geminiignore   # LLM bağlamını çöplerden koruyan akıllı yoksayma listesi
├── .gitignore      # Git versiyon kontrol istisnaları
├── README.md       # Detaylı mimari ve kurulum rehberi
└── LICENSE         # MIT Açık Kaynak Lisansı
```

---

### 🛠️ Kurulum

*   **Windows:**
    1.  `Win + R` tuşlarına basın, `%USERPROFILE%` yazın ve Enter'a basın.
    2.  Mevcut değilse `.gemini` adında bir klasör oluşturun.
    3.  Repo içerisindeki `GEMINI.md`, `settings.json` ve `.geminiignore` dosyalarını `%USERPROFILE%\.gemini\` klasörüne kopyalayın.
    4.  Antigravity IDE veya Gemini CLI oturumunuzu yeniden başlatın.

*   **macOS / Linux:**
    ```bash
    git clone https://github.com/MeteAvci/.gemini.git ~/.gemini
    # veya dosyaları doğrudan ~/.gemini klasörünüze kopyalayın
    ```

---

### 🧠 Ayarlar Rehberi (`settings.json`)

#### 1. Zeka ve Model Ayarları
| Ayar | Değer | Açıklama |
|---|---|---|
| `model.name` | `"Gemini 3.8 Flash (High)"` | Yüksek akıl yürütme ve geniş bağlam sunan aktif model. |
| `model.thinkingLevel` | `"high"` | Karmaşık mimari analizler için dinamik düşünme modu. |
| `model.compressionThreshold` | `0.7` | Bağlamın %70'ine ulaşılana kadar erken sıkıştırmayı önler. |

#### 2. Güvenlik ve Sınırlı Otonomi
| Ayar | Değer | Açıklama |
|---|---|---|
| `security.toolSandboxing` | `true` | Terminal araçlarını korumalı sandbox içinde çalıştırır. |
| `security.disableYoloMode` | `true` | Kontrolsüz kör çalıştırmayı engeller, sınırları belirler. |
| `general.defaultApprovalMode` | `"default"` | Güvenli araçlara otomatik izin verir, riskli eylemleri denetler. |

#### 3. Terminal ve Editör Performansı
| Ayar | Değer | Açıklama |
|---|---|---|
| `terminal.integrated.shellIntegration.enabled` | `true` | Editör terminal entegrasyonu. |
| `terminal.integrated.profiles.windows` | `pwsh -NoLogo -NoProfile` | Windows terminalinde escape kodlarının ajanı kör etmesini önler. |
| `files.autoSave` | `"onFocusChange"` | Ajan dosya okurken kullanıcının yazmasından doğan çakışmaları (race condition) engeller. |
| `typescript.tsserver.experimental.enableProjectDiagnostics` | `true` | Tüm projenin LSP üzerinden tip güvenliğini sağlar. |
| `editor.minimap.enabled` | `false` | GPU yükünü azaltır, kod okuma alanını genişletir. |

</details>

---

## Architecture Overview (English)

This repository serves as the universal configuration and constitutional core for my personal AI engineering setup. Built specifically for **Google Antigravity** and the **Gemini CLI** engine, it establishes an evidence-backed, high-performance runtime accessible to any developer.

### 🚀 Highlights of v2.0

1. **Model & Dynamic Reasoning:**
   Anchored to `Gemini 3.8 Flash (High)`. Under the "Model ID is Not Constitution" principle, operational rules govern capability profiles and reasoning effort rather than tying behavior to a single fleeting model name.

2. **Context Doctrine (1,000,000 Tokens ≠ 1,000,000 Tokens to Stuff):**
   A 1M token context window is capacity, not a dumping ground. Monolithic context stuffing causes Lost-in-the-Middle amnesia. System rules and repository structure are cached at the prefix via Google Context Caching (TTL-based), while active turns carry only focused objectives and concrete evidence.

3. **Bounded Execution (Retiring YOLO):**
   Unconstrained `agentYoloMode: true` is deprecated. In its place sits a governed autonomy model: `disableYoloMode: true` combined with Antigravity's `proceed-in-sandbox` architecture for reliable, safe execution.

4. **Claim ≠ Proof:**
   A prose claim that code works is not proof. Only machine-observable receipts (exit code 0, passing test suites, clean type checks) constitute proof.

5. **Clean PowerShell 7 Environment:**
   Configured `pwsh -NoLogo -NoProfile` on Windows to eliminate custom prompt artifacts and ANSI escape sequences that blind AI scrapers.

6. **Intelligent Context Hygiene (`.geminiignore`):**
   Isolates noisy build artifacts, virtual environments, and caches while explicitly protecting dependency lockfiles (`package-lock.json`, `pnpm-lock.yaml`) as immutable evidence.

---

### 📂 Repository Structure

```text
.gemini/
├── GEMINI.md       # ÇeteGPT v2.0 System Constitution & Persona Directives
├── settings.json   # Optimized runtime & workspace settings for Gemini CLI & Antigravity
├── .geminiignore   # Context hygiene filter to protect LLM context from build noise
├── .gitignore      # Git tracking exclusions
├── README.md       # Comprehensive documentation and setup guide
└── LICENSE         # MIT Open Source License
```

---

### 🛠️ Installation

*   **Windows:**
    1.  Press `Win + R`, type `%USERPROFILE%`, and press Enter.
    2.  Create a folder named `.gemini` if it doesn't already exist.
    3.  Copy `GEMINI.md`, `settings.json`, and `.geminiignore` from this repository into `%USERPROFILE%\.gemini\`.
    4.  Restart your Antigravity IDE or Gemini CLI session.

*   **macOS / Linux:**
    ```bash
    git clone https://github.com/MeteAvci/.gemini.git ~/.gemini
    # or copy the files directly into your ~/.gemini folder
    ```

---

### 🧠 Settings Reference (`settings.json`)

#### 1. Intelligence & Model
| Setting | Value | Description |
|---|---|---|
| `model.name` | `"Gemini 3.8 Flash (High)"` | Primary model combining high throughput and deep reasoning. |
| `model.thinkingLevel` | `"high"` | Dynamic reasoning enabled for complex architectural tasks. |
| `model.compressionThreshold` | `0.7` | Delays aggressive compaction until context reaches 70% capacity. |

#### 2. Security & Bounded Autonomy
| Setting | Value | Description |
|---|---|---|
| `security.toolSandboxing` | `true` | Executes terminal commands within contained sandbox perimeters. |
| `security.disableYoloMode` | `true` | Enforces governed autonomy and prevents blind unchecked mutations. |
| `general.defaultApprovalMode` | `"default"` | Auto-approves safe actions while gating risky operations. |

#### 3. Terminal & Editor Performance
| Setting | Value | Description |
|---|---|---|
| `terminal.integrated.shellIntegration.enabled` | `true` | Clean editor terminal integration. |
| `terminal.integrated.profiles.windows` | `pwsh -NoLogo -NoProfile` | Strips Windows prompt decorations to prevent scraper errors. |
| `files.autoSave` | `"onFocusChange"` | Prevents file read/write race conditions while the agent is editing. |
| `typescript.tsserver.experimental.enableProjectDiagnostics` | `true` | Full project LSP diagnostics across all files. |
| `editor.minimap.enabled` | `false` | Conserves GPU resources and maximizes code reading space. |

---

### 📜 License

Distributed under the MIT License. See [LICENSE](LICENSE) for details.
