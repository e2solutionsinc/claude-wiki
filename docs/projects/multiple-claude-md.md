# Managing Multiple CLAUDE.md Files

If you work across multiple customers or databases, you need each one to have its own isolated context. Claude Code loads `CLAUDE.md` based on the directory you start it from — and inherits from every parent folder up to your home directory. The structure below takes advantage of that to share global conventions while keeping each database isolated.

---

## Directory structure

```
~/sql/
├── CLAUDE.md                        ← global conventions (applies to all sessions)
├── eplus/
│   ├── aad/
│   │   └── CLAUDE.md               ← ePlus AAD schema and environment
│   └── wms/
│       └── CLAUDE.md               ← ePlus WMS schema and environment
├── customer2/
│   └── prod/
│       └── CLAUDE.md               ← Customer 2 production schema
└── customer3/
    └── dev/
        └── CLAUDE.md               ← Customer 3 dev schema
```

When you start Claude Code from `~/sql/eplus/aad/`, it loads that folder's `CLAUDE.md` **plus** `~/sql/CLAUDE.md`. Starting from `~/sql/customer2/prod/` loads that one plus the global. No context bleed between customers or environments.

---

## Setting up a new customer/environment

```bash
mkdir -p ~/sql/customer-name/environment
cd ~/sql/customer-name/environment
claude
```

Then follow the [Creating a CLAUDE.md](creating-claude-md.md) process from inside that directory. Each environment gets its own `CLAUDE.md` built from that customer's schema export.

---

## What goes where

| File | Loads when | Use for |
|---|---|---|
| `~/sql/CLAUDE.md` | Every session started under `~/sql/` | Global SQL conventions — formatting rules, `usp_` prefix, `SET NOCOUNT ON`, etc. |
| `~/sql/eplus/aad/CLAUDE.md` | Sessions started from that folder | ePlus AAD schema, table definitions, environment-specific notes |
| `~/sql/customer2/prod/CLAUDE.md` | Sessions started from that folder | Customer 2 production schema, conventions, environment |

Keep schema and customer-specific context in the environment-level `CLAUDE.md`. Put conventions that apply to all your SQL work in `~/sql/CLAUDE.md`.
