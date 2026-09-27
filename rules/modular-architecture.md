# 🏗️ Modular Architecture Protocol

> **Core Philosophy:** *Structure > Chaos | Simplicity > Complexity | Separation of Concerns*

## 1. Structure First, Code Second
Design the directory hierarchy and component boundaries **before** writing code. Writing code without an established architecture leads to sprawling god-files, circular dependencies, and high maintenance costs.

## 2. Domain-Driven Organization
Group code by **feature or domain** rather than flat technical layers:
```text
✅ GOOD (Domain-Driven):
src/
├── auth/
│   ├── auth.service.ts
│   ├── auth.controller.ts
│   └── auth.types.ts
└── billing/
    ├── billing.service.ts
    └── billing.types.ts

❌ BAD (Flat Technical Layers):
src/
├── controllers/
│   ├── auth.controller.ts
│   └── billing.controller.ts
└── services/
    ├── auth.service.ts
    └── billing.service.ts
```

## 3. Single Responsibility Principle (SRP)
- **One file = one clear responsibility.**
- If cognitive load increases or a file grows beyond a single cohesive concern, split it into modular subcomponents.
- Decouple pure business logic from UI rendering and transport layers.

## 4. Deep Hierarchies Over Flat Directory Spam
Prefer nested, logical structures over hundreds of files dumped into a single root folder. Clean folder nesting provides natural boundaries for module visibility, test scoping, and build packaging.

## 5. Descriptive & Typed Naming Conventions
- Avoid ambiguous names (`utils.ts`, `helpers.py`, `misc.js`).
- Use clear filenames with type or role suffixes:
  - `{feature}.service.ts`
  - `{feature}.controller.ts`
  - `{feature}.types.ts`
  - `test_{feature}.py`
