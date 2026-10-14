<h1 align="center">龙</h1>

```text
longtry@jxeqoz
──────────────────────────────────────────────
role     reverse engineer · game server dev · fullstack
main     lua · c# · c++ · typescript · rust
also     php · go · java · luau · python
engine   unity (c#)
infra    docker · compose · nginx
db       mysql · postgres · redis · mongo
runtime  bun, node when i have to
uptime   since 2021
now      rebuilding an mmo client in unity
```

### What I work on

#### Reverse engineering
Most of what I build starts with taking something apart.

- **Obfuscated Lua:** pulling custom bytecode VMs back apart into readable source.
- **Game protocols:** login, lobby and an ENet-based P2P relay for an old online shooter, rebuilt from packet captures. Opcode maps and packet layouts for several MMOs.
- **Asset formats:** proprietary map, character, animation and effect files from an old MMO engine, parsed and loaded into Unity.
- **Cheats and anti-cheat:** external memory read/write in Rust over WinAPI, DLL injection and native calls inside FiveM. On the defense side, a C++ scanner that does signature scanning, PE inspection, handle enumeration and overlay detection.
- **Client patching:** retargeting old game clients to private servers, plus the launchers and patchers that ship those patches.

#### Game servers
Emulators for older MMOs and shooters. Most of the job is reading packet captures until the protocol makes sense, then rebuilding the server in C# or C++. I also write the launcher and patcher in Rust + Tauri so updates actually reach players.

#### Unity
Porting a full MMO client off its old DirectX engine into Unity, in C#. Editor importers for the original maps, characters, animations, effects and sounds, then combat, quests, UI and a mobile build on top.

#### FiveM
Full resources from the Lua to the UI, plus the work that keeps a big server alive: getting resmon down, hunting memory leaks, fixing bugs and closing exploits. A server I work on has peaked at 2,048 players online.

Server-authoritative Lua 5.4 on ox_lib, NUIs in React, Svelte or Vue, MySQL and Redis behind it, and WebSockets when native events aren't enough.

#### Backend
APIs in Bun + Elysia or NestJS on Fastify. Dashboards in Next.js or Laravel + Inertia + Svelte. MySQL or Postgres through TypeORM, Redis for cache. Everything ships as Docker Compose stacks with nginx in front. I've also built payment integrations and Thai bank slip verification.

### Public repos

| | |
|---|---|
| [isle-admin](https://github.com/jxeqoz/isle-admin) | RCON, player database, whitelist, live map and proximity voice for The Isle: Evrima servers |
| [ws_lib](https://github.com/jxeqoz/ws_lib) | WebSockets for FiveM. One Lua API on client and server, Bun core underneath |
| [chatz](https://github.com/jxeqoz/chatz) | Self-hosted inbox for LINE OA. PHP 8.2, zero dependencies, one `docker compose up` |
| [fivem-mcp](https://github.com/jxeqoz/fivem-mcp) | Remote MCP server for FiveM dev: native lookup, manifest checks, code review |

<img src="https://skillicons.dev/icons?i=lua,cs,cpp,ts,rust,go,php,java,bun,nestjs,nextjs,react,svelte,vue,laravel,redis,mysql,postgres,mongodb,docker,nginx,tauri,unity&perline=12" />

<sub>Most of my work lives in private repos. If you want to see something, ask.</sub>
