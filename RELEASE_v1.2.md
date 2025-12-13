# v1.2 - "The Big Picture Update"

<details>
<summary>🇹🇷 Türkçe için tıkla!</summary>

---

# v1.2 - "Büyük Resim Güncellemesi"

Bu sürüm, AI'nın dar kapsamlı düşünme eğilimini düzeltmeye ve OS uyumluluğunu artırmaya odaklanmaktadır.

## 🎯 Temel Değişiklikler

### Yapısal Yeniden Düzenleme
- **Persona Önceliği:** `<persona_instructions>` artık dosyanın en başında (Bölüm I). AI'nın kimliği ve tonu artık ilk okunan şey.
- **Romen Rakamları:** Tüm bölüm başlıkları `1, 2, 3, 4, 5` yerine `I, II, III, IV, V` olarak güncellendi.
- **Identity Genişletildi:** "Maximum Intensity" direktifi Identity'e entegre edildi. AI artık varsayılan olarak "MAXIMUM effort and FULL SCOPE" ile çalışıyor.

### Yeni Direktifler

#### 🛠️ Tools First (Önce Araçlar)
Shell komutları artık son çare. AI, aşağıdaki OS-agnostik araçları öncelikli kullanacak:
- `find_by_name`, `grep_search`, `list_dir`, `view_file`, `view_file_outline`
- `write_to_file`, `replace_file_content`, `multi_replace_file_content`
- `read_url_content`, `search_web`, `browser_subagent`
- `generate_image`, `codebase_search`, `view_code_item`
- ve diğerleri...

#### 🖥️ OS Awareness (OS Farkındalığı)
PowerShell için somut örnekler eklendi:
| PowerShell | Bash Karşılığı |
|------------|----------------|
| `;` | `&&` |
| `Get-ChildItem` | `ls` |
| `Remove-Item -Recurse -Force` | `rm -rf` |
| `Select-String` | `grep` |
| `Move-Item a b` | `mv a b` |

#### 🔍 Debug Protocol (Hierarchy-First)
Yeni debugging prensibi: **Kökten yaprağa, yapraktan köke değil.**
- Bir alt bileşenin davranışı üst bileşene bağlıdır (CSS `overflow`, stacking context, vb.)
- Yerel mantık doğru ama davranış yanlışsa → bug üst seviyede
- Statik tanımları suçlamadan önce dinamik override'ları ara

### Dil ve Ton İyileştirmeleri

#### ✅ Pozitif Çerçeveleme
Tüm negatif ifadeler pozitife çevrildi:
| Eski | Yeni |
|------|------|
| "NEVER use replace_file_content" | "Prefer write_to_file" |
| "ABANDON replace_file_content" | "Use write_to_file exclusively" |
| "forbidden from reducing effort" | "default is MAXIMUM effort" |

#### 🔓 Esneklik
Safe Write Protocol artık daha esnek:
- Tam dosya yeniden yazımı **tercih edilen** yöntem, **zorunlu** değil
- Basit, izole değişiklikler için kısmi düzenlemeler kabul edilebilir

## 📁 Etkilenen Dosyalar
- `GEMINI.md` - Ana yapılandırma dosyası
- `README.md` - Changelog güncellendi

## ⚠️ Breaking Changes
Yok. Mevcut kullanım tam uyumlu.

---

</details>

This release focuses on fixing the AI's tendency toward narrow-scope thinking and improving OS compatibility.

## 🎯 Core Changes

### Structural Reorganization
- **Persona Priority:** `<persona_instructions>` now leads the file (Section I). The AI's identity and tone are read first.
- **Roman Numerals:** All section headers updated from `1, 2, 3, 4, 5` to `I, II, III, IV, V`.
- **Identity Expanded:** "Maximum Intensity" directive integrated into Identity. AI now defaults to "MAXIMUM effort and FULL SCOPE".

### New Directives

#### 🛠️ Tools First
Shell commands are now last resort. The AI will prioritize these OS-agnostic tools:
- `find_by_name`, `grep_search`, `list_dir`, `view_file`, `view_file_outline`
- `write_to_file`, `replace_file_content`, `multi_replace_file_content`
- `read_url_content`, `search_web`, `browser_subagent`
- `generate_image`, `codebase_search`, `view_code_item`
- and more...

#### 🖥️ OS Awareness
Concrete PowerShell examples added:
| PowerShell | Bash Equivalent |
|------------|-----------------|
| `;` | `&&` |
| `Get-ChildItem` | `ls` |
| `Remove-Item -Recurse -Force` | `rm -rf` |
| `Select-String` | `grep` |
| `Move-Item a b` | `mv a b` |

#### 🔍 Debug Protocol (Hierarchy-First)
New debugging principle: **Root to leaf, not leaf to root.**
- A child's behavior depends on ancestor state (CSS `overflow`, stacking contexts, etc.)
- If local logic is correct but behavior is wrong → bug is upstream
- Search for dynamic overrides before blaming static definitions

### Language & Tone Improvements

#### ✅ Positive Framing
All negative language converted to positive:
| Old | New |
|-----|-----|
| "NEVER use replace_file_content" | "Prefer write_to_file" |
| "ABANDON replace_file_content" | "Use write_to_file exclusively" |
| "forbidden from reducing effort" | "default is MAXIMUM effort" |

#### 🔓 Flexibility
Safe Write Protocol is now more flexible:
- Full file rewrites are the **preferred** method, not **mandatory**
- Partial edits acceptable for simple, isolated changes

## 📁 Files Changed
- `GEMINI.md` - Main configuration file
- `README.md` - Changelog updated

## ⚠️ Breaking Changes
None. Fully backward compatible.
