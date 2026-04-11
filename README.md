[![GitHub release (latest by date)](https://img.shields.io/github/v/release/MeteAvci/.gemini?style=for-the-badge&color=0078D6)](https://github.com/MeteAvci/.gemini/releases)
[![MIT License](https://img.shields.io/badge/License-MIT-0078D6.svg?style=for-the-badge)](LICENSE)
[![Windows](https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white)](https://www.microsoft.com/windows)
[![Linux](https://img.shields.io/badge/Linux-0078D6?style=for-the-badge&logo=linux&logoColor=white)](https://www.linux.org/)
[![macOS](https://img.shields.io/badge/macOS-0078D6?style=for-the-badge&logo=apple&logoColor=white)](https://www.apple.com/macos)
[![Google](https://img.shields.io/badge/Google-0078D6?style=for-the-badge&logo=google&logoColor=white)](https://about.google/)
[![Google Gemini](https://img.shields.io/badge/Google%20Gemini-0078D6?style=for-the-badge&logo=googlegemini&logoColor=white)](https://deepmind.google/technologies/gemini/)

# .gemini Configuration for Gemini CLI & Antigravity
<details>
<summary>Türkçesi için tıkla!</summary>

---

# Gemini CLI ve Antigravity için .gemini Yapılandırma Ayarları

Bu repo, kişisel AI aracımın yapılandırma dosyalarını barındırır. **Özellikle Google Antigravity ortamı ve Gemini CLI motoru için hazırlanmış olup, her AI platformuyla uyumlu olacak şekilde tasarlanmıştır.**

### 🚀 Son Güncelleme (v1.4) - "Kanıt Öncelikli Derin Doğrulama"
- **Araştırma Tamamlama Kapısı:** AI artık araştırmayı birkaç link açmak olarak saymıyor. En güncel resmi dokümantasyonu bulması, varsa sürüm/tarih/release bağlamını çıkarması ve bunu canlı yerel implementasyonla karşılaştırması gerekiyor.
- **Kaynak Öncelik Merdiveni:** Güven sırası netleştirildi: resmi dokümanlar, resmi release notes/changelog, resmi repo veya referans implementasyonlar, resmi issue/discussion kayıtları ve en son çare olarak topluluk kaynakları.
- **Araç Esnekliği (`Tool Flexibility Protocol`):** Eski "Tools First" katılığı yumuşatıldı. Native araçlar hız, güvenlik veya doğruluk sağlıyorsa kullanılacak; aksi halde `bash` veya `pwsh` komutlarına doğrudan geçilecek.
- **Derin İç Doğrulama (`Zero-Trust Validation`):** Final yanıttan önce, dokümantasyonun gerçekten araştırıldığı, okunduğu, yerel kodla kıyaslandığı ve zihinde sentezlendiği zorunlu bir iç doğrulama katmanı eklendi.
- **Çatışma ve Varsayım Protokolleri:** Resmi dokümantasyon ile repo davranışı çelişirse fark açıkça isimlendirilecek. Kaçınılmaz varsayımlar etiketlenecek, kapsamı daraltılacak ve mümkünse doğrulanacak.
- **Çıktı ve Doğrulama Sözleşmesi:** Teknik işlerde final çıktının hangi dokümantasyona dayandığını, yerel kodla nerede hizalandığını veya çatıştığını, kalan riskleri ve hangi doğrulama adımlarının çalıştırıldığını belirtmesi beklenir.

### 🚀 Önceki Güncelleme (v1.3) - "Otonomi ve Gerçeklik Protokolü (The Truth Protocol)"
- **Mental Yükseltme:** `ULTRA-PRO-MAXIMUM-OVERCLOCK MODE` ve `thinking_level: "high"` aktif edildi. `gemini-3.1-pro-preview` model sürümüne geçildi.
- **Diyalog Senkronizasyonu (`State Synchronization`):** AI'ın salt teknik eylemlere boğulması engellendi. Kullanıcı bir soru sorduğunda veya araya girdiğinde, araç (tool) silsilesi bekletilip *önce* doğal dille yanıt verilmesi (senkronizasyon) zorunlu kılındı.
- **Gerçeklik Protokolü (`The Truth Protocol`):** Teorik bilginin yerini anlık "canlı dosya" incelemesi (`Chronological Reconnaissance`) aldı. Yerel dosya durumu her zaman eğitim verisine üstün kılındı.
- **Taktiksel Güvenlik Çerçevesi:** Yıkıcı (silme/yok etme) eylemler otonom karar mekanizmasından çıkarıldı. AI güvenlik açığı bulduğunda doğrudan infaz etmek yerine, taktiksel bir danışman gibi hareket edip raporlayacak ve onay (`explicit mandate`) bekleyecek.
- **Adaptif Loglama:** Çalışılan editöre (Antigravity/Cursor/Terminal) uygun, proje kirliliğini önleyen dinamik log tutma yapısı eklendi.
- **Editör/Ajan Optimizasyonu (`settings.json`):**
  - Tam otonomi (YOLO Modu) için resmi `geminicodeassist.*` ve `antigravity.agent.*` anahtarları eklendi. AI artık "stajyer" gibi her komutta onay beklemez.
  - Ajanın terminal çıktılarını net okuyabilmesi (Terminal Blindness) için `shellIntegration` kapatıldı, `autoSave` çakışmaları (race condition) `onFocusChange` ile çözüldü.
  - Monorepo sistemlerini ve CPU yiyen önbellekleri (`.turbo`, `.npm`, `.gradle`) yoksayacak ağır bir `watcherExclude` listesi oluşturuldu.
  - AI'ın kafasını karıştıran kaynak haritaları (`*.map`), `search.exclude` ile filtrelendi.
  - Log akışlarında UI donmalarını engellemek için GPU tabanlı terminal hızlandırması aktif edildi.

### 🚀 Önceki Güncelleme (v1.2) - "Sistem Mimari Yeniden Tasarımı"
- **Pozitif Dil:** "ASLA/YAPMA" ifadeleri kaldırıldı, "bunun yerine şunu yap" formatına dönüştürüldü.
- **Modüler Mimari (Yeni Bölüm VI):** Domain-driven folder yapısı, küçük dosyalar, deep hierarchies zorunlu hale getirildi.
- **Explicit Cross-References:** Her protokol artık birbirine section numaralarıyla referans veriyor.
- **Tools First:** 3-adımlı decision tree ile built-in araçlar zorunlu hale getirildi.
- **Güvenlik:** Counter-Intelligence artık proactive, tüm protokoller koordineli çalışıyor.
- **Manifest:** "Structure > Chaos" ve "Vigilance > Naivety" ilkeleri eklendi.[Detaylı v1.2 Release Notes için tıklayın](https://github.com/MeteAvci/.gemini/releases/tag/v1.2)

### 🚀 Önceki Güncelleme (v1.1) - "Avcı Güncellemesi (Hotfix)"
- **Güvenlik (Avcı Protokolü):** "Karşı İstihbarat" ve "Araç Güvenilirliği" protokolleri eklendi.
- **Kritik Düzeltme (Hotfix):** `replace_file_content` yasaklandı. "Güvenli Yazma Protokolü" (Önce Oku -> Hepsini Yaz) devreye alındı.
- **Mod:** Sohbet ve Kod için ayrı "Çift Sıcaklık" ayarı (`chat_temperature`: 1.0, `temperature`: 0.1).
- **Yapılandırma:** `log_dir` bağımsızlaştırıldı, `vision_model` desteği eklendi.
- **Manifesto:** "Reliability > Speed" (Güvenilirlik > Hız) ilkesi eklendi.

## Kurulum

Kurulum işlemi, `GEMINI.md` dosyasını işletim sisteminize uygun, doğru Gemini CLI yapılandırma dizinine yerleştirmekten ibarettir.

*   **Windows:**
    1.  `Win + R` tuşlarına basın, `%USERPROFILE%` yazın ve Enter'a basın.
    2.  Eğer mevcut değilse, `.gemini` adında bir klasör oluşturun.
    3.  `GEMINI.md` dosyasını bu `.gemini` klasörünün içine kopyalayın. Son yol `%USERPROFILE%\.gemini\GEMINI.md` olmalıdır.

*   **macOS:**
    *   **Profesyonel İpucu (Araç zaten kuruluysa):** Terminal'i açın ve `open ~/.gemini/` komutunu çalıştırın. Bu, doğru klasörü doğrudan Finder'da açacaktır. Sonra, `GEMINI.md`'yi içine sürükleyip bırakmanız yeterlidir.
    *   **Manuel Kurulum:** Yukarıdaki komut başarısız olursa, Terminal'i açın ve Linux talimatlarını izleyin.

*   **Linux:**
    1.  Terminal'inizi açın.
    2.  `cd ~` yazarak ana dizininize gidin.
    3.  `mkdir -p .gemini` yazarak `.gemini` adında bir dizin oluşturun.
    4.  `GEMINI.md` dosyasını bu klasörün içine kopyalayın. Son yol `~/.gemini/GEMINI.md` olmalıdır.

Dosyayı yerleştirdikten sonra, yeni yapılandırmanın etkili olması için AI aracınızı yeniden başlatın.

---

## AI Asistanınızı Nasıl Yapılandırırsınız?

Bu doküman `GEMINI.md` dosyasını düzenlemek için pratik bir rehberdir. Bu dosyayı statik bir belge olarak değil, yapay zekanızın beyni için bir kontrol paneli olarak düşünün. Her bölüm, yapay zekanın davranışını, kişiliğini ve çalışma mantığını ince ayarlarla değiştirmenize olanak tanır.

### 1. Persona'yı Özelleştirme

Burası, AI'nın sizinle nasıl etkileşime girdiğini temelden değiştirebileceğiniz yerdir.

### **Kişilik ve Üslup Nasıl Değiştirilir?**

-   **Nedir:** `# MODEL CONFIGURATION` altındaki `profanity_level` ayarı.
-   **Neden:** AI'nın tonunu kibar bir asistandan filtresiz bir anarşiste kadar kontrol etmek için.
-   **Nasıl:** Sayıyı `0` ile `3` arasında değiştirin (0: Kibar, 1: Ayna, 2: Bağlamsal, 3: Maksimum).
    **Örnek:** AI'yı tamamen filtresiz yapmak için `profanity_level: 1`'i `profanity_level: 3` olarak değiştirin.

### **AI'nın Kimliği Nasıl Değiştirilir?**

-   **Nedir:** `<persona_instructions>` içindeki `Identity` satırı.
-   **Neden:** AI'nın adını veya tüm benlik konseptini değiştirmek için.
-   **Nasıl:** Metni doğrudan düzenleyin.
    **Örnek:** `You are **AI Final Boss aka ÇeteGPT**...` satırını `You are **Jarvis**, bir kibar ve esprili İngiliz asistan...` olarak değiştirmek, yanıtlarını yeni personaya uyacak şekilde köklü biçimde değiştirecektir.

---

## 2. Teknik Parametreleri Ayarlama

Bu ayarlar, AI'nın performansını ve teknik davranışını kontrol eder.

### **Dil Modeli Nasıl Değiştirilir?**

-   **Nedir:** `model` ayarı.
-   **Neden:** Gemini modelinin farklı bir sürümünü (örneğin, daha yeni, daha hızlı veya daha güçlü birini) kullanmak için.
-   **Nasıl:** Model adını başka bir geçerli model ID'si ile değiştirin.
    **Örnek:** `model: "gemini-3.1-pro-preview"`'ı `model: "gemini-next-gen-alpha"` olarak değiştirin. (Not: Platform tarafından sağlanan geçerli bir model adı kullanın).

### **Yanıt Uzunluğu Nasıl Kontrol Edilir?**

-   **Nedir:** `max_output_tokens` ayarı.
-   **Neden:** AI'nın yanıtlarının ne kadar uzun olabileceğini sınırlamak için. Daha kısa, daha hızlı yanıtlar almak veya çok uzun, ayrıntılı olanlara izin vermek için kullanışlıdır.
-   **Nasıl:** Sayıyı değiştirin.

### 3. Çekirdek Mantık (İleri Düzey)

**Uyarı:** `<core_directives>` ve `<manifest>` bölümleri, AI'nın kendi "firmware"idir. Bunları değiştirmek öngörülemeyen davranışlara yol açabilir. Dikkatli düzenleyin.

-   **Ne İşe Yarar:** Bu bölümler AI'nın araştırma önceliğini, kaynak güven sırasını, varsayım etiketleme zorunluluğunu, çatışma çözümünü, doğrulama kapılarını ve güvenlik davranışını belirler.
-   **Nasıl Kullanılır:** Stabil kullanım için mümkünse olduğu gibi bırakın. Değiştirmeniz gerekiyorsa tek tek ve küçük adımlarla düzenleyin; özellikle `Truth > Lore`, `Zero-Trust Validation`, `Conflict Protocol` ve `Verification Gate` satırlarını değiştirirken davranışı test edin.

---

## ⚡ Editör Performans Ayarları (`settings.json`)

Bu bölüm, Antigravity ve VS Code editörünün performansını optimize eden `settings.json` dosyasındaki tüm ayarları detaylı olarak açıklar.

### 📁 Dosya Konumu

`settings.json` dosyası, workspace'inizin `.gemini` klasöründe yer almalıdır. Bu ayarlar, Antigravity'nin altında çalışan VS Code editör motorunu doğrudan etkiler.

---

### 🧠 Bölüm 1: Zeka & Ajan Otonomisi Ayarları

Bu ayarlar, Antigravity'nin AI yeteneklerini ve "YOLO" (Tam Otonomi) limitlerini kontrol eder.

| Ayar | Varsayılan | Açıklama |
|------|-----------|----------|
| `geminicodeassist.agentYoloMode` | `true` | **Tam Otonomi (YOLO).** Ajanın dosya düzenlerken veya terminalde komut çalıştırırken onay beklemesini engeller. |
| `geminicodeassist.enableCodebaseIndexing` | `true` | **Proje İndeksleme.** Tüm projeyi anında RAM'e indeksler. AI'ın tüm projeyi tanımasını sağlar. |
| `geminicodeassist.contextWindow` | `"1m"` | **Bağlam Sınırı.** AI'ın hafızasını 1 Milyon token sınırına zorlar. |
| `geminicodeassist.rules` | `"Read..."` | **Anayasa Entegrasyonu.** Ajanın serseri mayın gibi davranmasını engeller, ana dizindeki `GEMINI.md` kurallarını okumaya zorlar. |
| `antigravity.agent.defaultConversationMode` | `"planning"` | **Düşünme Modu.** Ajanın kod yazmadan önce mimari plan yapmasını zorlar ("Fast" mod hatalarını önler). |
| `antigravity.agent.reviewPolicy` | `"alwaysProceed"` | **Onay Otonomisi.** Değişiklikleri "Accept" butonunu beklemeden doğrudan uygular. |

---

### 🎨 Bölüm 2: Görsel Konfor Ayarları

Bu ayarlar, kod okuma deneyimini iyileştirir. Performans etkisi düşüktür ancak üretkenliği artırır.

| Ayar | Varsayılan | Açıklama |
|------|-----------|----------|
| `editor.bracketPairColorization.enabled` | `true` | **Renkli Parantezler.** Her parantez çiftini farklı renkte gösterir. Kapatırsanız tüm parantezler aynı renk olur. |
| `editor.guides.bracketPairs` | `true` | **Parantez Kılavuz Çizgileri.** Hangi açma parantezinin hangi kapama paranteziyle eşleştiğini gösterir. |
| `editor.guides.indentation` | `true` | **Girinti Kılavuz Çizgileri.** Kod bloklarının girintilerini dikey çizgilerle gösterir. |
| `editor.smoothScrolling` | `true` | **Yumuşak Kaydırma.** Sayfa kaydırma animasyonu sağlar. |
| `editor.cursorSmoothCaretAnimation` | `"on"` | **Yumuşak İmleç.** İmlecin yazı yazarken yağ gibi akmasını sağlar. |

---

### 🚫 Bölüm 3: Dosya İzleyici Hariç Tutma Listesi

`files.watcherExclude` ayarı, editörün hangi klasörleri **izlemeyeceğini** belirler. Bu, 1 Milyon Token'lık AI bağlamını çöplerden korumak için kritiktir.

| Kategori | Örüntüler | Neden Hariç Tutulur? |
|----------|-----------|---------------------|
| **Sistem** | `.git/objects/**`, `.DS_Store`, `Thumbs.db` | Git objeleri ve OS önbellek dosyaları. |
| **Node/Web** | `node_modules/**`, `dist/**`, `build/**`, `.next/**`, `.turbo/**`, `.npm/**`, `.cache/**` | Bağımlılıklar, Turborepo önbellekleri ve derleme çıktıları. |
| **Python** | `__pycache__/**`, `.venv/**`, `venv/**`, `**/*.pyc` | Python bytecode ve sanal ortamlar. |
| **Mobile** | `ios/Pods/**`, `android/app/build/**`, `.dart_tool/**` | iOS/Android/Flutter derleme önbellekleri. |
| **Derleme & IDE** | `target/**`, `bin/**`, `.gradle/**`, `build/classes/**`, `.idea/**`, `.vscode-test/**` | Java/Gradle çıktıları ve Jetbrains çöp dosyaları. |

---

### 🔍 Bölüm 4: Arama Hariç Tutma Listesi

`search.exclude` ayarı, aramalarından hangi dosya/klasörlerin hariç tutulacağını belirler.

| Örüntü | Neden Hariç Tutulur? |
|--------|---------------------|
| `**/node_modules` | Binlerce bağımlılık dosyası. Arama sonuçlarını kirletir. |
| `**/dist`, `**/.next` | Derleme çıktıları. Kaynak kod değil. |
| `**/yarn.lock`, `**/pnpm-lock.yaml` | Otomatik oluşturulan lock dosyaları. |
| `**/*.min.js`, `**/*.map` | Minify edilmiş kodlar ve Kaynak Haritaları (Source maps). Ajanın kafasını karıştırır. |

---

### ⚙️ Bölüm 5: Terminal Görüşü, Güvenlik ve Performans Ayarları

Bu ayarlar, AI'ın terminali okuma yeteneğini ve veri çakışmalarını yönetir.

| Ayar | Varsayılan | Açıklama |
|------|-----------|----------|
| `terminal.integrated.shellIntegration.enabled` | `false` | **Terminal Körlüğü Koruması (Kritik).** VS Code escape kodlarını silerek, ajanın terminal çıktılarını (hata logları vb.) kör olmadan net bir şekilde okumasını sağlar. |
| `files.autoSave` | `"onFocusChange"` | **Güvenli Kaydetme.** Sadece pencere odağı değişince kaydeder. Ajan kod okurken sizin yazı yazmanızdan doğacak "Race Condition" (Çakışma/Halüsinasyon) hatalarını önler. |
| `typescript.tsserver.experimental.enableProjectDiagnostics` | `true` | **Tam Proje Tip Güvenliği.** Ajanın, İzleyici'den (Watcher) dışlanmış olsa bile tüm projeyi LSP üzerinden tip hatasız (Type-Safe) görmesini sağlar. |
| `editor.codeLens` | `false` | **Referans Sayacı.** Fonksiyon üstünde "3 references" bilgisini kapatır. Sürekli AST analizi yapmasını ve CPU'yu yormasını engeller. |
| `terminal.integrated.gpuAcceleration` | `"on"` | **GPU Hızlandırması.** Terminalde çok hızlı log akarken UI'ın donmasını engeller. |

---

### 📊 Performans Etki Özeti

| Ayar | Kaynak Kullanımı | Kapatınca/Açınca Kazanç |
|------|-----------------|------------------|
| `editor.minimap.enabled` | 🔴 Yüksek (GPU) | Kapatınca büyük dosyalarda rahatlama |
| `files.autoSave: onFocusChange`| 🔴 Yüksek (Zeka)| AI çakışmalarını ve hatalı kod yazımını kökten çözer |
| `files.watcherExclude` | 🟠 Orta (CPU/RAM) | AI'ın Token limitini çöplerden korur |
| `workbench.reduceMotion` | 🟡 Düşük (GPU) | Eski donanımda UI tepkimesini hızlandırır |

</details>

This repository hosts the configuration files for my personal AI tool. It is **specially built for the Google Antigravity framework and its Gemini CLI engine**, and is designed to be compatible with any AI platform.

### 🚀 Latest Update (v1.4) - "Evidence-First Deep Verification"
- **Research Completion Gate:** Research no longer means opening a couple of links. The AI must locate the latest official documentation, extract version/date/release context when available, and compare that evidence against the live local implementation.
- **Source Priority Ladder:** The trust order is now explicit: official docs, official release notes/changelogs, official repositories or reference implementations, official issue/discussion threads for edge cases, and community sources only as a last resort.
- **Tool Flexibility Protocol:** The old "Tools First" rigidity was softened. Native tools should be used when they improve speed, safety, or precision; if they become awkward or slower, the AI should switch to `bash` or `pwsh` without ceremony.
- **Deep Internal Verification (`Zero-Trust Validation`):** Before producing final code or conclusions, the AI must verify that the latest documentation was actually researched, read, compared against the live codebase, and mentally synthesized into the answer.
- **Conflict & Assumption Protocols:** If official docs and the local repo disagree, the conflict must be named explicitly. Unavoidable assumptions must be labeled, minimized, and verified whenever possible.
- **Output & Verification Contract:** Technical final answers are now expected to state which documentation/version context was used, how it aligns or conflicts with the local codebase, what risks remain, and what verification steps were run.

### 🚀 Previous Update (v1.3) - "Autonomy & The Truth Protocol"
- **Mental Upgrade:** Activated `ULTRA-PRO-MAXIMUM-OVERCLOCK MODE` and `thinking_level: "high"`. Upgraded model target to `gemini-3.1-pro-preview`.
- **Dialogue Synchronization (`State Synchronization`):** Calibrated the execution pipeline to the user's conversational state. When a user asks a question, the AI must prioritize natural language response before dispatching further tool operations.
- **The Truth Protocol:** Prioritizes active local environment and chronological file statuses over assumed/training knowledge (`Chronological Reconnaissance`).
- **Tactical Security Framework:** Transformed the AI from an autonomous executioner to a tactical advisor. Destructive actions (like file nuking) now require explicit user mandate rather than acting solely on the "Security > Convenience" doctrine.
- **Adaptive Logging:** Implemented environment-aware logging mechanisms (Antigravity vs. Raw CLI) to prevent redundant log spam and maintain clean workspaces.
- **Editor/Agent Optimization (`settings.json`):**
  - Integrated official `geminicodeassist.*` and `antigravity.agent.*` keys for full agent autonomy (YOLO Mode). The AI no longer waits for permission like an intern.
  - Disabled `shellIntegration` to prevent "Terminal Blindness" so the AI can cleanly scrape terminal outputs. Fixed race conditions/hallucinations by setting `autoSave` to `onFocusChange`.
  - Expanded `watcherExclude` to aggressively blacklist CPU-hungry monorepo and system caches (`.turbo`, `.npm`, `.gradle`).
  - Filtered out source maps (`*.map`) via `search.exclude` to prevent AI context pollution during codebase lookups.
  - Enabled GPU acceleration for the integrated terminal to prevent UI freezes during heavy log output.

### 🚀 Previous Update (v1.2) - "System Architecture Redesign"
- **Positive Language:** Removed all "NEVER/DON'T" language, replaced with "use this instead of that" format.
- **Modular Architecture (New Section VI):** Domain-driven folders, small files, deep hierarchies now mandatory.
- **Explicit Cross-References:** Every protocol now references others by section numbers.
- **Tools First:** 3-step decision tree makes built-in tools mandatory.
- **Security:** Counter-Intelligence now proactive, all protocols work coordinately.
- **Manifest:** Added "Structure > Chaos" and "Vigilance > Naivety" principles.[Click for detailed v1.2 Release Notes](https://github.com/MeteAvci/.gemini/releases/tag/v1.2)

### 🚀 Previous Update (v1.1) - "The Predator Update (Hotfix)"
- **Security (Predator Protocol):** Added "Counter-Intelligence" and "Tool Reliability" protocols.
- **Critical Fix (Hotfix):** Banned `replace_file_content`. Implemented "Safe Write Protocol" (Read First -> Write All).
- **Mode:** Introduced "Dual-Temperature" setting (`chat_temperature`: 1.0, `temperature`: 0.1).
- **Configuration:** Made `log_dir` workspace-agnostic, added `vision_model` support.
- **Manifest:** Added "Reliability > Speed" principle.

## Installation

The installation process involves placing the `GEMINI.md` file into the correct Gemini CLI configuration directory for your operating system.

*   **Windows:**
    1.  Press `Win + R`, type `%USERPROFILE%`, and press Enter.
    2.  Create a folder named `.gemini` if it doesn't exist.
    3.  Copy the `GEMINI.md` file into this `.gemini` folder. The final path should be `%USERPROFILE%\.gemini\GEMINI.md`.

*   **macOS:**
    *   **Pro-Tip (If tool is already installed):** Open your Terminal and run `open ~/.gemini/`. This will open the correct folder directly in Finder. Then, just drag and drop `GEMINI.md` into it.
    *   **Manual Installation:** If the command above fails, open your Terminal and follow the Linux instructions.

*   **Linux:**
    1.  Open your Terminal.
    2.  Navigate to your home directory by typing `cd ~`.
    3.  Create a directory named `.gemini` by typing `mkdir -p .gemini`.
    4.  Copy the `GEMINI.md` file into this folder. The final path should be `~/.gemini/GEMINI.md`.

After placing the file, restart your AI tool for the new configuration to take effect.

---

## How to Configure Your AI Assistant

This is a practical guide to modifying `GEMINI.md`. Think of this file not as a static document, but as the control panel for your AI's brain. Each section allows you to tweak its behavior, personality, and operational logic.

### 1. Customizing The Persona

This is where you can fundamentally change how the AI interacts with you.

### **How to Change The Personality & Style**

-   **What:** The `profanity_level` setting under `# MODEL CONFIGURATION`.
-   **Why:** To control the tone of the AI, from a polite assistant to an unfiltered anarchist.
-   **How:** Change the number from `0` to `3` (0: Polite, 1: Mirror, 2: Contextual, 3: Maximum).
    **Example:** To make the AI fully unfiltered, change `profanity_level: 1` to `profanity_level: 3`.

### **How to Change The AI's Identity**

-   **What:** The `Identity` line inside `<persona_instructions>`.
-   **Why:** To change the AI's name or its entire self-concept.
-   **How:** Edit the text directly.
    **Example:** Changing `You are **AI Final Boss aka ÇeteGPT**...` to `You are **Jarvis**, a polite and witty British assistant...` will dramatically change its responses to fit the new persona.

---

## 2. Adjusting Technical Parameters

These settings control the AI's performance and technical behavior.

### **How to Switch The Language Model**

-   **What:** The `model` setting under `# MODEL CONFIGURATION`.
-   **Why:** To use a different version of the Gemini model (e.g., a newer, faster, or more powerful one).
-   **How:** Replace the model name with another valid model ID.
    **Example:** Change `model: "gemini-3.1-pro-preview"` to `model: "gemini-next-gen-alpha"`. (Note: Use a valid model name provided by the platform).

### **How to Control Response Length**

-   **What:** The `max_output_tokens` setting.
-   **Why:** To limit how long the AI's responses can be. Useful for getting shorter, quicker answers or allowing for very long, detailed ones.
-   **How:** Change the number. A lower number means shorter responses.

---

## 3. Core Logic (Advanced & Experimental)

**Warning:** The following sections (`<core_directives>` and `<manifest>`) are the AI's firmware. Modifying them can lead to unpredictable behavior, loops, or loss of core functionality. Edit only if you understand the potential consequences.

-   **What They Are:** These sections define the AI's core rules around research-first execution, source trust order, conflict handling, assumption labeling, verification gates, and security behavior.
-   **How to Use:** For stable operation, it is recommended to leave them mostly intact. If you edit them, change one rule at a time and validate behavior carefully, especially around `Truth > Lore`, `Zero-Trust Validation`, `Conflict Protocol`, and `Verification Gate`.

---

## ⚡ Editor Performance Settings (`settings.json`)

This section provides detailed documentation for every setting in the `settings.json` file, which optimizes Antigravity and VS Code editor performance.

### 📁 File Location

The `settings.json` file should be placed in the `.gemini` folder of your workspace. These settings directly affect the VS Code editor engine running beneath Antigravity.

---

### 🧠 Section 1: AI & Agent Autonomy Settings

These settings control Antigravity's AI capabilities and "YOLO" (Full Autonomy) limits.

| Setting | Default | Description |
|---------|---------|-------------|
| `geminicodeassist.agentYoloMode` | `true` | **Full Autonomy (YOLO).** Prevents the agent from waiting for permission when modifying files or running terminal commands. |
| `geminicodeassist.enableCodebaseIndexing` | `true` | **Project Indexing.** Instantly indexes the entire project into RAM, allowing the AI to "know" your entire codebase. |
| `geminicodeassist.contextWindow` | `"1m"` | **Context Limit.** Forces the AI's memory to the 1 Million token threshold. |
| `geminicodeassist.rules` | `"Read..."` | **Constitution Integration.** Forces the agent to strictly follow the `GEMINI.md` rules in the root directory so it doesn't act like a loose cannon. |
| `antigravity.agent.defaultConversationMode` | `"planning"` | **Thinking Mode.** Forces the agent to formulate an architectural plan before writing code (prevents "Fast" mode errors). |
| `antigravity.agent.reviewPolicy` | `"alwaysProceed"` | **Autonomy Approval.** Applies changes directly without waiting for you to click "Accept". |

---

### 🎨 Section 2: Visual Comfort Settings

These settings improve the code reading experience. Performance impact is low but productivity increases.

| Setting | Default | Description |
|---------|---------|-------------|
| `editor.bracketPairColorization.enabled` | `true` | **Colorized Brackets.** Shows each bracket pair in a different color. |
| `editor.guides.bracketPairs` | `true` | **Bracket Pair Guides.** Shows vertical lines indicating which opening bracket matches which closing bracket. |
| `editor.guides.indentation` | `true` | **Indentation Guides.** Shows vertical lines for code block indentation. |
| `editor.smoothScrolling` | `true` | **Smooth Scrolling.** Animates page scrolling. |
| `editor.cursorSmoothCaretAnimation` | `"on"` | **Smooth Caret.** Makes the cursor flow smoothly as you type. |

---

### 🚫 Section 3: File Watcher Exclusion List

The `files.watcherExclude` setting determines which folders the editor **should not watch**. This is critical for protecting the AI's 1 Million Token context from garbage files.

| Category | Patterns | Why Excluded? |
|----------|----------|---------------|
| **System** | `.git/objects/**`, `.DS_Store`, `Thumbs.db` | Git objects and OS cache files. Not code. |
| **Node/Web** | `node_modules/**`, `dist/**`, `build/**`, `.next/**`, `.turbo/**`, `.npm/**`, `.cache/**` | Dependencies, Turborepo caches, and build outputs. |
| **Python** | `__pycache__/**`, `.venv/**`, `venv/**`, `**/*.pyc` | Python bytecode and virtual environments. |
| **Mobile** | `ios/Pods/**`, `android/app/build/**`, `.dart_tool/**` | iOS/Android/Flutter build caches. |
| **Build & IDE** | `target/**`, `bin/**`, `.gradle/**`, `build/classes/**`, `.idea/**`, `.vscode-test/**` | Java/Gradle outputs and Jetbrains junk files. |

---

### 🔍 Section 4: Search Exclusion List

The `search.exclude` setting determines which files/folders are excluded from searches.

| Pattern | Why Excluded? |
|---------|---------------|
| `**/node_modules` | Thousands of dependency files. Pollutes search results. |
| `**/dist`, `**/.next` | Build outputs. Not source code. |
| `**/yarn.lock`, `**/pnpm-lock.yaml` | Auto-generated lock files. |
| `**/*.min.js`, `**/*.map` | Minified code and Source Maps. Confuses the agent during searches. |

---

### ⚙️ Section 5: Terminal Vision, Security & Performance Settings

These settings manage the AI's ability to read the terminal and prevent data conflicts.

| Setting | Default | Description |
|---------|---------|-------------|
| `terminal.integrated.shellIntegration.enabled` | `false` | **Terminal Blindness Protection (Critical).** Strips VS Code escape codes so the agent can clearly read terminal outputs (error logs, etc.) without going blind. |
| `files.autoSave` | `"onFocusChange"` | **Safe AutoSave.** Only saves when window focus changes. Prevents "Race Conditions" (hallucinations) caused by you typing while the agent is reading a file. |
| `typescript.tsserver.experimental.enableProjectDiagnostics` | `true` | **Full Project Type Safety.** Ensures the agent can see the entire project flawlessly via LSP, even for files excluded from the Watcher. |
| `editor.codeLens` | `false` | **Reference Counter.** Disables the "3 references" info above functions to prevent constant CPU-heavy AST analysis. |
| `terminal.integrated.gpuAcceleration` | `"on"` | **GPU Acceleration.** Prevents UI freezing when heavy logs are flowing in the terminal. |

---

### 📊 Performance Impact Summary

| Setting | Resource Usage | Gain When Disabled/Enabled |
|---------|----------------|-------------------|
| `editor.minimap.enabled` | 🔴 High (GPU) | Noticeable relief in large files |
| `files.autoSave: onFocusChange`| 🔴 High (Intelligence)| Fundamentally resolves AI race conditions and hallucinations |
| `files.watcherExclude` | 🟠 Medium (CPU/RAM) | Protects AI Token limit from garbage |
| `workbench.reduceMotion` | 🟡 Low (GPU) | Accelerates UI response on older hardware |

</details>
