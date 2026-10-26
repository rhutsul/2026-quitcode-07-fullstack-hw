# Здача WS7

## Дані

- Роль: dev
- Команда: leave-portal
- GitHub-логін: rhutsul
- Ваше репо: https://github.com/rhutsul/leave-portal
- SHA: 19827f4c8e52e5e5d8d4c866089f0151a1c3938a
- Репо вимог PM: https://github.com/mkozlovskyi-ops/course-staff-management-spec
- Прод-URL: https://leave-portal-olive.vercel.app

## PM

—

## Розробник

- Рядок «Вимоги:» з `docs/conformance.md` на SHA: Вимоги: https://github.com/mkozlovskyi-ops/course-staff-management-spec · джерело: docs · знімок 2026-10-26
- PR «Оновлення вимог» зі зрізом 2 (A): — зріз 2 PM цього тижня не публікував: команда й PM перенесли його на WS8, а тиждень присвятили дизайн-системі. Останній знімок вимог (рішення PM https://github.com/mkozlovskyi-ops/course-staff-management-spec/issues/13 – https://github.com/mkozlovskyi-ops/course-staff-management-spec/issues/18 про вигляд) — https://github.com/rhutsul/leave-portal/pull/18
- PR «Оновлення вимог» після уточнень PM (A): https://github.com/rhutsul/leave-portal/pull/18 (знімок 2026-10-26)
- Питання в репо PM (A; щонайменше 2, з них щонайменше 1 — власне issue): — питання цього тижня стосувались лише вигляду, PM відповів на них у https://github.com/mkozlovskyi-ops/course-staff-management-spec/issues/13 … https://github.com/mkozlovskyi-ops/course-staff-management-spec/issues/18; чернетки питань до зрізу 2 (шкільний календар) чекають публікації вимог у WS8
- PR «Специфікація» з `add-<зріз2>` (A): — зріз 2 перенесено на WS8
- Дизайн-система — PR (B): https://github.com/rhutsul/leave-portal/pull/19 (токени, shadcn/ui, компоненти, `/design`), https://github.com/rhutsul/leave-portal/pull/20 і https://github.com/rhutsul/leave-portal/pull/21 (сторінки працівника), https://github.com/rhutsul/leave-portal/pull/22 (сторінки менеджера, `check:ui`, ADR 0004); доопрацювання: https://github.com/rhutsul/leave-portal/pull/27 (функції поруч із базою, скелетони у формі сторінок), https://github.com/rhutsul/leave-portal/pull/28 (лого, вибір теми, згортання бічної панелі, ADR 0005), https://github.com/rhutsul/leave-portal/pull/29 (панель вибору працівника й року в Balances), https://github.com/rhutsul/leave-portal/pull/30 (запис у Decisions — панель праворуч)
- Дизайн-система — `DESIGN.md` і джерело (B): https://github.com/rhutsul/leave-portal/blob/19827f4c8e52e5e5d8d4c866089f0151a1c3938a/DESIGN.md · джерело: артефакт Claude Design (Design System «Leave Portal» і полотно сторінок «Leave Portal screens»; приватні, посилання на них і промпт — в описі https://github.com/rhutsul/leave-portal/pull/19)
- Дизайн-система — прогін `architecture` на `main` (B): https://github.com/rhutsul/leave-portal/actions/runs/40401743436
- Знімки «до/після» (B): https://github.com/rhutsul/leave-portal/blob/19827f4c8e52e5e5d8d4c866089f0151a1c3938a/docs/img/ws7-before-requests-new-light.png, https://github.com/rhutsul/leave-portal/blob/19827f4c8e52e5e5d8d4c866089f0151a1c3938a/docs/img/ws7-after-requests-new-light.png (усі пари в обох темах — https://github.com/rhutsul/leave-portal/tree/19827f4c8e52e5e5d8d4c866089f0151a1c3938a/docs/img)
- Зміна `impl-<зріз2>` (C): — зріз 2 перенесено на WS8
- PR-и задач «Реалізація» (C; щонайменше 2): — зріз 2 перенесено на WS8 (права зрізу 1 — RLS, явні GRANT, перевірки в діях і тести відмов — реалізовано у WS6: https://github.com/rhutsul/leave-portal/pull/14, https://github.com/rhutsul/leave-portal/pull/16; цього тижня за рев'ю WS6 закрито право працівника змінювати своє ім'я — міграція з `revoke update (full_name)` і тест відмови в базі: https://github.com/rhutsul/leave-portal/pull/24; тест редиректу й спільна таблиця `dayShare`/`day_share`: https://github.com/rhutsul/leave-portal/pull/25)
- Мутаційна перевірка — червоні прогони (C; щонайменше 2): — зріз 2 перенесено на WS8
- ADR (D): https://github.com/rhutsul/leave-portal/blob/19827f4c8e52e5e5d8d4c866089f0151a1c3938a/docs/decisions/0004-design-system.md, https://github.com/rhutsul/leave-portal/blob/19827f4c8e52e5e5d8d4c866089f0151a1c3938a/docs/decisions/0005-theme-choice-and-collapsible-sidebar.md (вибір теми замість «лише за системою» з 0004)
- Архітектурне правило, крім `check:design` (D): job «Design system: ui components only» (`npm run check:ui`, `scripts/check-ui-primitives.mjs`) — https://github.com/rhutsul/leave-portal/pull/22; доказ, що ловить порушення: червоний прогін https://github.com/rhutsul/leave-portal/actions/runs/40376976868/job/121762584195 (draft-PR https://github.com/rhutsul/leave-portal/pull/26 з навмисним сирим `<button>`, закрито без злиття), тести https://github.com/rhutsul/leave-portal/blob/19827f4c8e52e5e5d8d4c866089f0151a1c3938a/tests/scripts/check-ui-primitives.test.ts
- Акаунти для PM (E): teacher1@example.test (працівник), teacher2@example.test (працівник), manager1@example.test (менеджер), manager2@example.test (менеджер), admin@example.test (адміністратор). Паролі — у зашифрованому `accounts.zip` (завантажити: https://github.com/rhutsul/leave-portal/raw/19827f4c8e52e5e5d8d4c866089f0151a1c3938a/accounts.zip; додано в https://github.com/rhutsul/leave-portal/pull/23), пароль до архіву — не тут
- Скріни за ролями (E): працівник — https://github.com/rhutsul/leave-portal/blob/19827f4c8e52e5e5d8d4c866089f0151a1c3938a/docs/img/ws7-after-requests-light.png; менеджер — https://github.com/rhutsul/leave-portal/blob/19827f4c8e52e5e5d8d4c866089f0151a1c3938a/docs/img/ws7-after-decisions-light.png; відмова в доступі — https://github.com/rhutsul/leave-portal/blob/19827f4c8e52e5e5d8d4c866089f0151a1c3938a/docs/img/ws7-after-decisions-denied-light.png
- AC зрізу 2 (E): — зріз 2 перенесено на WS8; AC зрізу 1 — 67 з 67 «реалізовано» в `docs/conformance.md`
- Відхилення від PM (E): не надходило

## Бонус

/design-артборд → реалізація. Спершу в Claude Design зібрано дизайн-систему й полотно всіх сторінок (вхід, Overview,
Balances, My requests, New request, Decisions), кілька раундів правок на полотні; потім кожну сторінку реалізовано за
ним і перевірено в браузері агента у світлій і темній темі — знімки «після» в `docs/img/` і в описах
https://github.com/rhutsul/leave-portal/pull/20, https://github.com/rhutsul/leave-portal/pull/21,
https://github.com/rhutsul/leave-portal/pull/22. Що знайшла перевірка й виправлено: вимкнений поточний крок форми
бліднув через `disabled:opacity-50`, день без годин перекривав день із записом у календарі, скелетон блимав на кожному
кліку рядка в Decisions (окремий `loading.tsx` прибрано). Висновок: полотно дає агенту конкретну ціль, а перевірка в
браузері ловить те, чого не видно в коді, — стани й теми.
