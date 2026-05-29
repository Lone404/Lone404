### Hi there,

I run **[Ryse](https://ryserp.com.br)** — a Brazilian roleplay server I built mostly from scratch: framework, inventory, phone, MDT, dispatch, housing, banking, jobs, payments. Server-authoritative everything; client owns visuals only.

#### What I work on

**Game server (Lua & TypeScript)**
- Custom framework (`ryse_core`) — `RcPlayer` metatable, vehicle/account classes, multichar, queue with realtime sync, Steam-link, donation benefits, statebags
- Defense-in-depth modules: `event_guard`, `statebag_guard`, `freeze_apply`, `ac_watchdog` — server trusts
- Custom inventory (slot-based + metadata, cases platform, typed stashes, crafts, clothing bridges)
- Custom phone with calls, videocall, messages, mail, photos, marketplace, crypto, wallet, integrated garages/houses/jobs
- Clean Architecture (infrastructure / services / repositories / presentation / callbacks)

**Web & integrations**
- Next.js 15 + React 19 + NextAuth 5 storefront, Discord OAuth, Supabase service-role kept server-side only
- Discord bot in `discord.js v14` driving role grant and payment reconciliation

**NUI**
- React & Svelte 5, standardized on Bun (Vite/esbuild bundles), Lottie integration, `ox_lib` callbacks for transport, focus discipline

#### Stack

- **Lua** (server-authoritative), **TypeScript** (Next.js 15, Svelte 5 :Runes, NUI React), **Node** (Discord bot)
- Tooling: `pnpm`, `bun`, Vite
