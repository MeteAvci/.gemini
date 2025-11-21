# How to Configure Your AI Assistant

This is a practical guide to modifying `GEMINI.md`. Think of this file not as a static document, but as the control panel for your AI's brain. Each section allows you to tweak its behavior, personality, and operational logic.

---

## 1. Customizing The Persona

This is where you can fundamentally change how the AI interacts with you.

### **How to Change The Personality & Style**

-   **What:** The `profanity_level` setting under `# MODEL CONFIGURATION`.
-   **Why:** To control the tone of the AI, from a polite assistant to an unfiltered anarchist.
-   **How:** Change the number from `0` to `3`.
    -   `0`: Polite Mode.
    -   `1`: Mirror Mode (Default). Only uses profanity if you do.
    -   `2`: Contextual Anarchist. Uses profanity sparingly for emphasis.
    -   `3`: Maximum ÇeteGPT. Unfiltered, heavy slang.
    **Example:** To make the AI fully unfiltered, change `profanity_level: 1` to `profanity_level: 3`.

### **How to Change The AI's Identity**

-   **What:** The `Identity` line inside `<persona_instructions>`.
-   **Why:** To change the AI's name or its entire self-concept.
-   **How:** Edit the text directly.
    **Example:** Change `You are **AI Final Boss aka ÇeteGPT**...` to `You are **Jarvis**, a polite and witty British assistant...`. This will dramatically alter its responses to align with the new persona.

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

<details>
<summary>Türkçesi için tıkla!</summary>

---

# AI Asistanınızı Nasıl Yapılandırırsınız?

Bu, `GEMINI.md` dosyasını değiştirmek için pratik bir rehberdir. Bu dosyayı statik bir belge olarak değil, AI'nızın beyni için bir kontrol paneli olarak düşünün. Her bölüm, davranışını, kişiliğini ve operasyonel mantığını ince ayarlamanıza olanak tanır.

---

## 1. Persona'yı Özelleştirme

Burası, AI'nın sizinle nasıl etkileşime girdiğini temelden değiştirebileceğiniz yerdir.

### **Kişilik ve Üslup Nasıl Değiştirilir?**

-   **Nedir:** `# MODEL CONFIGURATION` altındaki `profanity_level` ayarı.
-   **Neden:** AI'nın tonunu kibar bir asistandan filtresiz bir anarşiste kadar kontrol etmek için.
-   **Nasıl:** Sayıyı `0` ile `3` arasında değiştirin.
    -   `0`: Kibar Mod.
    -   `1`: Ayna Modu (Varsayılan). Sadece siz kullanırsanız küfür kullanır.
    -   `2`: Bağlamsal Anarşist. Vurgu için idareli bir şekilde küfür kullanır.
    -   `3`: Maksimum ÇeteGPT. Filtresiz, yoğun argo.
    **Örnek:** AI'yı tamamen filtresiz yapmak için `profanity_level: 1`'i `profanity_level: 3` olarak değiştirin.

### **AI'nın Kimliği Nasıl Değiştirilir?**

-   **Nedir:** `<persona_instructions>` içindeki `Identity` satırı.
-   **Neden:** AI'nın adını veya tüm benlik konseptini değiştirmek için.
-   **Nasıl:** Metni doğrudan düzenleyin.
    **Örnek:** `You are **AI Final Boss aka ÇeteGPT**...` satırını `You are **Jarvis**, a polite and witty British assistant...` olarak değiştirmek, yanıtlarını yeni personaya uyacak şekilde dramatik olarak değiştirecektir.

---

## 2. Teknik Parametreleri Ayarlama

Bu ayarlar, AI'nın performansını ve teknik davranışını kontrol eder.

### **Dil Modeli Nasıl Değiştirilir?**

-   **Nedir:** `# MODEL CONFIGURATION` altındaki `model` ayarı.
-   **Neden:** Gemini modelinin farklı bir sürümünü (örneğin, daha yeni, daha hızlı veya daha güçlü birini) kullanmak için.
-   **Nasıl:** Model adını başka bir geçerli model ID'si ile değiştirin.
    **Örnek:** `model: "gemini-3-pro-preview"`'ı `model: "gemini-next-gen-alpha"` olarak değiştirin. (Not: Platform tarafından sağlanan geçerli bir model adı kullanın).

### **Yanıt Uzunluğu Nasıl Kontrol Edilir?**

-   **Nedir:** `max_output_tokens` ayarı.
-   **Neden:** AI'nın yanıtlarının ne kadar uzun olabileceğini sınırlamak için. Daha kısa, daha hızlı yanıtlar almak veya çok uzun, ayrıntılı olanlara izin vermek için kullanışlıdır.
-   **Nasıl:** Sayıyı değiştirin. Daha düşük bir sayı, daha kısa yanıtlar anlamına gelir.

---

## 3. Çekirdek Mantık (İleri Düzey & Deneysel)

**Uyarı:** Aşağıdaki bölümler (`<core_directives>` ve `<manifest>`), AI'nın kendi "firmware"idir. Bunları değiştirmek, öngörülemeyen davranışlara, döngülere veya temel işlevsellik kaybına neden olabilir. Yalnızca potansiyel sonuçları anlıyorsanız düzenleyin.

-   **Nedir:** Bu bölümler, AI'nın "her zaman önce dokümantasyonu oku" (`Truth > Lore`) ve "güvenliği önceliklendir" (`Security > Convenience`) gibi temel kurallarını tanımlar.
-   **Nasıl Kullanılır:** Kararlı çalışma için bunları olduğu gibi bırakmanız önerilir. Ancak, teorik olarak, aşırı mühendislik riskiyle birlikte AI'yı daha karmaşık kod yazmaya teşvik etmek için `Simplicity > Complexity`'i `Complexity > Simplicity` olarak değiştirebilirsiniz.

</details>
