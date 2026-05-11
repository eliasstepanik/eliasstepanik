## Hi, I'm Elias.

I build infrastructure for AI agents, graphics engines in Rust, and tools that bridge hardware and software. Developer at Volkswagen, based in Wolfsburg, Germany.

---

### What I do

I work across the stack â€” from GPU-accelerated path tracing and real-time fluid simulation to semantic memory systems for LLM agents. My work is driven by a conviction that the most interesting problems live at the boundaries: between hardware and software, between graphics and simulation, between AI and structured tooling.

I started in C# and Java (2018â€“2022), building desktop applications, audio hardware integrations, and graphics simulations. A deep dive into Rust began in 2023 and has since become my primary language â€” it now powers everything from WebGPU engines to MCP servers to CLI tooling.

---

### Current focus

**AI agent infrastructure** â€” building the memory and task management layer that lets LLM agents operate with persistence, context, and structure. My MCP servers provide semantic retrieval and hierarchical task orchestration for agentic workflows.

**Self-hosted agentic CI** â€” [`odev`](https://github.com/eliasstepanik/odev) is a self-hosted runner that boots isolated Docker containers per task, streams a live opencode TUI over WebSocket, and surfaces diffs, file trees, and per-repo workspaces in a Leptos dashboard.

**Graphics & simulation in Rust** â€” a WebGPU engine with ECS-based scripting, a physically-based path tracer with Blender integration, and voxel terrain streaming at scale.

---

### Key projects

**AI / LLM Infrastructure**
- [`odev`](https://github.com/eliasstepanik/odev) (private) â€” Self-hosted agentic CI runner: isolated Docker sessions per task, live opencode TUI streamed via WebSocket, syntect-highlighted diff viewer, file browser, per-repo memory & task workspaces. Rust + axum 0.8 + Leptos 0.7 (SSR+WASM) + bollard 0.18. Single binary via cargo-leptos, deployed via Docker Compose at `ghcr.io/eliasstepanik/odev-server:latest`.
- [`memory-mcp-server`](https://github.com/eliasstepanik/memory-mcp-server) â€” Semantic memory for AI agents: hybrid FTS5 + vector retrieval, multi-provider embeddings (Voyage, OpenAI, Cohere, Ollama), temporal decay, cross-encoder reranking. Multi-arch Docker builds (amd64/arm64) â†’ GHCR.
- [`task-mcp-server`](https://github.com/eliasstepanik/task-mcp-server) â€” Hierarchical task management with semantic search, importance scoring, and full CRUD for agentic workflows. Multi-arch Docker builds (amd64/arm64) â†’ GHCR.
- [`Audiobook-Generator`](https://github.com/eliasstepanik/Audiobook-Generator) â€” LLM-powered multi-speaker audiobook pipeline using Qwen3 + TTS. 3-variant Docker builds (CUDA / CPU / ROCm) â†’ GHCR.

**Graphics & Game Dev (Rust)**

<table>
<tr>
<td width="50%">

**[`webgpu-engine`](https://github.com/eliasstepanik/webgpu-engine)** â€” Modern 3D engine in Rust/WebGPU with ECS architecture and embedded scripting

</td>
<td width="50%">
<img src="https://raw.githubusercontent.com/eliasstepanik/webgpu-engine/master/screenshot.png" width="100%" />
</td>
</tr>
<tr>
<td width="50%">

**[`Pathtracer`](https://github.com/eliasstepanik/Pathtracer)** â€” Physically-based path tracer, CPU + GPU, with Blender scene integration

</td>
<td width="50%">
<img src="https://raw.githubusercontent.com/eliasstepanik/Pathtracer/master/render_7680x4320_s131072_ap0.02_f10.0_tzW1Af.png" width="100%" />
</td>
</tr>
<tr>
<td width="50%">

**[`voxel-simulation`](https://github.com/eliasstepanik/voxel-simulation)** â€” Streaming voxel terrain engine in Bevy using big-space coordinates

</td>
<td width="50%">
<img src="https://raw.githubusercontent.com/eliasstepanik/voxel-simulation/master/images/voxel-simulation-demo.png" width="100%" />
</td>
</tr>
</table>

**Astronomy Automation**
- [`n8n-nodes-ninaapi`](https://github.com/eliasstepanik/n8n-nodes-ninaapi) â€” n8n workflow nodes for N.I.N.A. astronomy software: cameras, mounts, domes, focusers, polar alignment

**Infrastructure & DevOps**
- [`IonosDDNSUpdater`](https://github.com/eliasstepanik/IonosDDNSUpdater) â€” Dockerized dynamic DNS updater for Ionos API. Dev/prod branch pipelines + .NET 6 build+test suite.
- [`AutoProxy`](https://github.com/eliasstepanik/AutoProxy) â€” Automated proxy management infrastructure

**CI/CD**
- [`memory-mcp-server`](https://github.com/eliasstepanik/memory-mcp-server) + [`task-mcp-server`](https://github.com/eliasstepanik/task-mcp-server) â€” Multi-arch Docker builds (amd64/arm64) pushed to GHCR on every push to main
- [`Audiobook-Generator`](https://github.com/eliasstepanik/Audiobook-Generator) â€” 3-variant Docker images (CUDA / CPU / ROCm) built and published to GHCR
- [`IonosDDNSUpdater`](https://github.com/eliasstepanik/IonosDDNSUpdater) â€” Separate dev/prod branch pipelines with .NET 6 build, test, and publish
- [`bevy-project-template`](https://github.com/eliasstepanik/bevy-project-template) â€” Full CI/CD suite: dependency audit, continuous integration, continuous deployment
- Several others: ClusterManager, strudel-docker, WorldOfPadman_Dedi_Server, zmk-config, webgpu-engine

**Audio & Hardware**

<table>
<tr>
<td width="50%">

**[`VoicemeeterSliderControlCSharp`](https://github.com/eliasstepanik/VoicemeeterSliderControlCSharp)** â€” Arduino + C# hardware controller for Voicemeeter audio mixer (?5)

</td>
<td width="50%">
<img src="https://raw.githubusercontent.com/eliasstepanik/VoicemeeterSliderControlCSharp/master/3vm.jpg" width="100%" />
</td>
</tr>
</table>

---

### Infrastructure & Self-Hosted

Running on a self-managed homelab:

**AI / LLM services** â€” Ollama (local LLM inference), meridian (Claude proxy), audiobook-generator, qwen3-tts

**MCP infrastructure** â€” portainer-mcp, memory-mcp, task-mcp (custom MCP servers for AI agent tooling)

**Data layer** â€” Qdrant (vector database), SpacetimeDB, OpenCloud

**Workflow automation** â€” n8n

**Networking** â€” Headscale (WireGuard mesh), Tailscale agent, Caddy reverse proxy

**Monitoring** â€” Beszel, Watchtower, Skyserver

**Game servers** â€” Factorio, Terraria, Satisfactory, Project Zomboid, Enshrouded, Abiotic Factor

**Personal infra** â€” Syncthing, Protonmail Bridge, Pterodactyl

**Astronomy** â€” nova (DSO tracker)

---

### Tech stack

![Rust](https://img.shields.io/badge/Rust-000000?style=for-the-badge&logo=rust&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![C#](https://img.shields.io/badge/C%23-239120?style=for-the-badge&logo=csharp&logoColor=white)
![WebGPU](https://img.shields.io/badge/WebGPU-005A9C?style=for-the-badge&logo=webgpu&logoColor=white)
![Bevy](https://img.shields.io/badge/Bevy-232326?style=for-the-badge&logo=bevy&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![n8n](https://img.shields.io/badge/n8n-EA4B71?style=for-the-badge&logo=n8n&logoColor=white)
![Leptos](https://img.shields.io/badge/Leptos-EF3939?style=for-the-badge&logo=rust&logoColor=white)
![Axum](https://img.shields.io/badge/Axum-000000?style=for-the-badge&logo=rust&logoColor=white)
![Qdrant](https://img.shields.io/badge/Qdrant-000000?style=for-the-badge&logo=qdrant&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=for-the-badge&logo=ollama&logoColor=white)

---

<p align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=eliasstepanik&show_icons=true&theme=dark&hide_border=true&bg_color=0d1117&icon_color=58a6ff&text_color=c9d1d9&title_color=58a6ff&count_private=true&include_all_commits=true" alt="GitHub Stats" height="165" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=eliasstepanik&layout=compact&theme=dark&hide_border=true&bg_color=0d1117&text_color=c9d1d9&title_color=58a6ff&count_private=true" alt="Top Languages" height="165" />
</p>
<p align="center">
  <img src="https://streak-stats.demolab.com?user=eliasstepanik&theme=dark&hide_border=true&background=0d1117&stroke=58a6ff&ring=58a6ff&fire=58a6ff&currStreakLabel=58a6ff" alt="GitHub Streak" />
</p>

---

*[sailehd.de](https://sailehd.de)*