# BuySupply

[English README](README.en.md)

E-commerce платформа для офисной техники и расходных материалов на рынке Великобритании.

## Текущее состояние

Фактическая сверка: 2026-10-08. Базовая ветка: `main`. Source commit: `f6712315c84c4c38d3130abebb479642d5108e83`.

По текущему README и `package.json` подтверждены:
- Next.js 16 / React 19 / TypeScript;
- Supabase Postgres и Supabase Storage;
- Supabase Auth + iron-session для admin sessions;
- product management и image ordering;
- Netlify как текущий заявленный production path;
- manual Netlify build/deploy/smoke scripts.

## Локальный запуск

```bash
npm install
cp .env.example .env.local
npm run dev
```

## Проверки

```bash
npm run lint
npm run build
```

Netlify release-команды существуют в package.json, но не должны выполняться в рамках документационной задачи.

## Deployment docs

Перед любым deploy используйте:
- [NETLIFY_SETUP.md](NETLIFY_SETUP.md)
- [NETLIFY_HANDOFF.md](NETLIFY_HANDOFF.md)
- [PROJECT_TRANSFER.md](PROJECT_TRANSFER.md)

Датированные production-факты из handoff требуют свежей read-only проверки перед повторным утверждением.

## Управление проектом

GitHub Projects — единственный рабочий трекер. Конкретный Project в текущей сверке не подтверждён.

## Безопасность

Не публикуйте auth tokens, Supabase service keys, Netlify credentials, customer data или приватные enquiries.
