# Keepsake — Responsive Landing Page

Адаптивний односторінковий лендінг дизайн-агенції **Keepsake**, зверстаний за підходом **Mobile First** без використання сторонніх CSS/UI-фреймворків.

- **Демо (GitHub Pages):** `https://<username>.github.io/landing-keepsake/`

## Структура проєкту

```text
landing-keepsake/
├── index.html
├── README.md
├── css/
│   ├── reset.css
│   └── style.css
├── images/
│   ├── work-1.webp ... work-9.webp
│   └── journal-1.webp ... journal-4.webp
└── fonts/
```

## Використані технології та рішення

- **Семантичний HTML5:** використано `header`, `nav`, `aside`, `main`, `section`, `article`, `figure`, `figcaption`, `footer`, `form`, один `h1` на сторінку та логічну ієрархію заголовків `h1–h3`.
- **CSS Variables (`:root`):** усі кольори, шрифти, відступи контейнера та міжсекційні інтервали винесені в дизайн-токени.
- **Mobile First & Брейкпоінти:** базові стилі для екранів від `320px` (макет `375px`), адаптація через `@media (min-width: 768px)` (Tablet) та `@media (min-width: 1280px)` (Desktop), максимальна ширина контенту `1100px`.
- **Flexbox & CSS Grid:** розкладка навігації, кнопок, карток журналу й футера побудована на Flexbox; сітка робіт портфоліо реалізована через CSS Grid (`1` колонка / `5` карток на Mobile, `2` колонки / `8` карток на Tablet, `3` колонки / `9` карток на Desktop) із збереженням пропорцій через `aspect-ratio`.
- **Інтерактивність без JS:**
  - Мобільне виїзне меню працює на чистому CSS через прихований `checkbox` (`#menu-toggle:checked ~ .mobile-drawer`).
  - Фільтрація карток портфоліо за категоріями реалізована на чистому CSS через радіокнопки та загальний сусідній селектор (`:checked ~`).
- **Доступність та продуктивність:** підтримка навігації з клавіатури (`:focus-visible`, `:focus-within`), атрибути `aria-label`, `aria-controls`, `aria-expanded`, `aria-describedby`, зображення у форматі **WebP** із заданими `width` / `height` та `loading="lazy"`.
