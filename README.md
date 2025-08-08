# 🌟 Nombrini

[![Laravel](https://img.shields.io/badge/Laravel-10.x-red?style=flat&logo=laravel)](https://laravel.com)
[![Vue 3](https://img.shields.io/badge/Vue.js-3.x-green?style=flat&logo=vue.js)](https://vuejs.org)
[![Inertia.js](https://img.shields.io/badge/Inertia.js-enabled-blueviolet)](https://inertiajs.com/)
[![Vite](https://img.shields.io/badge/Vite-fast-purple?logo=vite)](https://vitejs.dev)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

**Nombrini** is a full-stack web app where users can create, save, and share personalized baby name lists. Built with Laravel, Vue 3, Inertia.js, and Vite, this app combines modern tools and clean architecture to deliver a delightful and smooth user experience.

> ✨ Designed to showcase my skills as a full-stack developer and also grow into a real product for people looking for the perfect name.

---

## 🎯 Project Goals

- ✅ Demonstrate full-stack development with Laravel + Vue
- ✅ Follow modern development best practices
- ✅ Be usable by real-world users
- ✅ Explore UI/UX design through custom Figma wireframes

---

## ✨ Features

- 👶 Create & manage custom baby name lists
- 📌 Add notes or tags to each name
- 💬 Multilingual support (i18n)
- 🧑‍🤝‍🧑 Share lists with friends or partners
- 🔍 Search and filter by gender, origin, popularity
- 🧠 Smart name suggestions (coming soon!)

---

## 🛠 Tech Stack

| Tech        | Details                                    |
|-------------|--------------------------------------------|
| Backend     | Laravel 10                                  |
| Frontend    | Vue 3, Composition API                      |
| Integration | Inertia.js (no REST API needed)            |
| Styling     | Tailwind CSS                                |
| Build tool  | Vite                                        |
| Design      | [Figma](#figma-design)                     |

---

## 🚀 Local Setup

Clone the repo:

```bash
git clone https://github.com/anigandini/nombrini.git
cd nombrini/backend
Install dependencies:


composer install
npm install
Create .env file:

cp .env.example .env
php artisan key:generate
Run migrations and seeders (optional):


php artisan migrate --seed
Start dev servers:


php artisan serve
npm run dev

```
---

## 🎨 Figma Design


Here’s the full design concept for the Nombrini interface:

🔗 View Figma File
---

## 🖼️ Screenshots

(Coming soon — will include login, name list view, mobile UI, etc.)

---

## 📂 Project Structure
```bash
nombrini/
├── backend/         # Laravel app with Vue frontend (Inertia)
│   ├── app/
│   ├── resources/js/  <-- Vue 3 components
│   ├── routes/
│   ├── public/
│   └── ...
├── README.md
├── LICENSE
└── .gitignore
```
---

## 💡 Highlights
Fully localized UI using Laravel's i18n

Laravel Collections for advanced filtering and data handling

Clean separation of concerns via Services and DTOs

Optimized with Vite for fast build and reload times

Responsive mobile-first layout

---

## 📄 License
This project is open source under the MIT License.

Made with ❤️ by Ani Gandini
---
