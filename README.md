# Evimiz · Presentación · LATAM

Репозиторий со всеми презентациями, маркетинговыми материалами и внутренними документами по выводу платформы **Evimiz** (smart-intercom + cameras + cloud) на рынок Латинской Америки (фокус — Аргентина).

> **Live-версия:** https://sputnik-systems.github.io/presentacion-latam/
> **Аудитория:** девелоперы / интеграторы / property managers / CTO / sales-команда AR.
> **Языки:** EN + ES (большинство decks билингвальные).

---

## Как читать этот документ

Раздел [Текущие версии (рекомендуется к показу)](#текущие-версии-рекомендуется-к-показу) — это то, что реально нужно отдавать клиентам **сейчас**. Остальное (`v1`, `v2`, `v3`) оставлено в репозитории для истории и быстрого отката, но активно не поддерживается.

В конце документа — [Changelog](#changelog) и [Протокол обновления README](#протокол-обновления-readme).

---

## Содержание

1. [Структура проекта](#структура-проекта)
2. [Текущие версии (рекомендуется к показу)](#текущие-версии-рекомендуется-к-показу)
3. [Все презентации (.html) — по семействам](#все-презентации-html--по-семействам)
   - [Hub — навигация](#hub--навигация)
   - [Developers — для девелоперов](#developers--для-девелоперов-недвижимости)
   - [Integrators — для интеграторов CCTV](#integrators--для-интеграторов-cctv)
   - [Admins — для property managers](#admins--для-property-managers-управляющих)
   - [GEO Platform — для портфеля зданий / CTO](#geo-platform--для-портфеля-зданий--cto)
   - [Hardware & Pricing — оборудование и цены](#hardware--pricing--оборудование-и-цены)
   - [App Demo — демо мобильного приложения](#app-demo--демо-мобильного-приложения)
   - [Product Tour / Platform Demo — обзор платформы](#product-tour--platform-demo--обзор-платформы)
   - [Smart Intercom — обзорные пакеты](#smart-intercom--обзорные-пакеты)
   - [PPTX](#pptx)
4. [Внутренние документы (.docx)](#внутренние-документы-docx)
5. [Папка assets/](#папка-assets)
6. [Известные проблемы / открытые вопросы](#известные-проблемы--открытые-вопросы)
7. [Changelog](#changelog)
8. [Протокол обновления README](#протокол-обновления-readme)

---

## Структура проекта

```
Presentación/
├── README.md                         ← этот файл
├── *.html                            ← 28 HTML-презентаций (см. ниже)
├── *.pptx                            ← 1 PowerPoint
├── *.docx                            ← внутренние документы (untracked, не в git)
├── *.png                             ← ассеты-скриншоты для referencé (en/es)
├── assets/                           ← все изображения, иконки, скриншоты
└── .git/                             ← репозиторий (origin: sputnik-systems/presentacion-latam)
```

Развёртывание: GitHub Pages обслуживает корень `main` ветки. Любой `.html` в корне доступен по `https://sputnik-systems.github.io/presentacion-latam/<filename>.html`.

---

## Текущие версии (рекомендуется к показу)

| Аудитория | Файл | Статус |
|---|---|---|
| Точка входа / навигация | `Evimiz-Hub-v2.html` | актуальный |
| Real-estate developers | `Evimiz-Developers-v4.html` | актуальный |
| CCTV integrators | `Evimiz-Integrators-v4.html` | актуальный |
| Property managers | `Evimiz-Admins-v4.html` | актуальный |
| CTO / portfolio / GEO | `Evimiz-GEO-Platform-v3.html` | актуальный |
| Hardware & pricing | `Evimiz-Hardware-and-Pricing-v2.html` | актуальный (retail-цены) |
| Демо мобильного приложения | `Evimiz-App-Demo-v2.html` | актуальный |
| Обзор платформы (16 экранов) | `Evimiz-Product-Tour-v2.html` | актуальный |

Все актуальные версии используют единый design-system (v4 / SVG-иконки, methodology-секция, цена $2.50, retail-математика без раскрытия внутренней механики +5%).

---

## Все презентации (.html) — по семействам

### Hub — навигация

#### `Evimiz-Hub-v2.html` — **актуальный**
Главная посадочная страница пакета. Один экран: «Turn Buildings Into Revenue-Generating Digital Assets» + три карточки-входа в decks по аудиториям:
- 01 — For Real Estate Developers (`Developers-v3`)
- 02 — For CCTV Integrators (`Integrators-v3`)
- 03 — For Property Managers (`Admins-v3`)

> ⚠️ Hub-v2 пока ссылается на `v3`-версии аудиторий. При следующем обновлении нужно перевязать на `v4`. См. [Известные проблемы](#известные-проблемы--открытые-вопросы).

#### `Evimiz-Hub.html` — устарел
Первая версия Hub-страницы. Та же структура, без обновлённых SVG-иконок и methodology.

---

### Developers — для девелоперов недвижимости

Все версии — один и тот же сюжет: «Smart Building = Premium Price». Эволюция была преимущественно в дизайне и плотности контента.

#### `Evimiz-Developers-v4.html` — **актуальный**
Структура (11 слайдов):
- Hero: «Sell Faster. Charge More.»
- Buyers Expect Smart Buildings (4 проблемы: устаревшие системы, ценовые уступки, нет mobile, простой инвентарь)
- Smart Building = Premium Price
- The Numbers That Matter (метрики)
- Stack Buildings. Stack Revenue. (масштабирование портфеля)
- Traditional Intercom vs Smart Access (сравнение)
- Your Brand. Your App. (white-label)
- Ready Before Handover (Cloud Platform · Hardware Ready · Weeks not Months · Spanish-First for LatAm)
- Proven at Scale
- Long-Term Value Beyond the Sale
- CTA: «Ready to Build Premium?»

Дизайн v4: SVG-иконки, methodology-секция, $2.50 pricing-anchor.

#### `Evimiz-Developers-v3.html` — устарел
v3: добавлен слайд «Stack Buildings. Stack Revenue.», добавлена 4-я проблема в hero. Без SVG-иконок v4.

#### `Evimiz-Developers-v2.html` — устарел
Переходная версия. Структура близка к v3, но без слайда «Stack Revenue».

#### `Evimiz-Developers.html` — устарел
Первая версия. Короче (10 слайдов), нет «The Numbers That Matter», нет «Stack Revenue».

---

### Integrators — для интеграторов CCTV

Сюжет: «Build a $10K/Month Install Business» (recurring revenue из каждой установки).

#### `Evimiz-Integrators-v4.html` — **актуальный**
Структура (11 слайдов):
- Hero: «Build a $10K/Month Install Business»
- The One-Time Payment Trap (3 проблемы: клиенты забывают, маржа падает, всегда в поиске)
- Build Predictable Monthly Revenue
- Each Building Is a Long-Term Asset
- Old Model vs Evimiz Model
- You Install. We Handle Everything Else. (no servers, no support, no dev)
- Your Brand. Their Loyalty to You. (white-label)
- Your Best Clients Are Already Yours
- Plug & Play. No Servers.
- Cameras + Access + App = 3× the Deal
- Methodology footer + CTA

#### `Evimiz-Integrators-v3.html` — устарел
v3: hero ещё «$10K/Month», но без SVG-иконок и methodology.

#### `Evimiz-Integrators-v2.html` — устарел
Hero: «Turn Every Install Into Monthly Revenue». Промежуточная версия.

#### `Evimiz-Integrators.html` — устарел
Первая версия. Hero «Turn Every Install Into Monthly Revenue». Меньше слайдов.

---

### Admins — для property managers (управляющих)

Сюжет: «Run Your Building Without the Headaches» — операционное облегчение.

#### `Evimiz-Admins-v4.html` — **актуальный**
Структура (11 слайдов):
- Hero: «Run Your Building Without the Headaches»
- Daily Building Management Is Inefficient and Stressful (lost keys / resident complaints / always on-site)
- Every Visit Is Recorded — No More Disputes (полный access log)
- Open Doors Without Being There (remote unlock, digital guest passes, push, resident app)
- Your Day. Before and After Evimiz.
- What This Saves You Every Month
- Better Service. More Buildings.
- 24/7 Video. Full Archive.
- Residents Use It Daily Without Training
- Upgrade Your Building Without Replacing Existing Systems
- Methodology footer + CTA

#### `Evimiz-Admins-v3.html` — устарел
v3: добавлен «What This Saves You Every Month», но без SVG-иконок.

#### `Evimiz-Admins-v2.html` — устарел
Промежуточная версия. Без слайда «What This Saves».

#### `Evimiz-Admins.html` — устарел
Первая версия. «Daily Building Management Is Broken». Меньше слайдов.

---

### GEO Platform — для портфеля зданий / CTO

Самый «стратегический» deck. Для CTO, владельцев портфеля, операционных директоров.

#### `Evimiz-GEO-Platform-v3.html` — **актуальный**
Полностью переделан под CTO/portfolio audience с sales-ammo (конкретные ROI, цифры). Структура (11 слайдов):
- Hero: «Control & Monitoring for your entire building portfolio»
- Operations teams drown in routine tasks (lost keys, no portfolio visibility, endless calls)
- Remote control over every door, every camera
- Direct channel to every resident — and your ops team
- Real-time dashboard across every building
- Product model: Core free, Premium pays
- From daily usage to recurring revenue
- Real ROI numbers from operating portfolios
- Portfolio math: numbers that compound
- 15-minute setup, certified partners, zero downtime
- Methodology footer + CTA «Ready to scale your portfolio without scaling headcount?»

#### `Evimiz-GEO-Platform-v2.html` — устарел (но интересный)
**Adaptive presentation** с сегментацией. Работает как сторителлинг: «Buildings are no longer physical → They are digital products → Monetization layer». Hero-слайды + контрастные WITHOUT/WITH панели. EN + ES в одном файле.

#### `Evimiz-GEO-Platform.html` — устарел
Product overview, билингвальный (EN/ES в одном экране). 17 слайдов: dashboard, locations, building details, access, branding, monetization, call diagnostics, 6-step setup. CTA — «Join 1,000+ buildings on Evimiz GEO».

---

### Hardware & Pricing — оборудование и цены

#### `Evimiz-Hardware-and-Pricing-v2.html` — **актуальный**
20 слайдов с реальными ценами и позиционированием. Структура:
- Hero: «Digital infrastructure for modern buildings»
- From legacy hardware to a connected stack (Closed/manual/offline → Open/mobile/real-time)
- A doorbell with a platform
- 6 серий камер по парам:
  - Basic & Dual Light
  - ZOOM & Strobe
  - PTZ & Motorized IR
- Every device, built to work as one
- Hardware + software, in real time
- Built for reliability and scale
- **Reference prices — from** (slide 11) — retail-цены: $45 / $130 / $135 / $210 / $330 / $510. ~50% дешевле Hikvision/Dahua. Никакой внутренней механики +5% / wholesale на этом слайде нет — она в internal docs.
- **Factory-direct, not cheap** (slide 12) — quality positioning, цепочка «Factory → direct sales → partner»
- Designed for modern projects
- Кросс-линки на `Developers-v4`, `Admins-v4`, `Integrators-v4`, `GEO-Platform-v3`
- Контакт: `demo@evimiz.ai`

> Последний значимый коммит (`5236831`, 6 мая 2026): заменили wholesale-математику на retail-цены — prospect-facing слайд больше не показывает внутренние +5% AR commission.

#### `Evimiz-Hardware-and-Pricing-v1.html` — устарел
v1: первая версия с wholesale-ценами на слайде. Заменена через v2 после решения скрыть internal pricing-mechanics.

#### `Evimiz-Hardware-v3.html` — устарел
Hardware-only deck (без pricing). Билингвальный, единая структура с парами серий. ~15 слайдов.

#### `Evimiz-Hardware-v2.html` — устарел
Hardware-only. 11 слайдов. Базовая версия с ecosystem-слайдом и «Built for reliability and scale».

#### `Evimiz-Hardware.html` — устарел
Первая версия. Hero «Smart security for your building». 10 слайдов.

---

### App Demo — демо мобильного приложения

Презентации в формате «слайды-как-телефон»: каждый экран = функция приложения.

#### `Evimiz-App-Demo-v2.html` — **актуальный**
16 слайдов в формате карусели, дизайн-токены v4. Сюжет:
- Everything in one app
- Someone is at your door
- Not at home? No problem.
- Open the door in one tap
- See what's happening in real time
- Go back in time when needed
- Give access in seconds
- Keep everyone connected
- Everything is tracked
- One unified platform for the whole building team

#### `Evimiz-App-Demo.html` — устарел
Первая версия с EN + ES в одном файле (двойной набор слайдов).

---

### Product Tour / Platform Demo — обзор платформы

#### `Evimiz-Product-Tour-v2.html` — **актуальный**
Переименование `Platform-Demo` после ребрендинга. 16 экранов веб-платформы:
- Everything is managed in one platform
- A complete view of your property
- Control who can enter
- See everything live
- Track every action
- Manage all devices remotely
- Operate the system in real time
- Manage multiple buildings in one place
- Connect with your existing systems
- One unified platform for your whole team
- Let's talk (CTA)

Каждый слайд содержит крупный скриншот веб-интерфейса в browser-фрейме.

#### `Evimiz-Platform-Demo.html` — устарел
Первая версия (билингвальная, EN + ES экраны подряд).

---

### Smart Intercom — обзорные пакеты

Старые «обзорные» презентации до раскола на per-audience decks. Хороши как «всё в одной».

#### `Evimiz-Smart-Intercom.html` — устарел, но используется как референс
EN-версия. Структура: The Problem · Evimiz Ecosystem (Cloud + App + Equipment) · Smart Intercom · IZI CCTV Cameras · Platform + White Label · SDK / API Integration · Grow Your User Base · Keyless Access.

#### `Evimiz-Intercomunicador-Inteligente.html` — устарел
ES-зеркало `Evimiz-Smart-Intercom.html`. Та же структура на испанском.

---

### PPTX

#### `Evimiz-Hub-Presentation.pptx`
PowerPoint-версия Hub-материалов. Используется когда клиент просит редактируемый PPTX-файл вместо HTML.

---

## Внутренние документы (.docx)

> ⚠️ **Все .docx — untracked** (не закоммичены в git). Содержат internal pricing, sales-скрипты, market research. Хранить вне публичного репо.

### Готовые / актуальные

#### `Evimiz_Argentina_Camaras_FULL_v4.docx`
Market research Аргентины, версия 4. Заменены placeholder'ы реальными factory-ценами (KZ ops, май 2026). Блоки: TCO 5-летний (barrio cerrado, 12 камер 6MP — Evimiz ~55-65% дешевле Hikvision), 6 серий с real-pricing, 11 objections (+1 новое: «почему так дёшево»), decision matrix с AR wholesale price, hardware unit-economics. Pricing-модель: factory × 1.05 = AR wholesale, × 1.9-2.1 = recommended retail.

#### `Evimiz_Argentina_Camaras_SUMMARY_v4.docx`
Executive summary к FULL v4. Для technical decision-makers.

#### `Evimiz_Differentiators_v0.5.docx`
Positioning-документ. Заполнена только Секция 10 — **Pricing as a differentiator**:
- 10.1 Anatomy of distribution markup (Hikvision vs Evimiz)
- 10.2 Wholesale price-list
- 10.3 Recommended retail strategy
- 10.4 NO DUMPING — стратегическая дисциплина
- 10.5 Sales talking points
- 10.6 Channel partner program — pricing tiers
- 10.7 Когда поднимать / снижать цены
- 10.8 KPI для pricing-strategy success

Секции 1–9 (UX, app, dashboard, AI, hardware build, cloud, integrations, support, brand) — TODO, ждут product-team interview + benchmarks.

#### `Evimiz_Partner_PriceList_v2_2.pdf` / `.docx` — **partner-facing АКТУАЛЬНЫЙ (25.05.2026, latest)**
v2.2 — минор обновление v2.1: удалён раздел 5.2 (Combined bundles) для упрощения калькуляции. **Confidential** — не для прямого распространения.
- **Раздел 5.2** (Combined bundles: Cross-Sell Pack / Country Perimeter / PYME Retail Starter / Pro-Installer Bundle) — **УДАЛЁН**. Mixing of one-off hardware + monthly license + monthly archive в первый год создавал confusion для partner quoting.
- **5.3 → 5.2** — Bundle prepay options перенумерован
- Section 5 теперь компактный: только Bundle архива по зданию (5.1) + Bundle prepay options (5.2)
- Educational value не теряется — дублируется в Quick Reference 1.6 (структура расчёта) и Section 2.4 (License combined examples)
- Логика: партнёр сам собирает bundles под конкретный deal. Готовые pre-computed bundles = constraint, не помощь.

#### `Evimiz_Partner_PriceList_v2_1.pdf` / `.docx` — **устарел (25.05.2026, замёнен v2.2)**
v2.1 — minor update v2 с завуализацией discount-механизмов для market entry flexibility. **Confidential** — не для прямого распространения. Файлname без точки (`v2_1`) из-за ограничения Word AppleScript на конверсию.
- **Раздел 1.5** — Volume & prepay discounts: убраны конкретные % (−15%, −20%, −10% и т.д.), заменены на "обсуждаем индивидуально". License $2.50 остаётся fixed.
- **Раздел 1.6** — Combined example: убраны конкретные numbers, оставлена только структура расчёта с disclaimer "illustrative, не fixed quote"
- **Раздел 5.3** — Bundle prepay options: убраны −10% / −18% / −12%, заменены на directional text
- **Раздел 6.1** — Hardware volume tiers: убрана таблица 1-9/.../200+, заменено на "по запросу для каждого quote"
- **Раздел 6.2** — Archive Partner tier program: оставлены tier names (Starter/Growth/Strategic) и criteria (cam-base), но убраны конкретные % discount'ов
- Базовая структура (license $2.50, base wholesale tiers, hard ceilings по сегментам) — остаётся прозрачной
- Логика: на market entry stage не создавать price-anchor'ы, работать кейс-by-кейс. Pricing Model v5 (internal) сохраняет конкретные guidelines для нашей sales-команды.

#### `Evimiz_Partner_PriceList_v2.pdf` / `.docx` — **устарел (25.05.2026, замёнен v2.1)**
v2 — первая two-component версия с конкретными discount-таблицами. Заменён v2.1 после решения завуализировать discount-механизмы для market entry.

#### `Evimiz_Cloud_Pricing_Model_v5.docx` — **АКТУАЛЬНЫЙ internal (25.05.2026, late)**
v5 — критический rebuild v4 с двухкомпонентной архитектурой:
- **License $2.50/intercom/мес FIXED** (no discounts, no MAP, monthly only) — включает все AI features
- **Archive — отдельно**, только storage (без AI markup в COGS)
- Pro GM 44% → **53%**, Enterprise 57% → **71%** (AI убрано из archive COGS)
- License revenue stream ~$150K Y1 (5,000 intercoms × $2.50 × 12)
- Combined Y1 ARR: $450-750K (vs archive-only $300-600K в v4)
- Cost model упрощён: формула COGS без AI add-on absolute
- Все sales scripts обновлены под двухкомпонентную модель

#### `Evimiz_Partner_PriceList_v1.pdf` / `.docx` — **устарел (25.05.2026, early)**
v1 — первая попытка прайс-листа, single-component модель с AI add-ons. Заменён v2 после введения License компоненты.
Прайс-лист для авторизованных партнёров (administradores, installers, monitoring firms). **Confidential** — не для прямого распространения. Combined Hardware + Cloud + Bundles в одном документе. Структура: 1-page Quick Reference + детальный catalog (7 разделов, 8 страниц).
- Раздел 1 — Quick Reference (one-page summary всех wholesale цен и terms)
- Раздел 2 — Hardware Catalog (все 6 серий камер + NVR + intercom)
- Раздел 3 — Cloud Subscriptions (Starter / Pro / Enterprise / 1y motion / ARS-Basic / Custom Enterprise)
- Раздел 4 — Bundles (cloud-only S/M/L/XL + combined HW+cloud bundles + prepay options)
- Раздел 5 — Volume discounts & Partner tier program (Tier 1/2/3 по active cam-base)
- Раздел 6 — MAP-policy и recommended retail ceilings по сегментам
- Раздел 7 — Order process & support (lead times, RMA, contacts)
- PDF — для distribution партнёрам, .docx — editable master
- Валидно до 31 июля 2026, контакт: vadbaz1357@gmail.com

#### `Evimiz_Cloud_Pricing_Model_v4.docx` — устарел (20.05.2026, заменён v5)
**INTERNAL ONLY.** Operational pricing-инструмент:
- Reseller-архитектура, MAP-policy (three borders)
- Wholesale base tiers (Starter $3, Pro $5.5, Enterprise $11, 1y motion-only $6, ARS-Basic $2)
- AI add-ons (Alerts вшит в Pro, Analytics в Enterprise, LPR/FR — modular)
- Hard ceilings по сегментам (cross-sell consorcios $9/$15, barrios $11/$18, enterprise $15/$25)
- Partner volume tiers, bundle prepay (1y/3y/HW+1y)
- Bundle по зданию (S/M/L/XL wholesale: $25/$75/$200/custom)
- Any-camera open platform (ONVIF/RTSP, одинаковый pricing)
- Custom Enterprise Quotes (1y 24/7, AR-residency)
- Cost model (coefficient-based, anchor $2 + retention/motion/resolution coefficients + AI add-ons)
- Sales scripts (vs Hikvision/Verisure/Hipcam, 30d market standard)
- **Раздел 7 сокращён до 1-страничного executive summary** — полная research в companion-документе

#### `Облачное_хранение_видео_Аргентина_v2.docx` — **актуальный research (20.05.2026)**
Полный market research по AR cloud-archive рынку с прямым сравнением Evimiz vs конкуренты по сегментам:
- B2C consumer cloud (EZVIZ, Ring LATAM, TP-Link, IMOU, Hik-Connect)
- B2B platform providers (Videoloft, Angelcam, Axis, HikCentral Connect 2-SKU breakdown, Hanwha SKY, Eagle Eye, Ivideon, CameraFTP, Claro AR)
- AR-local monitoring services (Verisure, Prosegur, USS — Prosegur acquired, Hipcam analysis)
- Provider availability в AR (Google Nest/Arlo не работают)
- 30 дней = market standard (доминирующий retention)
- Resolution × codec impact (H.265 vs H.264 = 2× экономия)
- Регуляторика AR (Disposición 10/2015, vertical-specific 1y+ mandates)
- TAM AR cloud-archive ≈ $15-100M USD/год, SAM Evimiz $5-15M
- **Прямые сравнения Evimiz vs market по сегментам** (разделы 3.2, 4.3, 4.4, 5.3, 6.4, 7.3, 11.3)
- Главные insights: 1y motion-only — unique position, mid-tier −15-30% vs HikCentral, Hipcam не закрывает archive

#### `Архив_Облачное_хранение_видео_Аргентина_2026_Claude.docx` — апрельская research baseline (заменён v2)

#### `Evimiz_Cloud_Pricing_Model_v3.docx` — устарел (20.05.2026, поздняя версия)
**INTERNAL ONLY.** v3 = v2 + интеграция апрельской research + два структурных нововведения:
- **Раздел 7 расширен** реальными ставками 15+ провайдеров (Videoloft $8.99, Hanwha SKY HD2 $26.55, Eagle Eye $15-45, Angelcam $13.99, Ivideon $19, Hik-Connect $13.1 full pack)
- **Раздел 7.5** — provider availability в AR (Google Nest и Arlo НЕ работают)
- **Раздел 11.4** — H.265 codec story (2× storage экономия vs H.264)
- **NEW Раздел 13** — Bundle по зданию (S/M/L/XL wholesale партнёру: $25/$75/$200/custom, 9% discount vs per-camera)
- **NEW Раздел 14** — Any-camera support (open platform для ONVIF/RTSP, одинаковый pricing для Evimiz/Hikvision/Dahua/Axis, marketing-pitch на Evimiz hardware преимуществах)
- Sales-scripts 8.6-8.8: 30-day market standard, bundle pitch, open platform pitch

#### `Evimiz_Cloud_Pricing_Model_v2.docx` — устарел (20.05.2026, ранняя версия)
Coefficient-based COGS, 1y motion-only mass-market, 1y 24/7 в Custom Enterprise Quote. Заменён v3 (интеграция research + bundle + any-camera).
**INTERNAL ONLY.** v2 заменяет v1 (assumption-driven COGS → coefficient-based с реальным anchor от Артура):
- Anchor: 7d 24/7 1080p = $2 / cam / мес (от Артура)
- Полная формула COGS: `$2 × retention_coef × motion_modifier × resolution_coef + AI_add_ons` (см. раздел 11)
- 1y motion-only стал mass-market SKU: wholesale $6 (was $15), ceiling $12-18 по сегментам
- 1y motion-only впервые доступен для cross-sell consorcios (ceiling $12) и barrios privados (ceiling $14)
- 1y 24/7 переведён в **Custom Enterprise Quote** (раздел 12) — niche compliance-driven (банки, gov, critical infra), ~5-15 deals Y1
- Pro tier GM 44% Y1 — принято как стратегическое решение (priority — market share)
- Все остальные wholesale-tiers, partner volumes, MAP-policy, ceilings cross-sell/barrios/enterprise, AR-residency, AI add-ons, bundle prepay, sales scripts — сохранены из v1

#### `Evimiz_Cloud_Pricing_Model_v1.docx` — устарел (19.05.2026)
Первая версия reseller-модели с assumption-driven COGS. Заменена v2 после получения $2 anchor от Артура. Структура и большинство решений (reseller-architecture, hard ceilings cross-sell/barrios/enterprise/Pro/Enterprise, AI add-ons, AR-residency, bundle prepay, ARS-Basic, sales scripts) — сохранены в v2. Можно отправить в архив.

**Общее (для обоих версий):** Полная reseller-модель для cloud-архива включает:
- Архитектура: partner резеллит cloud (мы не биллим жителя напрямую)
- Three-tier pricing: COGS → wholesale → retail (ceiling по сегментам)
- Wholesale tiers: Starter $3 / Pro $5.5 / Enterprise $11 / 1y motion-only $15 / 1y 24/7 $80 / ARS-Basic ~$2
- AI features — гибрид: Alerts/Analytics вшиты в Pro/Enterprise, LPR + Face Recognition — modular add-on
- AR-residency premium (Buenos Aires) — soft-launch +$1.5 wholesale
- Hard ceilings по сегментам: cross-sell consorcios $9/$15, barrios $11/$18/$28, enterprise $15/$25/$130
- Partner volume tiers 1/2/3 (10-49 / 50-199 / 200+ cams)
- Bundle prepay: 1y prepay −10%, 3y −18%, HW+1y bundle −12%
- Конкурентные benchmarks (май 2026): HikCentral Connect $13/cam total, Verisure/Prosegur — другая категория, Hipcam не закрывает archive
- Sales scripts vs Hikvision/Verisure/Prosegur/Hipcam
- Open questions для Артура: 4 AWS COGS числа
- P&L implications + KPI

#### `Evimiz_Sales_Pricing_Playbook.docx`
**INTERNAL ONLY.** Для AR sales-team:
- Структура цены (3 этажа: factory / AR wholesale / retail)
- Полная pricing-матрица (все модели, конверсия 500 KZT/USD)
- Volume discount tiers + worked examples
- Approval matrix (кто авторизует какой discount)
- Bundle pricing (cross-sell, country-club, pro-installer)
- 5 negotiation-скриптов: prospect просит «just because» / знает цены конкурентов / использует Hipcam как leverage / в долгом цикле (барриос) / просит «special price только для меня»

### STUB — каркасы, не заполнены

#### `Evimiz_Argentina_3year_FinPlan_STUB.docx`
3-летний финплан для борда / инвесторов. Каркас: Assumptions, Revenue model, Cost model, P&L, Cash flow, Break-even, KPI dashboard, Funding need, Sensitivity. **Нужны входные данные:** COGS per series, sales-team headcount, marketing-budget, working capital, cash reserve, Series A timing.

#### `Evimiz_Roadmap_LATAM_STUB.docx`
Долгосрочная strategic-карта Evimiz в LATAM. Каркас: Текущий core (Y1-Y2) → Adjacent (smart locks, parking, EV charging) → Smart home convergence → AI-analytics → Insurance integrations → PropTech → Geographic expansion → M&A → Platform strategy → Exit/IPO. **Нужны входные данные:** strategic vision от founders, market sizing, M&A landscape.

### Архивные версии (можно удалить при следующей чистке)

`Evimiz_Argentina_Camaras_FULL.docx`, `_FULL_v2.docx`, `_FULL_v3.docx`,
`Evimiz_Argentina_Camaras_SUMMARY.docx`, `_SUMMARY_v2.docx`, `_SUMMARY_v3.docx`,
`Evimiz_Differentiators_STUB.docx` — заменены v4 / v0.5.

---

## Папка `assets/`

Все изображения, используемые в decks:

**Камеры (6 серий, по 2 файла на серию):**
- `cam-basic-series.png` / `_1.png`
- `cam-dual-light.png` / `_1.png`
- `cam-zoom-series.png` / `_1.png`
- `cam-strobe.png` / `_1.png`
- `cam-ptz-with-zoom.png` / `_1.png`
- `cam-motorized-ir-series.png` / `_1.png`
- `camera-bullet.jpg`

**Интерком и продукт:**
- `evimiz-intercom-1.jpg`, `evimiz-intercom-2.jpg`, `evimiz-intercom-crop.jpg`
- `intercom.png`, `intercom-banner-en.jpg`, `intercom-banner-es.jpg`
- `vs-banner-en.jpg`, `vs-banner-es.jpg`, `evimiz-vs-old.jpg`
- `batyr-camera.jpg`, `batyr-camera-crop.jpg`

**Приложение и платформа:**
- `app-live.jpg`, `app-live.png`
- `appstore.png`
- `phone-apps.png`
- `platform-ui.png`
- `face-recognition.png`

**Бренд:**
- `logo-evimiz.png`
- `mascot-camera.png`, `mascot-guitar.png`, `mascot-window.png`

**Команда / выставки:**
- `team-expo.jpg`, `team-expo-a.jpg`, `team-expo-b.png`

**Иконки:**
- `icon-email.png`

**Корневые скриншоты (en/es) для дашборда платформы:**
- `es-dashboard.png`, `12-english-dashboard.png`
- `es-call-quality.png`, `13-call-quality.png`
- `es-installation-points.png`, `14-installation-points-tab.png`
- `es-mobile-branding.png`, `07-mobile-branding-en.png`
- `es-mobile-stories.png`, `08-mobile-stories-en.png`
- `es-mobile-push.png`, `09-mobile-push-en.png`
- `es-mobile-market.png`, `10-mobile-market-en.png`
- `es-residents.png`, `05-residents-en.png`
- `es-point-detail.png`, `15-pro-house-detail.png`

---

## Известные проблемы / открытые вопросы

1. **Hub-v2 ссылается на v3-decks.** При следующем обновлении нужно перевязать `Evimiz-Hub-v2.html` на `Developers-v4`, `Integrators-v4`, `Admins-v4`.
2. **Старые версии засоряют корень.** В репо лежат v1/v2/v3 для всех аудиторий — 28 HTML суммарно. На каком-то этапе провести чистку: переместить устаревшее в `archive/` или удалить (история сохраняется в git).
3. **`.docx` untracked.** Решить: оставить вне git, или создать отдельный приватный репо для internal docs (sales playbook содержит wholesale-математику + скрипты).
4. **Differentiators секции 1–9 пусты.** Нужен product-team interview для заполнения UX / app / dashboard / AI / hardware build / cloud / integrations / support / brand.
5. **FinPlan и Roadmap — STUB'ы.** Нужны цифры от founders / финдира.
6. **Hub PPTX устарел.** `Evimiz-Hub-Presentation.pptx` не отражает v4-материалы. При запросе клиентом редактируемого PPTX — пересобрать из текущих v4 decks.

---

## Changelog

История изменений README. Обновляется после каждой работы над проектом.

### 2026-05-25 (latest) — Price List v2.2: убран Combined bundles раздел
- Удалён раздел 5.2 (Combined bundles) в Price List v2.2. Mixing hardware (one-off) + license (monthly) + archive (monthly) в одном bundle создавал confusion для partner quoting. Также конкретные numbers ($1,170, $5,800) создавали anchors, что противоречит философии завуализации discount-механизмов из v2.1.
- 5.3 → 5.2 (Bundle prepay options перенумерован).
- Section 5 теперь компактный: 5.1 Bundle архива (S/M/L) + 5.2 Bundle prepay options. Партнёр сам собирает bundle под конкретный deal.
- v2.1 → deprecated.

### 2026-05-25 — Price List v2.1: завуализация discount-механизмов
- **Логика:** на market entry stage не создавать price-anchor'ы. Партнёру не показывать конкретные % дисконтов — обсуждать каждый кейс индивидуально.
- **Что завуализировано в Price List v2.1** (5 разделов):
  - 1.5 Volume & prepay discounts → текстовое описание вместо таблицы
  - 1.6 Combined example → структура расчёта без точных numbers + disclaimer
  - 5.3 Bundle prepay options → directional text
  - 6.1 Hardware volume tiers → "по запросу" вместо таблицы
  - 6.2 Archive Partner tier program → tier names и criteria без % discount'ов
- **Что остаётся прозрачным:** License $2.50 fixed, base wholesale tiers ($3/$5.5/$11/$6/$2), hard ceilings по сегментам, soft floor рекомендация, recommended retail license soft.
- **Pricing Model v5 (internal)** — без изменений. Конкретные discount-tier'ы остаются как internal guidelines для нашей собственной sales-команды.
- Filename без точки (`v2_1.docx/.pdf`) — из-за ограничения Word AppleScript на конверсию имён с точкой.
- v2 → deprecated.

### 2026-05-25 (late) — КРИТИЧЕСКИЙ rebuild: двухкомпонентная архитектура (License + Archive)
- **Открыто:** Вадим уточнил что pricing двухкомпонентный. License $2.50/intercom/мес (FIXED, no discounts) включает ВСЕ AI features. Архив — отдельно (только storage).
- **Implications:** AI add-ons (LPR, FR, Analytics, Alerts) убраны из архива. Pro GM 44%→53%, Enterprise 57%→71%. License — новая revenue stream ~$150K Y1.
- Создан `Evimiz_Cloud_Pricing_Model_v5.docx` (50 KB) — internal source-of-truth, двухкомпонентная.
- Создан `Evimiz_Partner_PriceList_v2.docx` (49 KB) + `.pdf` (424 KB) — partner-facing artifact, синхронизирован с v5 модели.
- v4 pricing + v1 price list → deprecated.
- Combined Y1 ARR target: $450-750K (vs archive-only $300-600K в v4).
- License retail — partner-choice (нет hard ceiling). MAP применяется только к архиву и hardware.

### 2026-05-25 (early) — Partner Price List v1 (PDF + DOCX)
- Создан `Evimiz_Partner_PriceList_v1.pdf` (381 KB) и `.docx` (47.4 KB editable master) — первый partner-facing документ для quoting.
- Combined Hardware + Cloud + Bundles в одном документе, 8 страниц.
- Структура: 1-page Quick Reference + детальный 7-разделовый catalog.
- Included: hardware wholesale (6 серий) + recommended retail, cloud subscriptions wholesale + recommended retail by segment, AI add-ons, bundle по зданию (S/M/L/XL), combined HW+cloud bundles, volume discounts, partner tier program (1/2/3), MAP-policy, order process, support channels.
- Excluded (internal-only): factory cost, COGS breakdown, AR sales 5% commission механика, coefficient model, sales scripts.
- Валидно до 31 июля 2026. PDF — для distribution партнёрам, DOCX — editable master.
- Связь с другими документами: содержание соответствует Cloud_Pricing_Model_v4 (operational pricing) и валидировано research-документом (Облачное_хранение_видео_Аргентина_v2). Recommended retail ceilings выровнены с pricing-моделью.

### 2026-05-20 (final) — Split: Pricing Model v4 + Research v2 (parallel documents)
- **Главная архитектурная перестройка:** разделение pricing-модели и market research на два separate, синхронизированных документа (по аналогии с Mercado_Domofonos_FULL/SUMMARY pair).
- **`Evimiz_Cloud_Pricing_Model_v4.docx`** — operational pricing-инструмент. Раздел 7 (конкурентная разведка) сокращён до 1-страничного executive summary с главными anchors. Все остальные разделы (reseller architecture, base tiers, ceilings, bundles, any-camera, AI add-ons, custom enterprise, P&L, cost model) — сохранены из v3.
- **`Облачное_хранение_видео_Аргентина_v2.docx`** — полная market research по AR cloud-archive. Берёт за baseline апрельский Архив + добавляет майские находки (Hipcam analysis, Verisure/Prosegur/USS monitoring, HikCentral Connect 2-SKU breakdown, market consolidation, Hipcam НЕ закрывает archive). Содержит **прямые сравнения Evimiz wholesale/retail vs конкуренты по сегментам** (разделы 3.2, 4.3, 4.4, 5.3, 6.4, 7.3, 11.3).
- Логика разделения: pricing-документ — для sales/operations (actionable цены, sales scripts). Research-документ — для стратегии (анализ рынка, positioning, TAM, регуляторика).
- v3 → архив.

### 2026-05-20 (late) — Cloud Pricing Model v3 (research + bundle + any-camera)
- Создан `Evimiz_Cloud_Pricing_Model_v3.docx` — интеграция апрельской research (Google Doc «Облачное_хранение_видео_Аргентина_2026_Claude») + два структурных нововведения.
- Раздел 7 (Competitive benchmarks) расширен с реальными ставками 15+ провайдеров: Videoloft $8.99, Hanwha SKY HD2 $26.55, Eagle Eye $15-45, Angelcam $13.99, Ivideon $19, CameraFTP, Axis Camera Station.
- Раздел 7.5 — provider availability в AR: Google Nest Aware, Arlo Secure НЕ доступны в AR (важно для positioning, убирает 2 потенциальных конкурента из sales-discussion).
- Раздел 11.4 — H.265 codec story в Cost model (2× storage экономия vs H.264, sales-talking-point).
- NEW Раздел 13 — Bundle по зданию (S=$25, M=$75, L=$200, XL=custom). Партнёр платит fixed wholesale за пакет, 9% discount vs per-camera. Только для Pro 30d 24/7.
- NEW Раздел 14 — Any-camera support: открытая платформа для ONVIF/RTSP сторонних камер (Hikvision/Dahua/Axis). Одинаковый pricing для всех. Marketing pitch фокусируется на Evimiz hardware преимуществах (unified SLA, factory-direct, native intercom integration). Tech-assumption — нужно подтвердить с Артуром, что cloud принимает произвольные ONVIF feeds.
- Sales-scripts: 8.6 (30 days = market standard), 8.7 (bundle pitch для admins), 8.8 (open platform pitch).
- v2 → архив.

### 2026-05-20 — Cloud Pricing Model v2 (coefficient-based COGS)
- Создан `Evimiz_Cloud_Pricing_Model_v2.docx` — обновление v1 после получения $2 anchor (7d 24/7) от Артура.
- COGS-модель: coefficient-based scaling (retention × motion × resolution + AI absolutes). Полная формула в разделе 11.
- 1y motion-only стал mass-market: wholesale $15→$6. TAM expansion 2.5×, новый product-market fit.
- 1y motion-only впервые для cross-sell consorcios (ceiling $12) и barrios privados (ceiling $14, было $28).
- 1y 24/7 переведён из default catalog в **Custom Enterprise Quote** (раздел 12 документа) — niche compliance market (банки, gov, critical), ~5-15 deals Y1. Sales-process: vertical + camera count → quote через 1-2 дня.
- Pro tier GM 44% Y1 — стратегическое решение принято (market share priority vs SaaS-стандарт 60-75%).
- Новый sales-script 8.4: «1y motion-only retention теперь mass-market» — unique market position (никто из конкурентов не предлагает affordable legal-grade motion-only retention).
- Новый sales-script 8.5: что отвечать когда prospect спрашивает про 1y 24/7 (custom quote process).
- v1 → архив, документация обновлена.

### 2026-05-19 — Cloud Pricing Model v1
- Создан `Evimiz_Cloud_Pricing_Model_v1.docx` — полная reseller-модель для cloud-архива (INTERNAL ONLY).
- Конкурентная разведка cloud-цен в AR (май 2026): подтверждены ceilings против HikCentral Connect $13/cam, Verisure/Prosegur bundle $130-160, Hipcam $1-3/unit. Hipcam не закрывает archive-категорию — gap для Evimiz.
- Pricing-архитектура: partner резеллит cloud → flat wholesale → hard ceiling по сегментам. Risk неплатежа жителя на партнёре.
- ARPU/cam/мес: $4/$7/$15 → $3/$5.5/$11 wholesale (−25-30%), компенсируется predictable cashflow + faster channel-scaling.
- Hard ceilings cross-sell consorcios: Pro $9 / Enterprise $15 (подняты vs первоначальной модели $7/$12).
- AI features — гибрид: AI Alerts вшит в Pro, AI Analytics в Enterprise, LPR/Face Recognition — modular add-on.
- Long-retention 1y разделён: motion-only ($15 wholesale, $28 ceiling) vs 24/7 ($80 wholesale, $130 ceiling — для gov/banking).
- Введён ARS-Basic tier для anti-inflation hedge (manual gating ≤50 unit consorcios).
- AR-residency Buenos Aires — soft-launch как premium add-on +$1.5 wholesale.
- Bundle prepay: 1y −10%, 3y −18%, HW+1y bundle −12%.
- Открытый блок-вопрос: 4 AWS COGS-числа от Артура для финализации.

### 2026-05-10 — initial
- Создан README с полным описанием 28 HTML-презентаций, 1 PPTX, 13 .docx-документов, папки `assets/`.
- Зафиксированы текущие (рекомендуемые к показу) версии: Hub-v2, Developers-v4, Integrators-v4, Admins-v4, GEO-Platform-v3, Hardware-and-Pricing-v2, App-Demo-v2, Product-Tour-v2.
- Последняя реальная работа над проектом перед созданием README: 6 мая 2026 — `Evimiz_Sales_Pricing_Playbook.docx` + retail-pricing fix в Hardware-and-Pricing-v2 (commit `5236831`).

---

## Протокол обновления README

**После любых работ над проектом этот README должен обновляться.** Минимальный регламент:

1. **Если изменился `.html`/`.docx`/`.pptx`:**
   - Если файл новый → добавить в соответствующий раздел с описанием структуры (heading + список слайдов или секций).
   - Если файл стал «актуальным» (заменил предыдущую версию) → пометить его **актуальный**, старый → **устарел**, обновить таблицу [Текущие версии](#текущие-версии-рекомендуется-к-показу).
   - Если контент внутри файла поменялся (новые слайды / переписанный сюжет) → обновить bullet-список структуры в описании.

2. **Если поменялись `assets/`:**
   - Добавить новые файлы в раздел [Папка assets/](#папка-assets) в правильную категорию.

3. **Закрытие открытых пунктов:**
   - Когда решён один из пунктов в [Известные проблемы](#известные-проблемы--открытые-вопросы) — удалить его и упомянуть в Changelog.

4. **Запись в Changelog:**
   - Каждое обновление README должно сопровождаться новой записью в [Changelog](#changelog) сверху, в формате:
     ```
     ### YYYY-MM-DD — короткое название
     - что изменилось
     - что добавлено / удалено
     ```

5. **Когда не нужно трогать README:**
   - Косметические правки CSS / опечатки в существующих слайдах без изменения структуры.
   - Багфиксы рендеринга.
   - Эксперименты в feature-ветках до мерджа в `main`.

---

*Поддерживается командой Evimiz при ассистенции Claude. По вопросам — Vadim (vadbaz2468@gmail.com).*
