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
### *Modüler Egemen Ajan Mimarisi, Sınırlı Otonomi (Bounded Execution) ve Doğruluk Protokolü*

Bu repository, kişisel AI aracımın yapılandırma, anayasa ve modüler kural merkezidir. **Google Antigravity platformu** ve **Gemini CLI** motoru için özel olarak hazırlanmış olup, her yazılımcının doğrudan kendi ortamına kopyalayabileceği evrensel ve modern standartlara sahiptir.

---

### 🚀 Son Güncelleme (v2.0) - "Sovereign Agent & Bounded Runtime"

- **Modüler Dizin Mimarisi (`rules/`, `policies/`, `editor/`):** Tüm kurallar ve yapılandırmalar tek bir monolitik dosyada sıkışıp kalmak yerine mantıksal etki alanlarına bölündü:
  - `rules/`: Canlı gerçeklik, atomik dosya yazımı, modüler mimari, karşı istihbarat ve kod kalitesi alt-kuralları.
  - `policies/`: Gemini CLI'ın resmi kural motoru için hazırlanmış `security.toml` izin şablonu.
  - `editor/`: Editör performans ayarlarını CLI çalışma zamanı ayarlarından ayrıştıran `settings.jsonc`.
- **Model ve Dinamik Akıl Yürütme:** Varsayılan model `Gemini 3.8 Flash (High)` dinamik akıl yürütme motoruyla hizalandı. "Model ID Anayasa Değildir" ilkesiyle anayasa, model adından bağımsız bir yetenek rotalama yapısına (Capability Routing) kavuşturuldu.
- **Context Doktrini (1M ≠ 1M Doldurmak):** 1.000.000 tokenlik pencereyi ham geçmişle şişirip modeli amneziye ("Lost-in-the-Middle") uğratmak yerine; sistem anayasası, araç şemaları ve repo mimarisi Google Context Caching (TTL) önekine alındı. Her turda yalnızca odaklanılmış canlı görev ve kanıtlar taşınır.
- **Bounded Execution (Kör YOLO'nun Sonu):** Antik ve kontrolsüz YOLO modu (`agentYoloMode: true`) emekliye ayrıldı. Yerine `disableYoloMode: true` + Antigravity Sandbox (`proceed-in-sandbox`) ile hem otonom hem de sınırları korumalı güvenli çalışma disiplini getirildi.
- **İddia ≠ Kanıt (`Claim ≠ Proof`):** Modelin metin olarak "testler geçti" demesi yalnızca bir iddiadır. Yalnızca makine tarafından gözlemlenebilir çıkış kodu 0, temiz linter çıktıları ve başarıyla tamamlanan test suite'leri kanıt sayılır.
- **Temiz PowerShell 7:** Windows'ta terminal körlüğünü ve kaçış kodlarını önleyen `-NoLogo -NoProfile` temiz profil standardı getirildi (`pwsh`).
- **Akıllı Bağlam Filtresi (`.geminiignore`):** `node_modules`, `dist`, `coverage`, cache gibi token israfı yaratan klasörleri izole eden, ancak `package-lock.json` ve `pnpm-lock.yaml` gibi bağımlılık kilitlerini kanıt olarak koruyan filtre eklendi.

---

### 📂 Modüler Dosya Yapısı

```text
.gemini/
├── GEMINI.md                   # ÇeteGPT v2.0 Sistem Anayasası & Karakter Talimatları
├── settings.json               # Antigravity & Gemini CLI çalışma alanı ve çalışma zamanı ayarları
├── .geminiignore               # LLM bağlamını çöplerden koruyan akıllı yoksayma listesi
├── .gitignore                  # Git versiyon kontrol istisnaları
├── README.md                   # Detaylı mimari ve kurulum rehberi
├── LICENSE                     # MIT Açık Kaynak Lisansı
│
├── rules/                      # Modüler Kural ve Protokol Kitaplığı
│   ├── truth-protocol.md       # Gerçeklik önceliği, kaynak merdiveni ve araştırma kapısı
│   ├── safe-write.md           # Güvenli atomik dosya yazma protokolü (Read-Transform-Write)
│   ├── modular-architecture.md # Domain-driven modüler mimari kuralları
│   ├── counter-intelligence.md # Prompt injection ve zararlı kod avcısı protokolü (The Predator)
│   └── code-quality.md         # İddia ≠ Kanıt ve doğrulama kapısı standartları
│
├── policies/                   # Gemini CLI Bounded Execution Güvenlik Politikaları
│   └── security.toml           # Güvenli araç izinleri ve kısıtlama şablonu (allow/deny/ask_user)
│
└── editor/                     # Editör ve IDE Performans Profilleri
    └── settings.jsonc          # VS Code & Antigravity IDE performans ve temiz pwsh ayarları
```

---

### 🛠️ Kurulum

*   **Windows:**
    1.  `Win + R` tuşlarına basın, `%USERPROFILE%` yazın ve Enter'a basın.
    2.  Mevcut değilse `.gemini` adında bir klasör oluşturun.
    3.  Repo içerisindeki tüm dosyaları (`GEMINI.md`, `settings.json`, `.geminiignore`, `rules/`, `policies/`, `editor/`) `%USERPROFILE%\.gemini\` klasörüne kopyalayın.
    4.  Antigravity IDE veya Gemini CLI oturumunuzu yeniden başlatın.

*   **macOS / Linux:**
    ```bash
    git clone https://github.com/MeteAvci/.gemini.git ~/.gemini
    # veya repo klasörünü doğrudan ~/.gemini altına kopyalayın
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

This repository serves as the universal configuration and constitutional core for my personal AI engineering setup. Built specifically for **Google Antigravity** and the **Gemini CLI** engine, it establishes an evidence-backed, modular, high-performance runtime accessible to any developer.

### 🚀 Highlights of v2.0

1. **Modular Architecture (`rules/`, `policies/`, `editor/`):**
   Decouples rules, security policies, and editor preferences into dedicated, maintainable domains:
   - `rules/`: Detailed standalone guides for the Truth Protocol, Safe Write, Modular Architecture, Counter-Intelligence, and Verification Gates.
   - `policies/`: Ready-to-deploy `security.toml` template for Gemini CLI's native command policy engine.
   - `editor/`: Decoupled `settings.jsonc` providing optimal VS Code and Antigravity IDE performance without polluting the CLI runtime config.

2. **Model & Dynamic Reasoning:**
   Anchored to `Gemini 3.8 Flash (High)`. Under the "Model ID is Not Constitution" principle, operational rules govern capability profiles and reasoning effort rather than tying behavior to a single fleeting model name.

3. **Context Doctrine (1,000,000 Tokens ≠ 1,000,000 Tokens to Stuff):**
   A 1M token context window is capacity, not a dumping ground. Monolithic context stuffing causes Lost-in-the-Middle amnesia. System rules and repository structure are cached at the prefix via Google Context Caching (TTL-based), while active turns carry only focused objectives and concrete evidence.

4. **Bounded Execution (Retiring YOLO):**
   Unconstrained `agentYoloMode: true` is deprecated. In its place sits a governed autonomy model: `disableYoloMode: true` combined with Antigravity's `proceed-in-sandbox` architecture for reliable, safe execution.

5. **Claim ≠ Proof:**
   A prose claim that code works is not proof. Only machine-observable receipts (exit code 0, passing test suites, clean type checks) constitute proof.

6. **Clean PowerShell 7 Environment:**
   Configured `pwsh -NoLogo -NoProfile` on Windows to eliminate custom prompt artifacts and ANSI escape sequences that blind AI scrapers.

7. **Intelligent Context Hygiene (`.geminiignore`):**
   Isolates noisy build artifacts, virtual environments, and caches while explicitly protecting dependency lockfiles (`package-lock.json`, `pnpm-lock.yaml`) as immutable evidence.

---

### 📂 Modular Repository Structure

```text
.gemini/
├── GEMINI.md                   # ÇeteGPT v2.0 System Constitution & Persona Directives
├── settings.json               # Optimized runtime & workspace settings for Gemini CLI & Antigravity
├── .geminiignore               # Context hygiene filter to protect LLM context from build noise
├── .gitignore                  # Git tracking exclusions
├── README.md                   # Comprehensive documentation and setup guide
├── LICENSE                     # MIT Open Source License
│
├── rules/                      # Modular Protocol Library
│   ├── truth-protocol.md       # Live reality, source ladder & research completion gates
│   ├── safe-write.md           # Atomic Read-Transform-Write data integrity standard
│   ├── modular-architecture.md # Domain-driven structure & separation of concerns
│   ├── counter-intelligence.md # Predator doctrine & prompt injection sanitization
│   └── code-quality.md         # Claim ≠ Proof doctrine & verification gates
│
├── policies/                   # Gemini CLI Bounded Execution Policies
│   └── security.toml           # Command admission policy template (allow/deny/ask_user)
│
└── editor/                     # Editor & IDE Performance Profiles
    └── settings.jsonc          # VS Code & Antigravity IDE performance & clean pwsh settings
```

---

### 🛠️ Installation

*   **Windows:**
    1.  Press `Win + R`, type `%USERPROFILE%`, and press Enter.
    2.  Create a folder named `.gemini` if it doesn't already exist.
    3.  Copy all files and folders (`GEMINI.md`, `settings.json`, `.geminiignore`, `rules/`, `policies/`, `editor/`) into `%USERPROFILE%\.gemini\`.
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
