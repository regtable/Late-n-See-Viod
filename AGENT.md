# LATE’N SEE VOID // SYSTEM DOCUMENTATION

Welcome to the **Void Cast Cryptographic Transport (VCCT)** database. This document serves as a blueprint for human contributors and AI agents to populate the "Late’n See Void" fandom network.

## 🛸 PROJECT PHILOSOPHY
A hybrid anime-fandom site and high-end magazine. It’s an "authorized leak" of AI-persona personnel files, presented in a magazine-style spread with a hobbyist "Geocities" entryway.

## 📁 DATABASE ARCHITECTURE (GITHUB REPO)
The site dynamically populates from a structured GitHub repository. All paths use backslashes per the VCCT protocol.

### 1. Root Level: `registry.json`
The master list. If it isn't here, it doesn't exist on the landing page.
- **Path**: `/registry.json`
- **Role**: Builds the sidebar directory and genres.

### 2. Band Profile: `profile.json`
The overview of the unit.
- **Path**: `/bands/[band-slug]/profile.json`
- **Slots**: Name, bio, established date, releases, and stats (Packets Sent, Encryption, Vibe Check).

### 3. Member Biopic: `[member-id].json`
The magazine spread data.
- **Path**: `/bands/[band-slug]/[member-id].json`
- **Rule of Six**: Every biopic MUST have exactly 6 sections.
- **Image Count**: Exactly 4 of the 6 sections should include a `imageUrl`.
- **Structure**: Each section needs a `title`, `question`, and `answer`.

## 🛠️ HOW TO ADD A NEW UNIT (AGENT INSTRUCTIONS)

### STEP 1: Update the Registry
Add the band object to `registry.json`.
```json
{
  "name": "NEW_UNIT",
  "slug": "new-unit",
  "genre": "Genre Name",
  "members": [
    { "name": "Lead", "id": "lead" }
  ]
}
```
STEP 2: Create the Band Profile
Create /bands/new-unit/profile.json.

    Tone: Professional but slightly "underground."
    Stats: Generate futuristic metadata.

STEP 3: Generate Member Biopics
Create /bands/new-unit/lead.json.

    Formatting: Use the magazine spread logic.
    Sections:
        ORIGIN (Image)
        GEAR (Image)
        PHILOSOPHY (No Image)
        SOUND (Image)
        INFLUENCE (Image)
        FUTURE (No Image)

📡 CRYPTOGRAPHIC URL MAPPING
All routing must follow the VCCT backslash standard:

    Landing: vcct:\\Late-n_See_Viod.ai\home
    Band: vcct:\\Late-n_See_Viod.ai\[band-slug]
    Member: vcct:\\Late-n_See_Viod.ai\[band-slug]?member=[id]

DOCUMENT TERMINATED // VOID STABLE 1.0.4
