# UNISEFE-PROJECT-AI
WEB PROJECT AI PORTAL

**Version:** `0.00000000.000000000.1 Alpha-`  
**Engine:** RIKI CORE `0.0.1 Alpha`  
**Format:** Single-file HTML application

**UNISEFE Project AI** is an experimental AI project builder designed around the principles of **RIKI CORE**. It combines project creation, AI-assisted editing, live preview, code inspection, history, testing and publishing inside a single standalone HTML file.

The application is intentionally minimal in infrastructure: no traditional database is required, no installation backend is required for the local DEMO workflow, and projects are represented through a canonical RIKI-style state based on permanent identities and dynamic values.

## Main idea

UNISEFE Project AI separates the product from its engine:

- **UNISEFE Project AI** — the application and user interface.
- **RIKI CORE** — the canonical state and validation model.
- **AI provider** — optional external intelligence used to propose valid project operations.

The core model follows four main concepts:

- **BYTE** — unique and permanent canonical identity.
- **VALORE / VALUE** — dynamic value associated with the same permanent BYTE.
- **CATENE / CHAINS** — permanent relations or equalities defined in the project Space.
- **BIT** — derived validity state; it is not an arbitrary value written by the AI.

## Current features

- Single HTML file.
- Projects view.
- Project workspace.
- ITALFABER-style fixed left navigation bar.
- Project tabs: **Chat**, **Preview**, **Code**, **History**, **Publish**.
- Local **DEMO** provider for zero-cost testing.
- **OpenAI** provider support.
- **OpenRouter** provider support.
- API keys kept outside the canonical RIKI project state.
- Live application preview.
- RIKI/code inspection.
- Project history/audit view.
- Standalone HTML publishing/export.
- Backup export and import.
- Built-in torture-test suite.
- Runtime validation of AI-generated operations.
- Protection against BYTE duplication and forbidden destructive operations.
- HTML/CSS sanitization for generated project output.

## Provider modes

### DEMO

The default provider is **DEMO**. It requires no API key, no network request and no paid service. It is intended to test the complete internal workflow:

`prompt → RIKI operations → validation → project state → preview → code → history → publish`

This makes it possible to test the application without spending API credit.

### OpenAI

OpenAI can be selected in Settings. The application is prepared to use the OpenAI Responses API and validates the returned operation payload before modifying the project.

For public deployments, do **not** hard-code a secret API key into the HTML. A public GitHub Pages deployment is client-side and cannot safely hide secrets.

### OpenRouter

OpenRouter is available as an alternative provider. The same rule applies: never publish a permanent secret key inside a public HTML file.

## RIKI CORE rules used by the builder

The current builder is intentionally stricter than the early experimental Portal versions.

### Permanent BYTE identity

Once a BYTE exists, its identity is not recreated, renamed or replaced as part of normal project evolution.

### Dynamic VALUE

The VALUE may change while the BYTE remains the same canonical identity.

### Permanent CHAINS

CHAINS are part of the project model, not a disposable action log. History is treated as technical audit information and is not used as a replacement canonical state.

### Derived BIT

BIT is computed from validation of connected CHAINS. The AI does not directly set BIT to `1` or `0` as a free operation.

## Safety and validation

AI output is treated as untrusted input.

The runtime checks proposed operations before applying them. Among other protections, the current build rejects or blocks:

- duplicate BYTE declarations;
- destructive BYTE replacement/deletion operations;
- direct arbitrary BIT assignment;
- forbidden CHAIN mutation patterns;
- unsafe expression forms;
- unsafe generated HTML attributes and executable markup.

The project also contains a built-in torture-test command in Settings so the internal rules can be checked without an external AI call.

## Publishing

A project can be exported as a standalone HTML application. The generated file contains the project output and runtime required by the exported application.

For GitHub Pages, the simplest deployment is:

1. Create a repository, for example `UNISEFE-PROJECT-AI`.
2. Rename the main application file to `index.html`.
3. Add this `README.md` and a license if desired.
4. Enable **GitHub Pages** from the `main` branch and repository root.

Suggested repository structure:

```text
UNISEFE-PROJECT-AI/
├── index.html
├── README.md
└── LICENSE
```

## Testing status

The current experimental build has been tested locally for the internal workflow, including:

- JavaScript syntax;
- BYTE permanence rules;
- CHAIN permanence checks;
- derived BIT behavior;
- duplicate/conflict rejection;
- hostile expression rejection;
- generated HTML safety checks;
- backup behavior;
- DEMO provider flow;
- project preview;
- code view;
- history view;
- publish/export flow;
- execution of an exported standalone HTML test application.

The only parts that cannot be fully verified without real external credentials and network access are the live third-party API responses themselves.

## Experimental status

`0.00000000.000000000.1 Alpha-` is intentionally an extremely early experimental release.

It should be treated as a research prototype, not as a stable production platform. The version number is deliberately ridiculous because the project is still at the beginning. :))))))))))))

## Philosophy

The project follows a simple direction:

> Reduce infrastructure before adding infrastructure.

Instead of starting from a large framework, database, backend and administration stack, UNISEFE Project AI tries to keep the project model, behavior and validation as small and explicit as possible.

The aim is not to imitate a traditional CMS or IDE. The aim is to explore whether an AI-assisted project environment can be built around a small canonical state model and still remain understandable, portable and publishable.

---

**UNISEFE Project AI**  
Powered by **RIKI CORE 0.0.1 Alpha**
