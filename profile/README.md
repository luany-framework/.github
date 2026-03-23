# Luany

**AST-compiled PHP MVC framework with an explicit request lifecycle and zero-regex template engine.**

Designed with a compiler-first mindset, Luany focuses on predictable behavior, clean abstractions, and minimal overhead.

---

## Ecosystem

| Package | Description | Version |
|---------|-------------|---------|
| [luany/core](https://github.com/luany-ecosystem/luany-core) | HTTP Request/Response, Router, Middleware Pipeline | v1.0.0 |
| [luany/database](https://github.com/luany-ecosystem/luany-database) | PDO Connection, Query Builder, Active Record ORM, Migrations | v1.0.0 |
| [luany/framework](https://github.com/luany-ecosystem/luany-framework) | Application Container, Kernel, Service Providers, i18n | v1.0.0 |
| [luany/lte](https://github.com/luany-ecosystem/luany-lte) | AST-compiled template engine (`.lte` files) | v1.0.0 |
| [luany/cli](https://github.com/luany-ecosystem/luany-cli) | Command-line tool, scaffolding, migrations | v1.0.0 |
| [luany/luany](https://github.com/luany-ecosystem/luany) | Ready-to-use application skeleton | v1.0.0 |

### Tooling

- **[LTE for VS Code](https://github.com/luany-ecosystem/luany-lte-vscode)** — Syntax highlighting and tooling support for `.lte` template files.
- **[Benchmarks](https://github.com/luany-ecosystem/luany-benchmarks)** — Reproducible performance benchmarks and comparisons.

---

## Quick Start
```bash
# With Luany CLI (recommended)
composer global require luany/cli
luany new my-app
cd my-app

# Or directly via Composer
composer create-project luany/luany my-app
cd my-app

luany doctor
luany migrate
luany serve
```

---

## Architecture

```
Browser → public/index.php → bootstrap/app.php → Kernel::boot()
    → Kernel::handle(Request) → Pipeline → Middleware → Router → Controller → Response
```

### Dependency Graph

```
luany/luany (skeleton)
├── luany/framework
│   ├── luany/core
│   └── luany/lte
├── luany/database
└── luany/cli (dev)
```

---

## Documentation

[docs.luany.dev](https://docs.luany.dev) *(coming soon)*

---

## Philosophy

- Performance-first architecture with zero magic
- AST-driven templating — no regex parsing
- Explicit request lifecycle with clear middleware pipeline
- Clean MVC design built for simplicity and long-term scalability

---

## Origin

Built in Angola.
Engineered for the global PHP community.

---

**License**: MIT | **PHP**: >= 8.2 | **Author**: António Ambrósio Ngola
