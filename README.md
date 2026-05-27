<div align="center">

# Jordan Ye

### Native Android Instrumentation · ARM64 Systems · Rust Tooling · AI Model Evaluation

[![Portfolio](https://img.shields.io/badge/Game_Runtime_Portfolio-111827?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Jordan231111/android-game-runtime-portfolio)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/jordan-ye-100b86237/)
[![GitHub](https://img.shields.io/badge/GitHub-Jordan231111-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Jordan231111)

</div>

## Focus

Computer Science + Mathematics student at RPI. Five years of independent Android
runtime-instrumentation work, plus active AI model-evaluation contract work through Handshake AI.

The center of gravity in my engineering is **below the editor layer**: ARM64 native code,
LSPosed/Xposed modules, IL2CPP metadata, `/proc/self/maps` parsing, pattern scanning, ELF symbol
resolution, page-permission-aware patching, and the verification scaffolding that keeps that work
honest.

## Featured Engineering

| Project | Stack | What it shows |
| --- | --- | --- |
| **[arm64-houdini-lsposed-framework](https://github.com/Jordan231111/arm64-houdini-lsposed-framework)** | C++ · Java · NDK · ARM64 | Self-contained ARM64 patching framework with no third-party inline-hook dependency. Implements the 16-byte `ldr x17, #8 / br x17 / <addr>` absolute-branch primitive, Houdini/native-bridge alias-aware writes (write every alias for the same file offset, not just the verified one), `/proc/self/maps` parser, IDA-style ARM64 signature scanner, file-backed code reads for verifier workflows, ELF symbol-table fallback when `dlsym` returns null. |
| **[lsposed-universal-template](https://github.com/Jordan231111/lsposed-universal-template)** | Java · Kotlin DSL · NDK · ShadowHook | Reusable LSPosed module scaffold on the modern `libxposed` API 101. `EngineDetector` classifies Unity / Unreal / Cocos2d-x / Godot / Flutter / React Native / Xamarin from native-lib-dir and `/proc/self/maps`. `FeatureRegistry` runtime flags with overlay UI bound per-feature. Debug/release split obfuscates everything except the LSPosed entry point. Configure script renames package, scope, metadata, and packaged `.so` name. |
| **[MalwareMinimizer](https://github.com/Jordan231111/MalwareMinimizer)** ★5 | Rust 2024 · CI/CD · `clap` · `proptest` · `criterion` | Cross-platform malware-scanning CLI. 321 commits, review-driven. CI matrix across Linux/macOS/Windows × x86_64/ARM64 with pinned action SHAs, `cargo audit`, `cargo deny`, `cargo supply-chain`, SBOM, and a crates.io-only dependency policy. Atomic database writes with rollback; quarantine-path validation with restrictive permissions; checksum-verified update artifacts published on a weekly schedule. Exit code `2` reserved so shells can tell "found malware" apart from "command failed." |
| **[BluestacksRoot](https://github.com/Jordan231111/BluestacksRoot)** ★64 | Batch · C++ · Python | One of the more widely used BlueStacks 5 rooting toolchains. Native Magisk component, semantic + dynamic integrity-check bypass in Python, GitHub Actions release pipeline. |
| **[mumu-magisk-1click](https://github.com/Jordan231111/mumu-magisk-1click)** ★39 | PowerShell · Batch | MuMu Player 12 root setup. 60KB PowerShell helper. Locates installs from the Windows uninstall registry, patches per-instance `customer_config.json` / `vm_config.json` / `shell_config.json` via real JSON parsing (not text replacement), writes `.bak` files before first mutation, supports `--dry-run` and `--edition global\|chinese\|all`. CI diffs the committed installer against MuMu's official download API and opens an update PR when it changes. |
| **[bluestacks-air-oneclick-root](https://github.com/Jordan231111/bluestacks-air-oneclick-root)** | Bash · macOS | BlueStacks Air on macOS. SIP-aware: separate code paths for SIP-enabled (manual copy) and SIP-disabled (fully automatic) systems. Patches `initrd_hvf.img` with Kitsune Magisk in a single curl-piped install. |

A private extended case study covering engine-neutral Cocos2d-x runtime hooks, Lua-load-boundary
inspection (`luaL_loadbuffer`), native `libapp.so` symbol research, and side-effect-preserving
simulation-speedup design is available on request.

## Broader Software Work

**[HackRPI 2025](https://github.com/Jordan231111/HackRPI-Website-2025)** — RPI's annual hackathon
site. Next.js, React, TypeScript, Tailwind, MongoDB, AWS Amplify, React Query, tRPC, Jest,
Playwright, GitHub Actions.

**[CommUnity](https://github.com/Jordan231111/CommUnity)** — Full-stack civic-tech app: HTML/CSS/JS
front-end, Firebase auth/db, Flask back-end, OpenAI API for AI-assisted outreach workflows.

## Stack

<p>
  <img src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white" />
  <img src="https://img.shields.io/badge/C-555555?style=flat-square&logo=c&logoColor=white" />
  <img src="https://img.shields.io/badge/Rust-000000?style=flat-square&logo=rust&logoColor=white" />
  <img src="https://img.shields.io/badge/Java-ED8B00?style=flat-square&logo=openjdk&logoColor=white" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" />
  <img src="https://img.shields.io/badge/PowerShell-5391FE?style=flat-square&logo=powershell&logoColor=white" />
  <br/>
  <img src="https://img.shields.io/badge/ARM64-111827?style=flat-square" />
  <img src="https://img.shields.io/badge/Android_NDK-3DDC84?style=flat-square&logo=android&logoColor=white" />
  <img src="https://img.shields.io/badge/Unity_IL2CPP-000000?style=flat-square&logo=unity&logoColor=white" />
  <img src="https://img.shields.io/badge/LSPosed/Xposed-6D28D9?style=flat-square" />
  <img src="https://img.shields.io/badge/Frida-EE3A8C?style=flat-square" />
  <img src="https://img.shields.io/badge/ShadowHook-1F6FEB?style=flat-square" />
  <br/>
  <img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black" />
  <img src="https://img.shields.io/badge/Next.js-000000?style=flat-square&logo=nextdotjs&logoColor=white" />
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white" />
  <img src="https://img.shields.io/badge/AWS_Amplify-FF9900?style=flat-square&logo=awsamplify&logoColor=white" />
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" />
</p>

## GitHub Snapshot

<div align="center">

![GitHub Stats](https://github-readme-stats-jordan231111.vercel.app/api?username=jordan231111&show_icons=true&theme=tokyonight&include_all_commits=true&count_private=true&v=3)
![Top Languages](https://github-readme-stats-jordan231111.vercel.app/api/top-langs/?username=jordan231111&layout=compact&theme=tokyonight&v=3)

</div>
