# Norway Legal Research MCP Server (`no-legal-mcp`)

**[Norsk](#lang-no) | [English Documentation](#english-documentation)**

---

<a id="lang-no"></a>
## Juridisk MCP-server for Norsk Lovgivning og Rettspraksis (`no-legal-mcp`) — Norsk

### Om dette depotet

Dette depotet inneholder en Model Context Protocol (MCP) server som kobler din AI-applikasjon (Claude Desktop, Cursor, Windsurf, VS Code / Copilot, Cline eller Antigravity) direkte til Lovdata (`lovdata.no`) og rettsavgjørelser fra tingrettene, de 6 lagmannsrettene og Norges Høyesterett.

### Installasjon (Valg av AI-applikasjon)

1. **Last ned:** Klikk på **`<> Code` -> `Download ZIP`** øverst til høyre og pakk ut mappen på datamaskinen.
2. **Start installasjonen:** Dobbeltklikk på **`Click_Here_To_Install_Windows.bat`** (Windows) eller **`Click_Here_To_Install_Mac.command`** (macOS).
3. **Velg AI-klient:** Kryss av for AI-programmene du bruker (Claude, Cursor, Windsurf, VS Code, Antigravity), klikk installer og start AI-applikasjonen på nytt.

**Sikkerhetsmerknad:** Installasjonsprogrammet opererer kun i lesemodus (read-only) og rører ingen personlige filer på datamaskinen din.

### Domstolsnivåer og offisielle kilder

| Instans | Domstoler som dekkes |
|:---|:---|
| **1. instans (Tingrettene og Forliksråd)** | 23 Tingretter (District Courts), Jordskifteretter (Land Consolidation Courts) & Forliksråd |
| **2. instans (De 6 Lagmannsrettene)** | 6 Lagmannsretter (Borgarting, Eidsivating, Agder, Gulating, Frostating, Hålogaland) |
| **3. instans (Norges Høyesterett & EFTA-domstolen)** | Norges Høyesterett (Supreme Court of Norway) & EFTA Court |

- **Lovdata API (api.lovdata.no) & Lovdata Open Legal Data (lovdata.no):** [https://api.lovdata.no/om-api-tjenesten/](https://api.lovdata.no/om-api-tjenesten/) (`lovdata.no`, `api.lovdata.no`, `stortinget.no`, `regjeringen.no`)
- **Lovdata Rettsavgjørelser (Høyesterett, Lagmannsrettene & Tingrettene — lovdata.no):** [https://lovdata.no](https://lovdata.no) (`lovdata.no`, `domstol.no`)

---

<a id="english-documentation"></a>
## English Documentation

Model Context Protocol (MCP) server providing live, read-only access to **Norway (NO)** legislation, official gazettes, multi-tier judicial decisions (First Instance, Regional/Cantonal/Appellate, and Supreme/Constitutional courts, including HTML and PDF full-text extraction), and statutory citation verification across all major AI clients (**ChatGPT Desktop, OpenAI Codex CLI, Claude Desktop, Claude Code CLI, Cursor, Windsurf, VS Code / GitHub Copilot / Cline / Roo Code, Google Antigravity / Gemini CLI, Perplexity, and Continue.dev**).

---

### Interactive Desktop Setup (Select Your AI Assistant)

This package includes a graphical installer for legal practitioners and non-technical users that lets you select which AI application(s) you use:

1. **Download:** Click **`<> Code`** at the top right of this repository, select **`Download ZIP`**, and extract the folder to your computer.
2. **Run the Setup Utility:**
   - **Windows:** Double-click `Click_Here_To_Install_Windows.bat`
   - **macOS:** Double-click `Click_Here_To_Install_Mac.command`
3. **Select Your AI Client(s) & Connect:** Check the box(es) for the AI assistant(s) installed on your computer (**ChatGPT Desktop & OpenAI Codex CLI**, **Claude Desktop & Claude Code CLI**, **Cursor**, **Windsurf**, **VS Code / GitHub Copilot / Cline / Roo Code**, **Google Antigravity / Gemini CLI**, or **Perplexity / Continue.dev**), click **Install to Selected AI Clients**, and restart your selected AI application.

**System Integrity Note:** The setup utility operates strictly in read-only mode with respect to your personal files and documents. It installs an isolated Python runtime inside the extracted folder and registers the server entry only in the AI client configuration files you select.

---

### Multi-Tier Judicial Hierarchy & Live Indexed National Archives

This server performs live queries across the full judicial hierarchy and official legal archives of **Norway**, extracting full text from both HTML pages and official court/gazette PDF judgments:

| Judicial Tier | Covered Courts & Tribunals |
|:---|:---|
| **Tier 1 — First Instance** | 23 Tingretter (District Courts), Jordskifteretter (Land Consolidation Courts) & Forliksråd |
| **Tier 2 — Regional / Cantonal / Appellate** | 6 Lagmannsretter (Borgarting, Eidsivating, Agder, Gulating, Frostating, Hålogaland) |
| **Tier 3 — Supreme & Constitutional** | Norges Høyesterett (Supreme Court of Norway) & EFTA Court |

#### Official Portals & Live Indexed Domains

- **National Legislation & Official Gazette:** Lovdata API (api.lovdata.no) & Lovdata Open Legal Data (lovdata.no) — [https://api.lovdata.no/om-api-tjenesten/](https://api.lovdata.no/om-api-tjenesten/)
  - *Indexed Legislation Domains:* `lovdata.no`, `api.lovdata.no`, `stortinget.no`, `regjeringen.no`
- **Court Decisions & Jurisprudence Archives:** Lovdata Rettsavgjørelser (Høyesterett, Lagmannsrettene & Tingrettene — lovdata.no) — [https://lovdata.no](https://lovdata.no)
  - *Indexed Judicial & Open Case Law Domains:* `lovdata.no`, `domstol.no`

---

### Available MCP Tools

| Tool | Description |
|:---|:---|
| `search_legislation` | Searches enacted statutes, codes, decrees, and official gazette publications in Norway. |
| `search_case_law` | Searches national jurisprudence and open judicial archives for Norway. |
| `search_tiered_court_decisions` | Filters case law specifically by judicial instance (`first_instance`, `appellate_regional`, `supreme_constitutional`) or specific regional/cantonal/district court. |
| `list_court_hierarchy` | Returns the complete 3-tier court structure and supported regional court filters for Norway. |
| `get_legal_document_markdown` | Retrieves full statutory or judicial texts (both HTML and official `.pdf` court judgments) and converts them into clean Markdown. |
| `verify_citation` | Validates statutory and case law citations against official registries. |

---

<details>
<summary><b>Manual Configuration for Developers (Optional)</b></summary>

```json
{
  "mcpServers": {
    "no-legal-mcp": {
      "command": "uvx",
      "args": [
        "--from",
        "https://github.com/jurisatlas/no-legal-mcp/archive/refs/heads/main.zip",
        "no-legal-mcp"
      ]
    }
  }
}
```
</details>
