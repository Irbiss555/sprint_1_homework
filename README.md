
### Уровень 1: 
Для разделения проекта Mesto на микрофронтенды, я выберу **Webpack Module Federation**. Этот подход позволяет динамически загружать части приложения из разных источников, что делает его идеальным для микрофронтендов


#### Решение
- **Микрофронтенды**:
  1. **Auth Microfrontend**: Управление аутентификацией (вход, регистрация).
  2. **Profile Microfrontend**: Управление профилем пользователя (создание, редактирование).
  3. **Gallery Microfrontend**: Управление фотографиями (загрузка, удаление, лайки).
  4. **Host**: Основное приложение, которое интегрирует все микрофронтенды.

### Уровень 2: Планирование изменений

#### Структура проекта
```plaintext
/microfrontend
  /auth-microfrontend
    /src
      /components
        Login.js
        Register.js
      /styles
        login.css
        register.css
      /utils
        auth.js
      index.js
    package.json
    webpack.config.js
  /profile-microfrontend
    /src
      /components
        Profile.js
        EditProfile.js
      /styles
        profile.css
        edit-profile.css
      /utils
        profile.js
      index.js
    package.json
    webpack.config.js
  /gallery-microfrontend
    /src
      /components
        Gallery.js
        Photo.js
      /styles
        gallery.css
        photo.css
      /utils
        gallery.js
      index.js
    package.json
    webpack.config.js
  /host
    /src
      /components
        App.js
        Navbar.js
      /styles
        app.css
        navbar.css
      index.js
    package.json
    webpack.config.js
  README.md
```

#### Обоснование
- **Auth Microfrontend**: Отделение логики аутентификации позволяет независимо разрабатывать и тестировать функции входа и регистрации.
- **Profile Microfrontend**: Управление профилем пользователя выделено в отдельный микрофронтенд для упрощения поддержки и масштабирования.
- **Gallery Microfrontend**: Функции, связанные с фотографиями, выделены в отдельный микрофронтенд для независимой разработки и деплоя.
