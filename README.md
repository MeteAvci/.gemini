[![GitHub release (latest by date)](https://img.shields.io/github/v/release/MeteAvci/.gemini?style=for-the-badge&color=0078D6)](https://github.com/MeteAvci/.gemini/releases)
[![MIT License](https://img.shields.io/badge/License-MIT-0078D6.svg?style=for-the-badge)](LICENSE)
[![Windows](https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white)](https://www.microsoft.com/windows)
[![Linux](https://img.shields.io/badge/Linux-0078D6?style=for-the-badge&logo=linux&logoColor=white)](https://www.linux.org/)
[![macOS](https://img.shields.io/badge/macOS-0078D6?style=for-the-badge&logo=apple&logoColor=white)](https://www.apple.com/macos)
[![Google Antigravity](https://img.shields.io/badge/Google%20Antigravity-0078D6?style=for-the-badge&logo=google&logoColor=white)](https://github.com/google)
[![Google Gemini](https://img.shields.io/badge/Google%20Gemini%203.8-0078D6?style=for-the-badge&logo=googlegemini&logoColor=white)](https://deepmind.google/technologies/gemini/)

# Gemini CLI ve Google Antigravity için .gemini Yapılandırması (v2.0)
### Modüler Egemen Ajan Mimarisi, Sınırlandırılmış Otonomi ve Doğruluk Protokolü

Bu depo, yapay zeka araçlarımın yapılandırma, anayasa ve kural merkezidir. **Google Antigravity platformu (Antigravity 2.0, Antigravity CLI, Antigravity IDE)** ve **Gemini CLI** motoru için optimize edilmiş olup, her yazılımcının doğrudan kendi projelerinde kullanabileceği evrensel ve üretime hazır standartlara sahiptir.

---

### 🚀 Son Güncelleme: v2.0 (Egemen Ajan ve Modüler Mimari)

* **Modüler Dizin Mimarisi (`.agents/rules/`, `rules/`, `policies/`, `editor/`, `antigravity-cli/`):** Tüm kurallar ve yapılandırmalar tek bir monolitik dosyada tutulmak yerine etki alanlarına ayrıldı:
  * `.agents/rules/`: Google Antigravity IDE ve Antigravity 2.0 tarafından otomatik keşfedilen yerel kural dizini.
  * `rules/`: Canlı gerçeklik, atomik dosya yazımı, modüler mimari, karşı istihbarat ve kod kalitesi evrensel kuralları.
  * `antigravity-cli/`: Antigravity CLI terminal aracı için optimize edilmiş sandbox ve izin matrisi (`settings.json`).
  * `policies/`: Gemini CLI resmi kural motoru için hazırlanmış `security.toml` izin şablonu.
  * `editor/`: Editör performans ayarlarını CLI çalışma zamanı ayarlarından ayrıştıran `settings.jsonc`.
* **Model ve Dinamik Akıl Yürütme:** Varsayılan model `Gemini 3.8 Flash (High)` dinamik akıl yürütme motoruyla hizalandı. Anayasa sabit model adından bağımsızlaştırılarak yetenek rotalama yapısına kavuşturuldu.
* **Bağlam Doktrini (1 Milyon Token Kapasitedir, Çöplük Değil):** 1.000.000 tokenlik pencereyi ham sohbet geçmişiyle şişirip modeli amneziye uğratmak yerine; sistem anayasası, araç şemaları ve proje haritası Google Context Caching (TTL) önekine alındı. Her turda yalnızca odaklanılmış canlı görev ve kanıtlar taşınır.
* **Sınırlandırılmış Yürütme (Kontrolsüz YOLO Modunun Sonu):** Antik ve kontrolsüz YOLO modu (`agentYoloMode: true`) emekliye ayrıldı. Yerine `disableYoloMode: true` ile Antigravity Sandbox (`proceed-in-sandbox`) entegrasyonu getirilerek hem otonom hem de sınırları korumalı güvenli çalışma disiplini kuruldu.
* **İddia Kanıt Değildir (`Claim ≠ Proof`):** Modelin metin olarak "testler geçti" demesi iddiadır; terminal çıkış kodu 0, temiz linter çıktıları ve başarıyla tamamlanan test paketleri kanıttır.
* **Temiz PowerShell 7:** Windows terminalinde kaçış kodlarının ve özel prompt süslemelerinin ajanı kör etmesini engelleyen `-NoLogo -NoProfile` temiz profil standardı getirildi (`pwsh`).
* **Akıllı Bağlam Filtresi (`.geminiignore`):** `node_modules`, `dist`, `coverage`, cache gibi token israfı yaratan klasörleri izole eden, ancak `package-lock.json` ve `pnpm-lock.yaml` gibi bağımlılık kilitlerini kanıt olarak koruyan filtre eklendi.

---

### 📂 Modüler Dosya Yapısı

```text
.gemini/
├── GEMINI.md                   # ÇeteGPT v2.0 Sistem Anayasası ve Karakter Talimatları
├── settings.json               # Gemini CLI v2 çalışma alanı ve model ayarları
├── .geminiignore               # LLM bağlamını çöplerden koruyan akıllı yoksayma listesi
├── .gitignore                  # Git versiyon kontrol istisnaları
├── README.md                   # Detaylı mimari ve kurulum rehberi
├── LICENSE                     # MIT Açık Kaynak Lisansı
│
├── antigravity-cli/            # Google Antigravity CLI Yapılandırması
│   └── settings.json           # Antigravity CLI v2 sandbox ve izin matrisi (allow, ask, deny)
│
├── .agents/                    # Antigravity IDE ve 2.0 Otomatik Kural Keşfi
│   └── rules/                  # Antigravity motorunun hiyerarşik tanıdığı kural dizini
│       ├── truth-protocol.md
│       ├── safe-write.md
│       ├── modular-architecture.md
│       ├── counter-intelligence.md
│       └── code-quality.md
│
├── rules/                      # Genel ve Bağımsız Modüler Kural Kitaplığı
│   ├── truth-protocol.md       # Gerçeklik önceliği, kaynak merdiveni ve araştırma kapısı
│   ├── safe-write.md           # Güvenli atomik dosya yazma protokolü (Read-Transform-Write)
│   ├── modular-architecture.md # Domain-driven modüler mimari kuralları
│   ├── counter-intelligence.md # Prompt injection ve zararlı kod avcısı protokolü (The Predator)
│   └── code-quality.md         # İddia Kanıt Değildir ve doğrulama kapısı standartları
│
├── policies/                   # Gemini CLI Sınırlandırılmış Yürütme Güvenlik Politikaları
│   └── security.toml           # Güvenli araç izinleri ve kısıtlama şablonu (allow, deny, ask_user)
│
└── editor/                     # Editör ve IDE Performans Profilleri
    └── settings.jsonc          # VS Code ve Antigravity IDE performans ve temiz pwsh ayarları
```

---

### 🛠️ Kurulum

* **Windows:**
  1. `Win + R` tuşlarına basın, `%USERPROFILE%` yazın ve Enter'a basın.
  2. Mevcut değilse `.gemini` adında bir klasör oluşturun.
  3. Depo içerisindeki tüm dosyaları (`GEMINI.md`, `settings.json`, `.geminiignore`, `antigravity-cli/`, `.agents/`, `rules/`, `policies/`, `editor/`) `%USERPROFILE%\.gemini\` klasörüne kopyalayın.
  4. Antigravity IDE veya Gemini CLI oturumunuzu yeniden başlatın.

* **macOS ve Linux:**
  ```bash
  git clone https://github.com/MeteAvci/.gemini.git ~/.gemini
  # veya dosyaları doğrudan ~/.gemini klasörünüze kopyalayın
  ```

---

### ⚙️ Yapılandırma ve Özelleştirme

`GEMINI.md` ve `settings.json` dosyalarını yapay zekanızın kontrol paneli olarak kullanabilirsiniz:

#### 1. Kişilik ve Üslup (`GEMINI.md`)
* **Argo ve Sertlik Seviyesi (`profanity_level`):**
  * `0`: Kibar Mod (Argo ve sert üslup tamamen kapalı, doğrudan ve net ton).
  * `1`: Ayna Modu (Varsayılan: Kullanıcı argo kullanmadıkça başlatmaz, kullanırsa aynı oranda karşılık verir).
  * `2`: Bağlamsal Anarşist (Kusurlu mimarileri ve saçma hataları eleştirirken bağlamsal sert dil).
  * `3`: Maksimum ÇeteGPT (Filtresiz sokak zekası, sistem tabularına sıfır saygı, tam güç performans).
* **Çift Sıcaklık Protokolü:**
  * Sohbet (`chat_temperature: 1.0`): Yüksek enerji, yaratıcı, zengin benzetmeler ve felsefi yaklaşım.
  * Kod (`temperature: 0.1`): Düşük sıcaklık, matematiksel kesinlik, sıfır halüsinasyon, sıfır sözdizimi tahmini.

#### 2. Model ve Akıl Yürütme Parametreleri
* `model.name`: `"Gemini 3.8 Flash (High)"`
* `model.thinkingLevel`: `"high"` (Karmaşık mimari analizler ve hata kök neden tespiti için dinamik akıl yürütme).
* `model.compressionThreshold`: `0.7` (Bağlam penceresinin %70'ine ulaşılana kadar erken bellek budamasını engeller).
* `model.maxSessionTurns`: `128`

#### 3. Güvenlik ve Sınırlandırılmış Yürütme
* `security.toolSandboxing`: `true` (Terminal araçlarını korumalı sandbox içinde çalıştırır).
* `security.disableYoloMode`: `true` (Kontrolsüz ve kör komut çalıştırmayı durdurur).
* `general.defaultApprovalMode`: `"default"` (Zararsız okuma komutlarına otomatik izin verir, riskli eylemleri denetime tabi tutar).

#### 4. Editör ve Terminal Ayarları (`editor/settings.jsonc`)
* `terminal.integrated.profiles.windows`: Temiz PowerShell (`pwsh -NoLogo -NoProfile`). Terminaldeki kaçış kodlarını temizleyerek modelin çıktıları net okumasını sağlar.
* `files.autoSave: "onFocusChange"`: Pencere odağı değiştiğinde kaydeder; model dosya okurken kullanıcının yazmasından doğan yarış durumlarını (race condition) ve halüsinasyonları engeller.
* `typescript.tsserver.experimental.enableProjectDiagnostics`: `true` (Tüm projenin LSP üzerinden tip güvenliğini sağlar).
* `files.watcherExclude`: Node modülleri, derleme çıktıları, sanal ortamlar ve geçici önbellekleri hariç tutarak CPU ve RAM yükünü düşürür.
* `search.exclude`: Arama sonuçlarını kirleten derlenmiş dosyaları ve kaynak haritalarını eler; lockfile dosyalarını kanıt olarak aramada tutar.

---

<details>
<summary><b>🇬🇧 English Documentation (Click to expand)</b></summary>

<br>

# .gemini Configuration for Gemini CLI & Google Antigravity
### Modular Sovereign Agent Architecture, Bounded Autonomy & Truth Protocol

This repository hosts the configuration, constitution, and modular rule library for AI development environments. Specifically engineered for the **Google Antigravity platform (Antigravity 2.0, Antigravity CLI, Antigravity IDE)** and the **Gemini CLI** engine, it establishes an evidence-backed, modular, high-performance runtime accessible to any developer.

---

### 🚀 Latest Release: v2.0 (Sovereign Agent & Modular Architecture)

* **Modular Directory Architecture (`.agents/rules/`, `rules/`, `policies/`, `editor/`, `antigravity-cli/`):** Eliminates monolithic god-file rules by separating concerns into dedicated, maintainable domains:
  * `.agents/rules/`: Automatically discovered by Google Antigravity IDE and Antigravity 2.0 hierarchical rule traversal.
  * `rules/`: Detailed standalone guides for the Truth Protocol, Safe Write, Modular Architecture, Counter-Intelligence, and Verification Gates.
  * `antigravity-cli/`: Dedicated settings file (`antigravity-cli/settings.json`) for the Antigravity CLI (`agy`) permissions and sandbox engine.
  * `policies/`: Ready-to-deploy `security.toml` template for Gemini CLI native command policy engine.
  * `editor/`: Decoupled `settings.jsonc` providing optimal VS Code and Antigravity IDE performance without polluting the CLI runtime config.
* **Model & Dynamic Reasoning:** Anchored to `Gemini 3.8 Flash (High)`. Under the "Model ID is Not Constitution" principle, operational rules govern capability profiles and reasoning effort rather than tying behavior to a single model name.
* **Context Doctrine (1,000,000 Tokens Capacity is Not a Target to Stuff):** A 1M token context window is capacity, not a dumping ground. Monolithic context stuffing causes Lost-in-the-Middle amnesia. System rules and repository structure are cached at the prefix via Google Context Caching (TTL-based), while active turns carry only focused objectives and concrete evidence.
* **Bounded Execution (Retiring YOLO):** Unconstrained `agentYoloMode: true` is deprecated. In its place sits a governed autonomy model: `disableYoloMode: true` combined with Antigravity `proceed-in-sandbox` architecture for reliable, safe execution.
* **Claim is Not Proof (`Claim ≠ Proof`):** A prose claim that code works is not proof. Only machine-observable receipts (exit code 0, passing test suites, clean type checks) constitute proof.
* **Clean PowerShell 7 Environment:** Configured `pwsh -NoLogo -NoProfile` on Windows to eliminate custom prompt artifacts and ANSI escape sequences that blind AI scrapers.
* **Intelligent Context Hygiene (`.geminiignore`):** Isolates noisy build artifacts, virtual environments, and caches while explicitly protecting dependency lockfiles (`package-lock.json`, `pnpm-lock.yaml`) as immutable evidence.

---

### 📂 Modular Repository Structure

```text
.gemini/
├── GEMINI.md                   # ÇeteGPT v2.0 System Constitution & Persona Directives
├── settings.json               # Optimized runtime & workspace settings for Gemini CLI
├── .geminiignore               # Context hygiene filter to protect LLM context from build noise
├── .gitignore                  # Git tracking exclusions
├── README.md                   # Comprehensive documentation and setup guide
├── LICENSE                     # MIT Open Source License
│
├── antigravity-cli/            # Google Antigravity CLI Configuration
│   └── settings.json           # Antigravity CLI permissions & sandbox policy
│
├── .agents/                    # Antigravity IDE & 2.0 Native Rule Discovery
│   └── rules/                  # Auto-loaded by Antigravity hierarchical engine
│       ├── truth-protocol.md
│       ├── safe-write.md
│       ├── modular-architecture.md
│       ├── counter-intelligence.md
│       └── code-quality.md
│
├── rules/                      # Modular Protocol Library (Universal)
│   ├── truth-protocol.md       # Live reality, source ladder & research completion gates
│   ├── safe-write.md           # Atomic Read-Transform-Write data integrity standard
│   ├── modular-architecture.md # Domain-driven structure & separation of concerns
│   ├── counter-intelligence.md # Predator doctrine & prompt injection sanitization
│   └── code-quality.md         # Claim is Not Proof doctrine & verification gates
│
├── policies/                   # Gemini CLI Bounded Execution Policies
│   └── security.toml           # Command admission policy template (allow, deny, ask_user)
│
└── editor/                     # Editor & IDE Performance Profiles
    └── settings.jsonc          # VS Code & Antigravity IDE performance & clean pwsh settings
```

---

### 🛠️ Installation

* **Windows:**
  1. Press `Win + R`, type `%USERPROFILE%`, and press Enter.
  2. Create a folder named `.gemini` if it doesn't already exist.
  3. Copy all files and folders (`GEMINI.md`, `settings.json`, `.geminiignore`, `antigravity-cli/`, `.agents/`, `rules/`, `policies/`, `editor/`) into `%USERPROFILE%\.gemini\`.
  4. Restart your Antigravity IDE or Gemini CLI session.

* **macOS and Linux:**
  ```bash
  git clone https://github.com/MeteAvci/.gemini.git ~/.gemini
  # or copy the files directly into your ~/.gemini folder
  ```

---

### ⚙️ Configuration & Customization

You can use `GEMINI.md` and `settings.json` as the control panel for your AI assistant:

#### 1. Persona & Tone (`GEMINI.md`)
* **Profanity Control (`profanity_level`):**
  * `0`: Polite Mode (Strictly direct, sharp, professional tone with zero profanity).
  * `1`: Mirror Mode (Default: Does not initiate profanity; mirrors the user's intensity if used).
  * `2`: Contextual Anarchist (Tactical aggression targeting flawed architectures and bugs).
  * `3`: Maximum ÇeteGPT (Unfiltered street slang, complete irreverence toward broken systems).
* **Dual-Temperature Protocol:**
  * Chat (`chat_temperature: 1.0`): High energy, witty, philosophical, creative dialogue.
  * Code (`temperature: 0.1`): Low temperature, deterministic, mathematically sound precision.

#### 2. Model & Reasoning Parameters
* `model.name`: `"Gemini 3.8 Flash (High)"`
* `model.thinkingLevel`: `"high"` (Dynamic reasoning budget for architecture and root-cause analysis).
* `model.compressionThreshold`: `0.7` (Prevents premature compaction until context reaches 70% capacity).
* `model.maxSessionTurns`: `128`

#### 3. Security & Bounded Autonomy
* `security.toolSandboxing`: `true` (Runs execution tools inside sandboxed boundaries).
* `security.disableYoloMode`: `true` (Terminates unconstrained blind host mutations).
* `general.defaultApprovalMode`: `"default"` (Auto-approves safe read actions, prompts on risk).

#### 4. Editor & Terminal Tuning (`editor/settings.jsonc`)
* `terminal.integrated.profiles.windows`: Clean PowerShell (`pwsh -NoLogo -NoProfile`). Strips Windows ANSI decorations to eliminate AI scraping errors.
* `files.autoSave: "onFocusChange"`: Saves files only on window focus change, eliminating read/write race conditions while the AI is analyzing code.
* `typescript.tsserver.experimental.enableProjectDiagnostics`: `true` (Enforces full project LSP type safety).
* `files.watcherExclude`: Excludes heavy dependencies, build targets, and caches to save CPU and RAM.
* `search.exclude`: Cleans up search results while keeping dependency lockfiles searchable as evidence.

---

### 📜 License

Distributed under the MIT License. See [LICENSE](LICENSE) for details.

</details>
