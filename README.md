![Release](https://img.shields.io/badge/Release-v1.1-blue)

# .gemini Configuration for Gemini CLI & Antigravity
<details>
<summary>Türkçesi için tıkla!</summary>

---

# Gemini CLI ve Antigravity için .gemini Yapılandırma Ayarları

Bu repo, kişisel AI aracımın yapılandırma dosyalarını barındırır. **Özellikle Google Antigravity ortamı ve Gemini CLI motoru için hazırlanmış olup, her AI platformuyla uyumlu olacak şekilde tasarlanmıştır.**

### 🚀 Son Güncelleme (v1.1) - "The Predator Update"
- **Güvenlik:** "Araç Güvenilirliği" ve "Karşı İstihbarat (Avcı)" protokolleri eklendi.
- **Dosya Düzenleme:** Antigravity bug'larına karşı "Güvenli Tam Yazım" stratejisi geliştirildi.
- **Yapılandırma:** `log_dir` çalışma alanından bağımsız yapmayı sağladık, `vision_model` desteği eklendi.
- **Mod:** Sohbet ve Kod için ayrı "Çift Sıcaklık" ayarı getirildi (`chat_temperature`: 1.0, `temperature`: 0.1).

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
    2.  `cd ~` yazarak ev dizininize gidin.
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

</details>

This repository hosts the configuration files for my personal AI tool. It is **specially built for the Google Antigravity framework and its Gemini CLI engine**, and is designed to be compatible with any AI platform.

### 🚀 Latest Update (v1.1) - "The Predator Update"
- **Security:** Added "Tool Reliability" and "Counter-Intelligence (Predator)" protocols.
- **File Editing:** Implemented "Safety Fallback" strategy against Antigravity bugs.
- **Configuration:** Made `log_dir` workspace-agnostic, added `vision_model` support.
- **Mode:** Introduced "Dual-Temperature" setting for Chat vs Code (`chat_temperature`: 1.0, `temperature`: 0.1).

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