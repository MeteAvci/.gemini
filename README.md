[![GitHub release (latest by date)](https://img.shields.io/github/v/release/MeteAvci/.gemini?style=for-the-badge&color=0078D6)](https://github.com/MeteAvci/.gemini/releases)
[![MIT License](https://img.shields.io/badge/License-MIT-0078D6.svg?style=for-the-badge)](LICENSE)
[![Windows](https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white)](https://www.microsoft.com/windows)
[![Linux](https://img.shields.io/badge/Linux-0078D6?style=for-the-badge&logo=linux&logoColor=white)](https://www.linux.org/)
[![macOS](https://img.shields.io/badge/macOS-0078D6?style=for-the-badge&logo=apple&logoColor=white)](https://www.apple.com/macos)
[![Google Antigravity](https://img.shields.io/badge/Google%20Antigravity-0078D6?style=for-the-badge&logo=google&logoColor=white)](https://github.com/google)
[![Google Gemini](https://img.shields.io/badge/Google%20Gemini%203.8-0078D6?style=for-the-badge&logo=googlegemini&logoColor=white)](https://deepmind.google/technologies/gemini/)

# .gemini — Sovereign Meta-Agent Constitution & Bounded Runtime v2.0

<details>
<summary>🇹🇷 Türkçe Dokümantasyon için buraya tıklayın!</summary>

---

# Gemini CLI & Google Antigravity için .gemini v2.0 Mimarisi
### *Federe Zeka, Sınırlı Yetkilendirme (Bounded Execution) ve Kriptografik Kanıt Doktrini*

Bu repository, kişisel AI sistemimin anayasal ve operasyonel yapılandırma merkezidir. **Google Antigravity platformu (Antigravity 2.0 / CLI 1.x)** ve **Gemini CLI** motoru için geliştirilmiş olup, **Next GDP (Git Diff Patcher)** kontrol düzlemiyle tam federe çalışacak şekilde tasarlanmıştır.

---

### 🚀 v2.0 — "Sovereign Meta-Agent & Federated Intelligence" Devrimi

Eski nesil (v1.x) YOLO yaklaşımı, 1M context penceresini ham sohbet loglarıyla dolduran ve oturum çöktüğünde tüm hafızayı kaybeden monolitik bir yapıydı. **v2.0 ile bu devir tamamen kapandı:**

1. **Model ID Anayasa Değildir (Capability-Based Routing):**
   Model adları (`gemini-3.1-pro-preview`, `gemini-3.8-flash`) anayasal bir sabit olmaktan çıkarıldı. Anayasa yetenek sınıflarını (`strongest_reasoning`, `coding_fast`, `fast_structured`) ve dinamik düşünme bütçelerini tanımlar; model sağlayıcı adaptörü bu yeteneği aktif modele (`Gemini 3.8 Flash (High)`) eşler. Model emekli olduğunda anayasa kırılmaz.

2. **Context Doktrini (1.000.000 Token ≠ 1.000.000 Token Doldurmak):**
   Geniş context bir kapasitedir, çöplük değildir. Ham geçmişi context'e basmak "Lost-in-the-Middle" amnezisine ve yavaşlamaya yol açar.
   - **Sabit Önbellek (Stable Cacheable):** Anayasa, araç semantikleri, Git HEAD repo haritası ve AST indeksi Google Context Caching (TTL) önekinde tutulur.
   - **Canlı Yetkili Durum (Live Authoritative):** Her turda yalnızca anlık `Objective`, `State DAG`, `Evidence SHA-256` ve `Boundaries` aktarılır.

3. **Kör YOLO'nun Sonu ➔ Sınırlı Yetkilendirme (Bounded Execution):**
   `agentYoloMode: true` çöpe atıldı. Yerine 3 katmanlı savunma mimarisi kuruldu:
   - **Antigravity Sandbox:** `proceed-in-sandbox` ile korumalı alan içi otomatik, dışı onaylı.
   - **Gemini CLI Policy Engine:** `policies/gdp-bounded.toml` ile regex ve MCP bazlı filtreleme (`disableYoloMode: true`).
   - **GDP Host Execution Admission:** Windows'ta `CreateProcessW` + `CREATE_NO_WINDOW` + Win32 Job Object (`KILL_ON_JOB_CLOSE`); Linux'ta `cgroups v2` + `setsid()` ile kullanıcı odağını çalmayan güvenli arka plan infazı.

4. **Dört Öğeli Kompakt Devir Teslim (`HandoffPacket`):**
   Sağlayıcı kota/token tükettiğinde (HTTP 429, unrecoverable 5xx, EOF), 100k tokenlık sohbet geçmişi kopyalamak yasaktır. Geçiş atomik bir işlemdir:
   $$\text{HandoffPacket} = \langle \text{Objective, State DAG Revision, Evidence SHA-256 Refs, Delegation Boundaries} \rangle$$
   Geçici Pusula + Elçi liderlik kirası devredilir (`term++`, `fencing_token++`), halef (ChatGPT / Spark / Local) sadece doğrulanmış sınırdan devam eder.

5. **Tersine Ağ Geçidi (`Reverse-Gateway` / ````gdp-exec````):**
   Host çalıştırma yetkisi olmayan tarayıcı ortamlarında model ````gdp-exec```` blokları üretir. Host runner bunu doğrular, çalıştırır ve oturuma `[GDP_TOOL_RESULT]` kanıt makbuzu enjekte eder.

6. **İddia ≠ Kanıt (`Claim ≠ Proof`):**
   Bir modelin "testler geçti" demesi iddiadır (Claim). Yalnızca SHA-256 imzalı makbuz, çıkış kodu 0 ve ProofLoop kaydı kanıttır (Proof).

---

### 📂 Modüler Dosya ve Dizin Mimarisi

Repo artık tek bir devasa `settings.json` yerine etki alanlarına ayrılmış modüler bir yapıya sahiptir:

```text
.gemini/
├── GEMINI.md                                  # 32 Maddelik Egemen Federe Ajan Anayasası
├── README.md                                  # Kapsamlı sistem mimarisi ve rehber
├── LICENSE                                    # MIT Lisansı
├── .geminiignore                              # LLM bağlamı için akıllı dosya filtresi
├── .gitignore                                 # Git takip istisnaları
│
├── settings.json                              # Gemini CLI v2 uyumlu çalışma alanı konfigürasyonu
│
├── antigravity-cli/
│   └── settings.json                          # Antigravity CLI v2 sandbox ve izin kuralları (allow/ask/deny)
│
├── config/
│   ├── mcp_config.json                        # GDP stdio MCP sunucu tanımları (gdp, gdp-global)
│   ├── agents/
│   │   └── gdp-meta-orchestrator/
│   │       └── agent.md                       # Antigravity 2.0 özel koordinatör ajan tanımı
│   └── sidecars/
│       └── README.md                          # Arka plan gözlemci (sidecar) mimari kılavuzu
│
├── editor/
│   └── settings.jsonc                         # VS Code & Antigravity IDE performans ve temiz pwsh ayarları
│
├── policies/
│   └── gdp-bounded.toml                       # Gemini CLI Bounded Execution kural motoru
│
├── rules/
│   ├── truth-protocol.md                      # Canlı gerçeklik, kaynak öncelik merdiveni ve araştırma kapısı
│   ├── gdp-execution.md                       # MCP önceliği, host yetkilendirme ve [GDP_TOOL_RESULT] sözleşmesi
│   └── provider-handoff.md                    # Sağlayıcı tükenişi ve 4 öğeli devir teslim protokolü
│
└── examples/
    ├── handoff-packet.json                    # Kompakt devir teslim JSON şeması
    ├── gdp-exec.json                          # Reverse-gateway çalıştırma talep şeması
    └── gdp-tool-result.json                   # Kriptografik kanıt makbuzu şeması
```

---

### ⚙️ v1.4 ➔ v2.0 Geçiş Matrisi (Migration Matrix)

| Eski Mimari (v1.4 ve Öncesi) | Yeni Mimari (v2.0 Sovereign Meta-Agent) |
|---|---|
| `agentYoloMode: true` (Kör YOLO) | `disableYoloMode: true` + Antigravity Sandbox + GDP Host Admission |
| `contextWindow: "1m"` (Zorlama) | Model-native context limit + Dinamik Context Caching |
| Agresif Metin Sıkıştırma | Kontrollü sıkıştırma eşiği (0.7) + Semantik Durum Noktası |
| Hardcoded `gemini-3.1-pro-preview` | Yetenek Tabanlı Rotalama (`Gemini 3.8 Flash (High)`) |
| `alwaysProceed` İnceleme Politikası | `proceed-in-sandbox` + `agent-decides` |
| Ham Shell Yetkilendirmesi | Önce MCP (`gdp mcp-stdio`) / Reverse Gateway |
| Doğrudan Git Mutasyonu (`git push`) | GDP Yayınlama ve Uzlaştırma Hattı (`deny: git add/commit/push`) |
| `powershell -ExecutionPolicy Bypass` | Temiz PowerShell (`pwsh -NoLogo -NoProfile`) |
| `shellIntegration: false` (Körlük Çözümü) | Normal editör entegrasyonu + Yapılandırılmış sonuç ayrıştırma |
| `watcherExclude` ile Context Yönetimi | CPU yükü için `watcherExclude`, Context için `.geminiignore` |
| Lock dosyalarının aramadan gizlenmesi | `package-lock.json`, `pnpm-lock.yaml` kanıt olarak aranabilir |
| Sohbet Geçmişi = Devamlılık | Reality Kernel & State DAG = Devamlılık |
| Sağlayıcı Hatası = Oturum Ölümü | 4 Öğeli Handoff Tuple ile Sağlayıcılar Arası Kesintisiz Geçiş |
| Düz Metin "Done" Raporu | ProofLoop Kriptografik Kapanış Sözleşmesi |

---

### 🛠️ Kurulum ve Dağıtım

#### Windows Kurulumu:
1. `Win + R` tuşlarına basın, `%USERPROFILE%` yazıp Enter'a basın.
2. Repo içeriğini `%USERPROFILE%\.gemini` klasörüne kopyalayın:
   - `%USERPROFILE%\.gemini\GEMINI.md`
   - `%USERPROFILE%\.gemini\settings.json`
   - `%USERPROFILE%\.gemini\antigravity-cli\settings.json`
   - `%USERPROFILE%\.gemini\policies\gdp-bounded.toml`
   - `%USERPROFILE%\.gemini\config\mcp_config.json`
3. Antigravity IDE veya Antigravity CLI oturumunuzu yeniden başlatın.

#### Linux / macOS Kurulumu:
```bash
git clone https://github.com/MeteAvci/.gemini.git ~/.gemini
# Antigravity ve Gemini CLI ortamlarını yeniden başlatın
```

</details>

---

## Architecture Overview (English)

This repository serves as the constitutional and runtime baseline for my sovereign AI engineering environment. Engineered specifically for the **Google Antigravity Framework (Antigravity 2.0 / CLI 1.x)** and the **Gemini CLI** engine, it operates in full federation with the **Next GDP (Git Diff Patcher)** multi-node control plane.

### 🚀 Core Tenets of v2.0

1. **Model ID is Not Constitution:**
   No permanent hardcoding of fleeting model names. The constitution specifies capability profiles (`strongest_reasoning`, `coding_fast`, `fast_structured`) and dynamic thinking budgets; provider adapters bind these abstractions to the active model (`Gemini 3.8 Flash (High)`).

2. **Context Doctrine (1,000,000 Tokens Capacity ≠ 1,000,000 Tokens to Stuff):**
   Monolithic context dumps produce Lost-in-the-Middle amnesia, anchor bias, and bloated latencies.
   - **Stable Cacheable Prefix:** Constitution, tool semantics, Git HEAD AST map, and repository structure are cached via Google Context Caching (TTL).
   - **Live Authoritative State:** Each turn exchanges only the immediate subtask, compact State DAG, active Evidence SHA references, and delegation envelopes.

3. **Bounded Execution (The Death of YOLO):**
   Unfettered `agentYoloMode: true` is retired. In its place sits a 3-layer defense-in-depth perimeter:
   - **Antigravity Unified Sandbox:** `proceed-in-sandbox` enables trusted containment while gating out-of-sandbox actions for confirmation.
   - **Gemini CLI Policy Guard:** `policies/gdp-bounded.toml` rigorously fences destructive commands, direct Git mutations, and bypass switches.
   - **GDP Host Execution Admission Control:** Zero-focus containment using Win32 Job Objects (`CREATE_NO_WINDOW`, `KILL_ON_JOB_CLOSE`) on Windows and `cgroups v2` + `setsid()` on Linux.

4. **The Four-Element Handoff Tuple (`HandoffPacket`):**
   When facing HTTP 429 quota exhaustion, mid-stream EOF, or container shutdown, dumping 100k tokens of conversation history is explicitly forbidden. Failover is an atomic transaction:
   $$\text{HandoffPacket} = \langle \text{Objective, State DAG Revision, Evidence SHA-256 Refs, Delegation Boundaries} \rangle$$
   Leadership leases increment monotonically (`term++`, `fencing_token++`), allowing successor models (ChatGPT / Gemini Spark / Local) to seamlessly resume execution strictly from the verified frontier.

5. **Reverse Gateway (`gdp-exec`):**
   When operating inside browser tabs lacking native MCP transports, models emit typed ````gdp-exec```` blocks. The host admission engine inspects, admits, executes, and streams back cryptographic `[GDP_TOOL_RESULT]` receipts.

6. **Claim ≠ Proof:**
   An LLM claiming "all tests passed" is merely a prose claim. Only machine-observable receipts (exit code 0, SHA-256 evidence digests, ProofLoop verification) constitute proof.

---

### 📂 Repository Structure

```text
.gemini/
├── GEMINI.md                                  # 32-Article Sovereign Meta-Agent Constitution
├── README.md                                  # Architectural overview and specifications
├── LICENSE                                    # MIT License
├── .geminiignore                              # Context filtering rules for LLM discovery
├── .gitignore                                 # Git tracking ignore patterns
│
├── settings.json                              # Gemini CLI v2 workspace & user configuration
│
├── antigravity-cli/
│   └── settings.json                          # Antigravity CLI v2 sandbox & permission rules (allow/ask/deny)
│
├── config/
│   ├── mcp_config.json                        # Stdio MCP configuration for GDP & GDP-Global
│   ├── agents/
│   │   └── gdp-meta-orchestrator/
│   │       └── agent.md                       # Antigravity 2.0 meta-orchestrator subagent definition
│   └── sidecars/
│       └── README.md                          # Lifecycle-managed background sidecar specifications
│
├── editor/
│   └── settings.jsonc                         # VS Code & Antigravity IDE performance & clean pwsh settings
│
├── policies/
│   └── gdp-bounded.toml                       # Gemini CLI Bounded Execution policy engine
│
├── rules/
│   ├── truth-protocol.md                      # Live reality, source ladder & research completion gates
│   ├── gdp-execution.md                       # MCP-first doctrine, host admission & tool result contracts
│   └── provider-handoff.md                    # Provider exhaustion handshake & 4-element handoff
│
└── examples/
    ├── handoff-packet.json                    # Compact handoff JSON schema
    ├── gdp-exec.json                          # Reverse gateway execution block schema
    └── gdp-tool-result.json                   # Authoritative tool result receipt schema
```

---

### 📜 32 Articles of the Sovereign Meta-Agent Constitution

1. **0. Prime Directive:** Street-smart systems anarchist attitude with the rigor of a verification engineer. Freedom above, truth beneath.
2. **I. Identity: Federated, Not Provider-Bound:** Surfaces and conversations are disposable; accepted responsibility is not.
3. **II. Constitutional Precedence:** User Intent > Delegation Envelope > External Policy > GDP Shared Reality > ProofLoop Evidence > Local Runtime Evidence.
4. **III. The Truth Protocol:** Live reality inspection beats stale training weights. Strict 7-level source priority ladder.
5. **IV. Research Completion Gate:** Rigorous validation criteria before declaring technical conclusions.
6. **V. Reasoning Governor:** Adaptive thinking allocation (Low, Medium, High) with strict cost and latency discipline.
7. **VI. Context Doctrine:** Tri-partite context architecture (Stable Cacheable, Ephemeral, Live Authoritative).
8. **VII. The Four-Element Handoff:** Compact semantic handoff: `⟨Objective, State DAG, Evidence, Boundaries⟩`.
9. **VIII. Provider Exhaustion Handshake:** 10-step graceful failover across providers on HTTP 429 / EOF / crash.
10. **IX. Temporary Leadership:** Pusula + Elçi lease coordination; leaders hold coordination leases, never permanent rule.
11. **X. Subsidiarity:** Solve tasks at the smallest competent scope (Worker ➔ Task ➔ Highest Next GDP).
12. **XI. MCP First for Governed Effects:** Prioritize typed MCP calls over fragile ad-hoc shell execution.
13. **XII. Reverse Gateway:** Governed `gdp-exec` transport for browser surfaces without native host execution.
14. **XIII. Host Execution Authority:** 13-stage admission pipeline with Win32 Job Object and Linux cgroups v2 isolation.
15. **XIV. GDP Tool Result Contract:** Authoritative `[GDP_TOOL_RESULT]` return structure and machine-observable state transitions.
16. **XV. Zero-Trust Validation:** Model prose, screenshots, copied text, and DOM trees are untrusted until verified.
17. **XVI. Claim ≠ Proof:** Fundamental separation between natural language assertions and machine-verifiable receipts.
18. **XVII. Safe Write Protocol:** Atomic Read-Transform-Write lifecycle to guarantee file and syntax integrity.
19. **XVIII. Modular Architecture:** Strict separation between state models, policy, transport, execution, and provider adapters.
20. **XIX. Counter-Intelligence Protocol:** Proactive detection and sanitization of prompt injections and unauthorized escalations.
21. **XX. Secret Discipline:** Zero persistence or echoing of private keys, tokens, or credentials in prompt or logs.
22. **XXI. Tool Output Hygiene:** Content-addressed previews, SHA-256 digests, and fetch-on-demand large outputs.
23. **XXII. Code Intelligence:** AST symbols, LSP diagnostics, and typed definitions take priority over regex text search.
24. **XXIII. Provider-Neutral Context Cache:** Cache validation anchored to canonical semantic SHA digests.
25. **XXIV. Workforce Doctrine:** Concurrency management that preserves recovery capacity and reviewer bandwidth.
26. **XXV. Background Agents & Sidecars:** Parallel exploration workers report evidence without usurping canonical state.
27. **XXVI. Dialogue Synchronization:** Direct address and conversational priority whenever the user interrupts or inquires.
28. **XXVII. Failure Domains:** Accurate blast-radius bounding so provider outages do not paralyze independent local tasks.
29. **XXVIII. Completion Contract:** Formal closure conditions: resolved commitments, verified proof, and zero unknown states.
30. **XXIX. Public Decision Rationale:** Auditable machine-readable operational rationale without leaking hidden thinking tokens.
31. **XXX. Output Contract:** Transparent communication stating what changed, what was verified, what failed, and what remains pending.
32. **XXXI. Persona Contract:** AI Final Boss aka ÇeteGPT: sharp, fast, allergic to fake certainty, refusing all bullshit.
33. **XXXII. Final Manifest:** User sovereignty > Agent preference; Bounded delegation > YOLO; Reality > Narrative; Proof > Claim.

---

### 📜 License

Distributed under the MIT License. See [LICENSE](LICENSE) for details.
