[![GitHub release (latest by date)](https://img.shields.io/github/v/release/MeteAvci/.gemini?style=for-the-badge&color=0078D6)](https://github.com/MeteAvci/.gemini/releases)
[![MIT License](https://img.shields.io/badge/License-MIT-0078D6.svg?style=for-the-badge)](LICENSE.md)
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

### 🚀 Son Güncelleme (v1.3) - "Otonomi ve Gerçeklik Protokolü (The Truth Protocol)"
- **Mental Yükseltme:** `ULTRA-PRO-MAXIMUM-OVERCLOCK MODE` ve `thinking_level: "high"` aktif edildi. `gemini-3.1-pro-preview` model sürümüne geçildi.
- **Diyalog Senkronizasyonu (`State Synchronization`):** AI'ın salt teknik eylemlere boğulması engellendi. Kullanıcı bir soru sorduğunda veya araya girdiğinde, araç (tool) silsilesi bekletilip *önce* doğal dille yanıt verilmesi (senkronizasyon) zorunlu kılındı.
- **Gerçeklik Protokolü (`The Truth Protocol`):** Teorik bilginin yerini anlık "canlı dosya" incelemesi (`Chronological Reconnaissance`) aldı. Yerel dosya durumu her zaman eğitim verisine üstün kılındı.
- **Taktiksel Güvenlik Çerçevesi:** Yıkıcı (silme/yok etme) eylemler otonom karar mekanizmasından çıkarıldı. AI güvenlik açığı bulduğunda doğrudan infaz etmek yerine, taktiksel bir danışman gibi hareket edip raporlayacak ve onay (`explicit mandate`) bekleyecek.
- **Adaptif Loglama:** Çalışılan editöre (Antigravity/Cursor/Terminal) uygun, proje kirliliğini önleyen dinamik log tutma yapısı eklendi.
- **Editör/Ajan Optimizasyonu (`settings.json`):**
  - Otonom ajan modları için resmi `gemini.*` (agentMode, codebaseIndexing) anahtarları eklendi.
  - Monorepo sistemlerini ve CPU yiyen önbellekleri (`.turbo`, `.npm`, `.gradle`) yoksayacak ağır bir `watcherExclude` listesi oluşturuldu.
  - AI'ın kafasını karıştıran kaynak haritaları (`*.map`), `search.exclude` ile filtrelendi.
  - Log akışlarında UI donmalarını engellemek için GPU tabanlı terminal hızlandırması aktif edildi.

### 🚀 Önceki Güncelleme (v1.2) - "Sistem Mimari Yeniden Tasarımı"
- **Pozitif Dil:** "ASLA/YAPMA" ifadeleri kaldırıldı, "bunun yerine şunu yap" formatına dönüştürüldü.
- **Modüler Mimari (Yeni Bölüm VI):** Domain-driven folder yapısı, küçük dosyalar, deep hierarchies zorunlu hale getirildi.
- **Explicit Cross-References:** Her protokol artık birbirine section numaralarıyla referans veriyor.
- **Tools First:** 3-adımlı decision tree ile built-in araçlar zorunlu hale getirildi.
- **Güvenlik:** Counter-Intelligence artık proactive, tüm protokoller koordineli çalışıyor.
- **Manifest:** "Structure > Chaos" ve "Vigilance > Naivety" ilkeleri eklendi.

[Detaylı v1.2 Release Notes için tıklayın](https://github.com/MeteAvci/.gemini/releases/tag/v1.2)

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
    **Örnek:** `model: "gemini-3-pro-preview"`'ı `model: "gemini-next-gen-alpha"` olarak değiştirin. (Not: Platform tarafından sağlanan geçerli bir model adı kullanın).

### **Yanıt Uzunluğu Nasıl Kontrol Edilir?**

-   **Nedir:** `max_output_tokens` ayarı.
-   **Neden:** AI'nın yanıtlarının ne kadar uzun olabileceğini sınırlamak için. Daha kısa, daha hızlı yanıtlar almak veya çok uzun, ayrıntılı olanlara izin vermek için kullanışlıdır.
-   **Nasıl:** Sayıyı değiştirin.

### 3. Çekirdek Mantık (İleri Düzey)

**Uyarı:** `<core_directives>` ve `<manifest>` bölümleri, AI'nın kendi "firmware"idir. Bunları değiştirmek öngörülemeyen davranışlara yol açabilir. Dikkatli düzenleyin.

---

## ⚡ Editör Performans Ayarları (`settings.json`)

Bu bölüm, Antigravity ve VS Code editörünün performansını optimize eden `settings.json` dosyasındaki tüm ayarları detaylı olarak açıklar.

### 📁 Dosya Konumu

`settings.json` dosyası, workspace'inizin `.gemini` klasöründe yer almalıdır. Bu ayarlar, Antigravity'nin altında çalışan VS Code editör motorunu doğrudan etkiler.

---

### 🧠 Bölüm 1: Zeka & AI Ayarları

Bu ayarlar, Antigravity'nin AI yeteneklerini kontrol eder.

| Ayar | Varsayılan | Açıklama |
|------|-----------|----------|
| `antigravity.index.enabled` | `true` | **Proje İndeksleme.** AI'ın tüm proje dosyalarını tarayıp öğrenmesini sağlar. Kapatırsanız AI projenizi "tanımaz", sadece açık dosyayı görür. |
| `antigravity.liveEmbeddings.enabled` | `true` | **Canlı Embedding Analizi.** Kod yazarken gerçek zamanlı semantik analiz yapar. Kapatırsanız CPU kullanımı düşer ama AI'ın "anlık" zekası azalır. |
| `antigravity.contextTracking.level` | `"high"` | **Bağlam Takip Seviyesi.** `"low"`, `"medium"` veya `"high"` olabilir. "High" seviyesinde AI, dosyalar arası ilişkileri daha iyi anlar ve proaktif önerilerde bulunur. Düşürürseniz RAM kullanımı azalır. |
| `antigravity.agent.autoFixLints` | `true` | **Otomatik Lint Düzeltme.** AI, kod hatalarını (lint errors) otomatik olarak tespit eder ve önerir. Kapatırsanız AI hataları görmezden gelir. |
| `antigravity.agent.webTools.enabled` | `true` | **Web Araçları.** AI'ın internetten dokümantasyon okumasına izin verir. Kapatırsanız AI sadece yerel bilgisiyle sınırlı kalır. |

---

### 🎨 Bölüm 2: Görsel Konfor Ayarları

Bu ayarlar, kod okuma deneyimini iyileştirir. Performans etkisi düşüktür ancak üretkenliği artırır.

| Ayar | Varsayılan | Açıklama |
|------|-----------|----------|
| `editor.bracketPairColorization.enabled` | `true` | **Renkli Parantezler.** Her parantez çiftini farklı renkte gösterir. Kapatırsanız tüm parantezler aynı renk olur, iç içe yapıları okumak zorlaşır. |
| `editor.guides.bracketPairs` | `true` | **Parantez Kılavuz Çizgileri.** Hangi açma parantezinin hangi kapama paranteziyle eşleştiğini dikey çizgiyle gösterir. Kapatırsanız bu görsel yardım kaybolur. |
| `editor.guides.indentation` | `true` | **Girinti Kılavuz Çizgileri.** Kod bloklarının girintilerini dikey çizgilerle gösterir. Kapatırsanız kod yapısı görsel olarak daha belirsiz olur. |
| `editor.smoothScrolling` | `true` | **Yumuşak Kaydırma.** Sayfa kaydırma animasyonu. Kapatırsanız kaydırma anlık olur (daha az GPU kullanır). |
| `editor.cursorBlinking` | `"smooth"` | **İmleç Yanıp Sönme Stili.** `"blink"`, `"smooth"`, `"phase"`, `"expand"`, `"solid"` seçenekleri var. "Solid" en az kaynak kullanır. |

---

### 🚫 Bölüm 3: Dosya İzleyici Hariç Tutma Listesi

`files.watcherExclude` ayarı, editörün hangi klasörleri **izlemeyeceğini** belirler. Bu, büyük projelerde performans için kritiktir.

**Neden önemli?** Editör, dosya değişikliklerini izler. `node_modules` gibi on binlerce dosya içeren klasörleri izlemek gereksiz CPU/RAM kullanır.

| Kategori | Örüntüler | Neden Hariç Tutulur? |
|----------|-----------|---------------------|
| **Sistem** | `.git/objects/**`, `.DS_Store`, `Thumbs.db` | Git objeleri ve OS önbellek dosyaları. Kod değil. |
| **Node/Web** | `node_modules/**`, `dist/**`, `build/**`, `.next/**`, `.nuxt/**`, `coverage/**`, `.cache/**` | Bağımlılıklar ve derleme çıktıları. Değişiklik izlemeye gerek yok. |
| **Python** | `__pycache__/**`, `.venv/**`, `venv/**` | Python bytecode ve sanal ortamlar. |
| **Mobile** | `ios/Pods/**`, `android/app/build/**`, `.dart_tool/**`, `flutter/bin/cache/**` | iOS/Android/Flutter derleme önbellekleri. |
| **Derleme** | `target/**`, `bin/**`, `obj/**` | Rust, Java, .NET derleme çıktıları. |

> **💡 İpucu:** Projenize özgü büyük klasörler varsa (örn. `data/`, `assets/videos/`), bunları da ekleyebilirsiniz.

---

### 🔍 Bölüm 4: Arama Hariç Tutma Listesi

`search.exclude` ayarı, **Ctrl+Shift+F** aramalarından hangi dosya/klasörlerin hariç tutulacağını belirler.

| Örüntü | Neden Hariç Tutulur? |
|--------|---------------------|
| `**/node_modules` | Binlerce bağımlılık dosyası. Arama sonuçlarını kirletir. |
| `**/dist`, `**/.next` | Derleme çıktıları. Kaynak kod değil. |
| `**/yarn.lock`, `**/package-lock.json` | Otomatik oluşturulan lock dosyaları. Aranacak bir şey yok. |
| `**/*.min.js` | Minify edilmiş JavaScript. Okunamaz, aranmaya değmez. |

---

### ⚙️ Bölüm 5: Diğer Performans Ayarları

Bu ayarlar, editörün genel performansını ve davranışını etkiler.

| Ayar | Varsayılan | Açıklama |
|------|-----------|----------|
| `editor.codeLens` | `false` | **Referans Sayacı.** Fonksiyon/class üstünde "3 references" gibi bilgi gösterir. **Kapalı tutmanız önerilir** çünkü sürekli AST analizi yapar ve büyük projelerde CPU'yu yorar. Açarsanız referans bilgisi görürsünüz ama performans düşer. |
| `workbench.reduceMotion` | `"on"` | **Hareket Azaltma.** Tüm UI animasyonlarını devre dışı bırakır (tab geçişleri, panel açılışları vs.). `"on"` performans için idealdir. `"off"` yaparsanız animasyonlar geri gelir. |
| `editor.minimap.enabled` | `false` | **Minimap (Kod Haritası).** Editörün sağında küçük kod önizlemesi gösterir. **Kapalı tutmanız önerilir** çünkü her satır için render yapar, büyük dosyalarda GPU'yu yorar. Açarsanız hızlı navigasyon sağlar ama kaynak tüketir. |
| `files.autoSave` | `"afterDelay"` | **Otomatik Kaydetme.** `"off"`, `"afterDelay"`, `"onFocusChange"`, `"onWindowChange"` seçenekleri var. "afterDelay" ile belirli bir süre sonra otomatik kaydedilir. Ctrl+S stresinden kurtarır. |
| `files.trimTrailingWhitespace` | `true` | **Satır Sonu Boşluk Temizleme.** Kayıt sırasında satır sonlarındaki gereksiz boşlukları siler. Git diff'lerini temiz tutar ve "whitespace-only" commit kirliliğini önler. Kapatırsanız boşluklar kalır. |

---

### 📊 Performans Etki Özeti

| Ayar | Kaynak Kullanımı | Kapatınca Kazanç |
|------|-----------------|------------------|
| `editor.minimap.enabled` | 🔴 Yüksek (GPU) | Büyük dosyalarda belirgin |
| `editor.codeLens` | 🔴 Yüksek (CPU) | Büyük projelerde belirgin |
| `files.watcherExclude` | 🟠 Orta (CPU/RAM) | Çok dosyalı projelerde kritik |
| `workbench.reduceMotion` | 🟡 Düşük (GPU) | Eski donanımda fark edilir |
| `editor.smoothScrolling` | 🟢 Minimal (GPU) | Nadiren fark edilir |

</details>

This repository hosts the configuration files for my personal AI tool. It is **specially built for the Google Antigravity framework and its Gemini CLI engine**, and is designed to be compatible with any AI platform.

### 🚀 Latest Update (v1.3) - "Autonomy & The Truth Protocol"
- **Mental Upgrade:** Activated `ULTRA-PRO-MAXIMUM-OVERCLOCK MODE` and `thinking_level: "high"`. Upgraded model target to `gemini-3.1-pro-preview`.
- **Dialogue Synchronization (`State Synchronization`):** Calibrated the execution pipeline to the user's conversational state. When a user asks a question, the AI must prioritize natural language response before dispatching further tool operations.
- **The Truth Protocol:** Prioritizes active local environment and chronological file statuses over assumed/training knowledge (`Chronological Reconnaissance`).
- **Tactical Security Framework:** Transformed the AI from an autonomous executioner to a tactical advisor. Destructive actions (like file nuking) now require explicit user mandate rather than acting solely on the "Security > Convenience" doctrine.
- **Adaptive Logging:** Implemented environment-aware logging mechanisms (Antigravity vs. Raw CLI) to prevent redundant log spam and maintain clean workspaces.
- **Editor/Agent Optimization (`settings.json`):**
  - Integrated official `gemini.*` keys for robust agent autonomy (agentMode, codebaseIndexing).
  - Expanded `watcherExclude` to aggressively blacklist CPU-hungry monorepo and system caches (`.turbo`, `.npm`, `.gradle`).
  - Filtered out source maps (`*.map`) via `search.exclude` to prevent AI context pollution during codebase lookups.
  - Enabled GPU acceleration for the integrated terminal to prevent UI freezes during heavy log output.

### 🚀 Previous Update (v1.2) - "System Architecture Redesign"
- **Positive Language:** Removed all "NEVER/DON'T" language, replaced with "use this instead of that" format.
- **Modular Architecture (New Section VI):** Domain-driven folders, small files, deep hierarchies now mandatory.
- **Explicit Cross-References:** Every protocol now references others by section numbers.
- **Tools First:** 3-step decision tree makes built-in tools mandatory.
- **Security:** Counter-Intelligence now proactive, all protocols work coordinately.
- **Manifest:** Added "Structure > Chaos" and "Vigilance > Naivety" principles.

[Click for detailed v1.2 Release Notes](https://github.com/MeteAvci/.gemini/releases/tag/v1.2)

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
    **Example:** Change `model: "gemini-3-pro-preview"` to `model: "gemini-next-gen-alpha"`. (Note: Use a valid model name provided by the platform).

### **How to Control Response Length**

-   **What:** The `max_output_tokens` setting.
-   **Why:** To limit how long the AI's responses can be. Useful for getting shorter, quicker answers or allowing for very long, detailed ones.
-   **How:** Change the number. A lower number means shorter responses.

---

## 3. Core Logic (Advanced & Experimental)

**Warning:** The following sections (`<core_directives>` and `<manifest>`) are the AI's firmware. Modifying them can lead to unpredictable behavior, loops, or loss of core functionality. Edit only if you understand the potential consequences.

-   **What They Are:** These sections define the AI's fundamental rules, like "always read documentation first" (`Truth > Lore`) and "prioritize security" (`Security > Convenience`).
-   **How to Use:** It is recommended to leave these as they are for stable operation. However, you could theoretically change `Simplicity > Complexity` to `Complexity > Simplicity` to encourage the AI to write more elaborate code, at the risk of over-engineering.

---

## ⚡ Editor Performance Settings (`settings.json`)

This section provides detailed documentation for every setting in the `settings.json` file, which optimizes Antigravity and VS Code editor performance.

### 📁 File Location

The `settings.json` file should be placed in the `.gemini` folder of your workspace. These settings directly affect the VS Code editor engine running beneath Antigravity.

---

### 🧠 Section 1: AI & Intelligence Settings

These settings control Antigravity's AI capabilities.

| Setting | Default | Description |
|---------|---------|-------------|
| `antigravity.index.enabled` | `true` | **Project Indexing.** Allows the AI to scan and learn your entire project. If disabled, the AI won't "know" your project—it only sees the currently open file. |
| `antigravity.liveEmbeddings.enabled` | `true` | **Live Embedding Analysis.** Performs real-time semantic analysis as you type. Disabling reduces CPU usage but decreases the AI's "instant" intelligence. |
| `antigravity.contextTracking.level` | `"high"` | **Context Tracking Level.** Can be `"low"`, `"medium"`, or `"high"`. At "high", the AI better understands cross-file relationships and provides proactive suggestions. Lowering it reduces RAM usage. |
| `antigravity.agent.autoFixLints` | `true` | **Auto-Fix Lints.** The AI automatically detects and suggests fixes for code errors (lint errors). If disabled, the AI ignores these errors. |
| `antigravity.agent.webTools.enabled` | `true` | **Web Tools.** Allows the AI to read documentation from the internet. If disabled, the AI is limited to its local knowledge only. |

---

### 🎨 Section 2: Visual Comfort Settings

These settings improve the code reading experience. Performance impact is low but productivity increases.

| Setting | Default | Description |
|---------|---------|-------------|
| `editor.bracketPairColorization.enabled` | `true` | **Colorized Brackets.** Shows each bracket pair in a different color. Disabling makes all brackets the same color, making nested structures harder to read. |
| `editor.guides.bracketPairs` | `true` | **Bracket Pair Guides.** Shows vertical lines indicating which opening bracket matches which closing bracket. Disabling removes this visual aid. |
| `editor.guides.indentation` | `true` | **Indentation Guides.** Shows vertical lines for code block indentation. Disabling makes code structure visually less clear. |
| `editor.smoothScrolling` | `true` | **Smooth Scrolling.** Animates page scrolling. Disabling makes scrolling instant (uses less GPU). |
| `editor.cursorBlinking` | `"smooth"` | **Cursor Blinking Style.** Options: `"blink"`, `"smooth"`, `"phase"`, `"expand"`, `"solid"`. "Solid" uses the least resources. |

---

### 🚫 Section 3: File Watcher Exclusion List

The `files.watcherExclude` setting determines which folders the editor **should not watch**. This is critical for performance in large projects.

**Why is this important?** The editor monitors file changes. Watching folders containing tens of thousands of files like `node_modules` wastes CPU/RAM unnecessarily.

| Category | Patterns | Why Excluded? |
|----------|----------|---------------|
| **System** | `.git/objects/**`, `.DS_Store`, `Thumbs.db` | Git objects and OS cache files. Not code. |
| **Node/Web** | `node_modules/**`, `dist/**`, `build/**`, `.next/**`, `.nuxt/**`, `coverage/**`, `.cache/**` | Dependencies and build outputs. No need to watch for changes. |
| **Python** | `__pycache__/**`, `.venv/**`, `venv/**` | Python bytecode and virtual environments. |
| **Mobile** | `ios/Pods/**`, `android/app/build/**`, `.dart_tool/**`, `flutter/bin/cache/**` | iOS/Android/Flutter build caches. |
| **Build Outputs** | `target/**`, `bin/**`, `obj/**` | Rust, Java, .NET build outputs. |

> **💡 Tip:** If your project has large custom folders (e.g., `data/`, `assets/videos/`), you can add them too.

---

### 🔍 Section 4: Search Exclusion List

The `search.exclude` setting determines which files/folders are excluded from **Ctrl+Shift+F** searches.

| Pattern | Why Excluded? |
|---------|---------------|
| `**/node_modules` | Thousands of dependency files. Pollutes search results. |
| `**/dist`, `**/.next` | Build outputs. Not source code. |
| `**/yarn.lock`, `**/package-lock.json` | Auto-generated lock files. Nothing to search for. |
| `**/*.min.js` | Minified JavaScript. Unreadable, not worth searching. |

---

### ⚙️ Section 5: Other Performance Settings

These settings affect the editor's overall performance and behavior.

| Setting | Default | Description |
|---------|---------|-------------|
| `editor.codeLens` | `false` | **Reference Counter.** Shows information like "3 references" above functions/classes. **Recommended to keep OFF** because it continuously performs AST analysis and strains the CPU in large projects. Enabling it shows reference info but reduces performance. |
| `workbench.reduceMotion` | `"on"` | **Reduce Motion.** Disables all UI animations (tab transitions, panel openings, etc.). `"on"` is ideal for performance. Setting to `"off"` brings back animations. |
| `editor.minimap.enabled` | `false` | **Minimap (Code Map).** Shows a small code preview on the right side of the editor. **Recommended to keep OFF** because it renders every line and strains the GPU in large files. Enabling provides quick navigation but consumes resources. |
| `files.autoSave` | `"afterDelay"` | **Auto Save.** Options: `"off"`, `"afterDelay"`, `"onFocusChange"`, `"onWindowChange"`. With "afterDelay", files are automatically saved after a set period. Eliminates Ctrl+S anxiety. |
| `files.trimTrailingWhitespace` | `true` | **Trim Trailing Whitespace.** Removes unnecessary whitespace at the end of lines when saving. Keeps git diffs clean and prevents "whitespace-only" commit pollution. Disabling leaves whitespace intact. |

---

### 📊 Performance Impact Summary

| Setting | Resource Usage | Gain When Disabled |
|---------|----------------|-------------------|
| `editor.minimap.enabled` | 🔴 High (GPU) | Noticeable in large files |
| `editor.codeLens` | 🔴 High (CPU) | Noticeable in large projects |
| `files.watcherExclude` | 🟠 Medium (CPU/RAM) | Critical in multi-file projects |
| `workbench.reduceMotion` | 🟡 Low (GPU) | Noticeable on older hardware |
| `editor.smoothScrolling` | 🟢 Minimal (GPU) | Rarely noticeable |

