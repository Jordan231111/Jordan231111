<div align="center">

# Jordan Ye

### Native Android Instrumentation · ARM64 Systems · Rust Tooling · AI Model Evaluation

[![Portfolio](https://img.shields.io/badge/Game_Runtime_Portfolio-111827?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Jordan231111/android-game-runtime-portfolio)

</div>

## Focus

Computer Science + Mathematics student at RPI. Five years of independent Android
runtime-instrumentation work, plus active AI model-evaluation contract work through Handshake AI.

The center of gravity in my engineering is **below the editor layer**: ARM64 native code,
LSPosed/Xposed modules, IL2CPP metadata, `/proc/self/maps` parsing, pattern scanning, ELF symbol
resolution, page-permission-aware patching, and the verification scaffolding that keeps that work
honest.

---

## Flagship

<table>
<tr><td>

### **[ae-pcd-stamp-tracer — Case Study](https://github.com/Jordan231111/ae-pcd-stamp-tracer-public)**

`C++` · `Java` · `Lua` · `Python` · `NDK` · **~10K+ LOC · 5 years**

Engine-neutral runtime instrumentation for a Cocos2d-x / Lua native-heavy Android runtime. The
**applied layer** of a three-tier engineering trajectory: reusable template → ARM64/Houdini
specialization → target-specific application.

Case study covers **7 specific engineering problems with their solutions** — engine routing
without source, stable observation points over fixed RVAs, Houdini alias-aware patching, JNI
symbol-table stealth, fail-closed verification, side-effect-preserving fast iteration,
process-scope filtering — plus architecture lineage and system-flow diagrams.

Private repo; live walk-through available on request.

</td></tr>
</table>

---

## Native Instrumentation Foundations

<table>
<tr><td>

#### **[arm64-houdini-lsposed-framework](https://github.com/Jordan231111/arm64-houdini-lsposed-framework)**

`C++` · `Java` · `Android NDK` · `ARM64`

Self-contained ARM64 patching framework with **no third-party inline-hook dependency** — keeps
working on Houdini/native-bridge emulators where general libraries refuse to bind their ABI.

- Houdini/native-bridge alias-aware writes — every alias for the same file offset gets patched, not just the verified one
- 16-byte ARM64 absolute-branch primitive: `ldr x17, #8 / br x17 / <addr>`
- IDA-style ARM64 pattern scanner + manual ELF symbol-table fallback when `dlsym` returns null

</td></tr>
<tr><td>

#### **[lsposed-universal-template](https://github.com/Jordan231111/lsposed-universal-template)**

`Java` · `Kotlin DSL` · `NDK` · `ShadowHook`

Reusable LSPosed module scaffold on the modern **libxposed API 101**. Process scope defaults skip
push, crash, sandbox, and anti-cheat-satellite processes unless explicitly opted in.

- `EngineDetector` classifies Unity / Unreal / Cocos2d-x / Godot / Flutter / React Native / Xamarin via `nativeLibraryDir` + `/proc/self/maps`
- ShadowHook registered via `JNI_OnLoad` + `RegisterNatives` so the `.so` symbol table doesn't advertise package-derived JNI export names
- `configure-template.py` renames package, scope, metadata, and packaged `.so` in one command

</td></tr>
<tr><td>

#### **[Archero-LSPOSED-Mod](https://github.com/Jordan231111/Archero-LSPOSED-Mod)**

`C++` · `Java` · `Android NDK` · `Unity IL2CPP`

Applied Unity IL2CPP runtime-hook study against a live `arm64-v8a` target — the IL2CPP counterpart
to the Cocos2d-x case study above.

- Metadata-driven method/field resolution against `libil2cpp.so` with fail-closed install (no blind RVA patching)
- Side-aware logic in the IL2CPP managed-type system
- Authorized testing on owned devices only

</td></tr>
</table>

---

## Rust Systems

<table>
<tr><td>

#### **[MalwareMinimizer ★5](https://github.com/Jordan231111/MalwareMinimizer)**

`Rust 2024` · `clap` · `proptest` · `criterion` · `wiremock`

**RCOS Project Lead of a 5-person team** at Rensselaer Center for Open Source — Spring 2026 MVP,
presented at the RCOS Spring 2026 showcase. 321 commits, 139 PRs, 110 issues — issue-driven team
ownership, not a one-off demo.

- Cross-platform CI matrix: Linux / macOS / Windows × x86_64 / ARM64 with pinned action SHAs
- Supply-chain: `cargo audit` + `cargo deny` + `cargo supply-chain` + SBOM, crates.io-only policy
- 174 automated tests; atomic DB writes with rollback; exit code `2` reserved for "found malware"
- Auto-graded starter-task track for onboarding new Rust contributors

</td></tr>
</table>

---

## Emulator and Device Tooling

<table>
<tr><td>

#### **[BluestacksRoot ★64](https://github.com/Jordan231111/BluestacksRoot)** — `Batch` · `C++` · `Python`

Widely used BlueStacks 5 rooting toolchain. Native Magisk component, semantic + dynamic
integrity-check bypass in Python, full CI release pipeline.

</td></tr>
<tr><td>

#### **[mumu-magisk-1click ★39](https://github.com/Jordan231111/mumu-magisk-1click)** — `PowerShell` · `Batch`

MuMu Player 12 root setup. Locates installs via the Windows uninstall registry, patches per-instance
config JSON with real parsing (not text replacement), writes `.bak` files before mutation, supports
`--dry-run`. CI diffs the bundled installer against MuMu's official download API.

</td></tr>
<tr><td>

#### **[bluestacks-air-oneclick-root](https://github.com/Jordan231111/bluestacks-air-oneclick-root)** — `Bash` · `macOS`

BlueStacks Air on macOS. **SIP-aware** — separate code paths for SIP-enabled and SIP-disabled
systems. Single curl-piped installer.

</td></tr>
</table>

---

## Leadership

**RCOS Project Lead — MalwareMinimizer** *(Spring 2026)* · Rensselaer Center for Open Source
- Led a 5-person team (plus 3 external contributors) to a demoable Spring 2026 MVP.
- Owned architecture, CI/CD, and database/update workflow; partners covered scanner/quarantine, CLI, utilities, and setup/docs.
- Built auto-graded onboarding tasks for new Rust contributors; `validate_strict.sh` + CODEOWNERS keep the review bar high.
- Presented at the RCOS Spring 2026 showcase.

**Junior Director of Technology — HackRPI** *(Oct 2024 – Present)*
- Drive the technical roadmap for **[HackRPI.com](https://github.com/Jordan231111/HackRPI-Website-2025)** (Next.js 14, React 18, TypeScript, MongoDB, AWS Amplify, Jest, Playwright) — 500+ event participants.
- Lead 3+ project leads and 20+ organizers via status check-ins and PR code reviews.

---

## Certifications

**AWS Certified Cloud Practitioner** — Issued Jul 2023, valid through Jul 2026

---

## Stack

<p>
  <img src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white" />
  <img src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white" />
  <img src="https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Lua-2C2D72?style=flat-square&logo=lua&logoColor=white" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" />
  <br/>
  <img src="https://img.shields.io/badge/ARM64-111827?style=flat-square" />
  <img src="https://img.shields.io/badge/Android_NDK-3DDC84?style=flat-square&logo=android&logoColor=white" />
  <img src="https://img.shields.io/badge/Unity_IL2CPP-000000?style=flat-square&logo=unity&logoColor=white" />
  <img src="https://img.shields.io/badge/LSPosed/Xposed-6D28D9?style=flat-square" />
  <img src="https://img.shields.io/badge/Frida-EE3A8C?style=flat-square" />
  <br/>
  <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black" />
  <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white" />
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" />
</p>

---

## GitHub Snapshot

<div align="center">

![GitHub Stats](https://github-readme-stats-jordan231111.vercel.app/api?username=jordan231111&show_icons=true&theme=tokyonight&include_all_commits=true&count_private=true&v=3)
![Top Languages](https://github-readme-stats-jordan231111.vercel.app/api/top-langs/?username=jordan231111&layout=compact&theme=tokyonight&v=3)

</div>

---

## Contact

- **Email** — yejordan8888@gmail.com
- **LinkedIn** — [jordan-ye-100b86237](https://www.linkedin.com/in/jordan-ye-100b86237/)
