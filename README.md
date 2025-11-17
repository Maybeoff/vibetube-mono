# VibeTube

Реалистичный клон YouTube, созданный с использованием **SvelteKit** и **SQLite**.

## Особенности

- 🎬 **Загрузка видео** - Загружайте видео с эскизами (поддержка перетаскивания)
- 👤 **Аутентификация пользователей** - Регистрация, вход в систему, сеансы на основе JWT
- 💬 **Комментарии** - Система комментирования в реальном времени
- 👍 **Лайки и дизлайки** - Взаимодействуйте с видео
- 🔔 **Подписки** - Подписывайтесь на любимых авторов
- 🔍 **Поиск** - Поиск видео по названию и описанию
- 📱 **Адаптивный дизайн** - Работает на настольных компьютерах, планшетах и мобильных устройствах
- 🌙 **Темная тема** - Профессиональный пользовательский интерфейс в стиле YouTube
- ⚡ **Быстрая производительность** - SSR с SvelteKit + SQLite

## Технологический стек

- **Frontend & Backend**: SvelteKit (TypeScript)
- **Database**: SQLite с Better-SQLite3
- **Authentication**: JWT с bcryptjs
- **File Uploads**: Native FormData handling
- **Styling**: Custom CSS (вдохновленный YouTube)
- **Icons**: Lucide Svelte

## Структура проекта

```
/
├── ADD_YOUR_LOGO_HERE.md
├── ALL_FIXES_COMPLETE.md
├── COMPLETE_UPDATE.md
├── FINAL_FIXES_COMPLETE.md
├── FINAL_UPDATE.md
├── FIXES_APPLIED.md
├── LATEST_FIXES.md
├── LATEST_UPDATES.md
├── MOBILE_AND_STUDIO_UPDATE.md
├── PHASE1_COMPLETE.md
├── PROJECT_COMPLETE.md
├── SUMMARY.md
├── VibeTube/
│   ├── FILE_STRUCTURE.md
│   ├── logo.png
│   ├── migrate-thumbnail.js
│   ├── package.json
│   ├── QUICK_START.md
│   ├── README.md
│   ├── seed.js
│   ├── START_HERE.md
│   ├── svelte.config.js
│   ├── tsconfig.json
│   ├── vite.config.ts
│   ├── src/
│   │   ├── app.css
│   │   ├── app.d.ts
│   │   ├── app.html
│   │   ├── lib/
│   │   │   ├── auth.ts
│   │   │   ├── db.ts
│   │   │   ├── i18n.ts
│   │   │   ├── index.ts
│   │   │   ├── theme.ts
│   │   │   ├── utils.ts
│   │   │   ├── assets/
│   │   │   │   ├── favicon.svg
│   │   │   ├── components/
│   │   │   │   ├── CommentItem.svelte
│   │   │   │   ├── Comments.svelte
│   │   │   │   ├── Header.svelte
│   │   │   │   ├── LanguageSwitcher.svelte
│   │   │   │   ├── Sidebar.svelte
│   │   │   │   ├── VideoCard.svelte
│   │   │   │   ├── VideoGrid.svelte
│   │   ├── routes/
│   │   │   ├── +layout.svelte
│   │   │   ├── +page.svelte
│   │   │   ├── api/
│   │   │   │   ├── auth/
│   │   │   │   │   ├── login/
│   │   │   │   │   │   ├── +server.ts
│   │   │   │   │   ├── logout/
│   │   │   │   │   │   ├── +server.ts
│   │   │   │   │   ├── me/
│   │   │   │   │   │   ├── +server.ts
│   │   │   │   │   ├── register/
│   │   │   │   │   │   ├── +server.ts
│   │   │   │   ├── comments/
│   │   │   │   │   ├── +server.ts
│   │   │   │   │   ├── [id]/
│   │   │   │   │   │   ├── +server.ts
│   │   │   │   │   │   ├── heart/
│   │   │   │   │   │   │   ├── +server.ts
│   │   │   │   │   │   ├── like/
│   │   │   │   │   │   │   ├── +server.ts
│   │   │   │   │   │   ├── pin/
│   │   │   │   │   │   │   ├── +server.ts
│   │   │   │   ├── liked/
│   │   │   │   │   ├── videos/
│   │   │   │   │   │   ├── +server.ts
│   │   │   │   ├── likes/
│   │   │   │   │   ├── +server.ts
│   │   │   │   ├── studio/
│   │   │   │   │   ├── comments/
│   │   │   │   │   │   ├── +server.ts
│   │   │   │   │   ├── stats/
│   │   │   │   │   │   ├── +server.ts
│   │   │   │   ├── subscriptions/
│   │   │   │   │   ├── +server.ts
│   │   │   │   ├── user/
│   │   │   │   │   ├── update/
│   │   │   │   │   │   ├── +server.ts
│   │   │   │   ├── users/
│   │   │   │   │   ├── [id]/
│   │   │   │   │   │   ├── +server.ts
│   │   │   │   ├── videos/
│   │   │   │   │   ├── +server.ts
│   │   │   │   │   ├── [id]/
│   │   │   │   │   │   ├── +server.ts
│   │   │   │   │   │   ├── update/
│   │   │   │   │   │   │   ├── +server.ts
│   │   │   │   ├── watch-history/
│   │   │   │   │   ├── +server.ts
│   │   │   ├── channel/
│   │   │   │   ├── [id]/
│   │   │   │   │   ├── +page.svelte
│   │   │   ├── history/
│   │   │   │   ├── +page.svelte
│   │   │   ├── liked/
│   │   │   │   ├── +page.svelte
│   │   │   ├── login/
│   │   │   │   ├── +page.svelte
│   │   │   ├── my-videos/
│   │   │   │   ├── +page.svelte
│   │   │   ├── register/
│   │   │   │   ├── +page.svelte
│   │   │   ├── search/
│   │   │   │   ├── +page.svelte
│   │   │   ├── settings/
│   │   │   │   ├── +page.svelte
│   │   │   ├── studio/
│   │   │   │   ├── +page.svelte
│   │   │   │   ├── analytics/
│   │   │   │   │   ├── +page.svelte
│   │   │   │   ├── comments/
│   │   │   │   │   ├── +page.svelte
│   │   │   │   ├── edit/
│   │   │   │   │   ├── [id]/
│   │   │   │   │   │   ├── +page.svelte
│   │   │   │   ├── videos/
│   │   │   │   │   ├── +page.svelte
│   │   │   ├── trending/
│   │   │   │   ├── +page.svelte
│   │   │   ├── upload/
│   │   │   │   ├── +page.svelte
│   │   │   ├── watch/
│   │   │   │   ├── [id]/
│   │   │   │   │   ├── +page.svelte
│   │   │   ├── watch-later/
│   │   │   │   ├── +page.svelte
│   ├── static/
│   │   ├── logo.png
│   │   ├── robots.txt
│   │   ├── uploads/
│   │   │   ├── .gitkeep
```

## Ссылки на файлы

- [ADD_YOUR_LOGO_HERE.md](ADD_YOUR_LOGO_HERE.md)
- [ALL_FIXES_COMPLETE.md](ALL_FIXES_COMPLETE.md)
- [COMPLETE_UPDATE.md](COMPLETE_UPDATE.md)
- [FINAL_FIXES_COMPLETE.md](FINAL_FIXES_COMPLETE.md)
- [FINAL_UPDATE.md](FINAL_UPDATE.md)
- [FIXES_APPLIED.md](FIXES_APPLIED.md)
- [LATEST_FIXES.md](LATEST_FIXES.md)
- [LATEST_UPDATES.md](LATEST_UPDATES.md)
- [MOBILE_AND_STUDIO_UPDATE.md](MOBILE_AND_STUDIO_UPDATE.md)
- [PHASE1_COMPLETE.md](PHASE1_COMPLETE.md)
- [PROJECT_COMPLETE.md](PROJECT_COMPLETE.md)
- [SUMMARY.md](SUMMARY.md)
- [VibeTube/FILE_STRUCTURE.md](VibeTube/FILE_STRUCTURE.md)
- [VibeTube/logo.png](VibeTube/logo.png)
- [VibeTube/QUICK_START.md](VibeTube/QUICK_START.md)
- [VibeTube/README.md](VibeTube/README.md)
- [VibeTube/START_HERE.md](VibeTube/START_HERE.md)

## Лицензия

MIT License - Feel free to use for learning and projects!

## Благодарности

Built with ❤️ using:

- [SvelteKit](https://kit.svelte.dev/)
- [Better-SQLite3](https://github.com/WiseLibs/better-sqlite3)
- [Lucide Icons](https://lucide.dev/)

---

**VibeTube** - Your videos, your vibe! 🎵
