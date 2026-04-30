### Hi there,

I run **[Ryse](https://ryserp.com.br)** — a Brazilian roleplay server I built mostly from scratch: framework, inventory, phone, MDT, dispatch, housing, banking, jobs, payments. Server-authoritative everything; client owns visuals only.

#### What I work on

**Game server (Lua & TypeScript)**
- Custom framework (`ryse_core`) — `RcPlayer` metatable, vehicle/account classes, multichar, queue with realtime sync, Steam-link anti-multiaccount, donation benefits, statebags
- Defense-in-depth modules: `event_guard`, `statebag_guard`, `freeze_apply`, `ac_watchdog` — server trusts nothing the client says
- Custom inventory (slot-based + metadata, cases platform, typed stashes, crafts, clothing bridges)
- Custom phone with calls, videocall, messages, mail, photos, marketplace, crypto, wallet, integrated garages/houses/jobs
- Police MDT in Clean Architecture (infrastructure / services / repositories / presentation / callbacks) + Svelte 5 NUI with Tiptap, Leaflet, jsPDF, dnd-kit

**Web & integrations**
- Next.js 15 + React 19 + NextAuth 5 storefront, Discord OAuth, Supabase service-role kept server-side only
- Custom payment webhook handler — timing-safe secret compare, HMAC-SHA256 verify, timestamp replay protection, `devMode` guard in production, amount cross-check vs catalog, idempotent fulfillment via DB unique constraint
- Discord bot in `discord.js v14` driving role grant and payment reconciliation

**NUI**
- React & Svelte 5, standardized on Bun (Vite/esbuild bundles), Lottie integration, `ox_lib` callbacks for transport, focus discipline

#### Stack

- **Lua** (server-authoritative), **TypeScript** (Next.js 15, Svelte 5, NUI React), **Node** (Discord bot)
- **MySQL** via `oxmysql` (prepared statements on hot paths), **Supabase** for web/queue/payments
- `ox_lib`, `pma-voice`
- Tooling: `pnpm`, `bun`, Vite, ESLint, Biome, Playwright
