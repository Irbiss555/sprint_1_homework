
### Уровень 1: 
Для разделения проекта Mesto на микрофронтенды, я выберу **Webpack Module Federation**. Судя по материалу курса, он более простой и лучше подойдет для такого небольшого проекта.


### Уровень 2:

**Микрофронтенды**:
  1. **Auth Microfrontend**: Управление аутентификацией (вход, регистрация).
  2. **Profile Microfrontend**: Управление профилем пользователя (создание, редактирование).
  3. **Gallery Microfrontend**: Управление фотографиями (загрузка, удаление, лайки).
  4. **Host**: Основное приложение, которое интегрирует все микрофронтенды.

#### Структура проекта
```plaintext
/microfrontend
  /auth-microfrontend
    /src
      /context
        CurrentUserContext.js
      /components
        InfoToolTip.js
        Login.js
        Register.js
      /styles
        /auth-form
        /login
      /utils
        auth.js
      index.js
    package.json
    webpack.config.js
  /profile-microfrontend
    /src
      /components
        EditAvatar.js
        EditProfile.js
      /styles
        /__add-button
        /__description
        /__edit_button
        /__image
        /__info
        /__title
      /images
        add-icon.svg
        avatar.jpg
      index.js
    package.json
    webpack.config.js
  /gallery-microfrontend
    /src
      /components
        AddPlacePopup.js
        Card.js
        ImagePopup.js
      /styles
        /card
        /places
      /images
        card_1.jpg
        card_2.jpg
        card_3.jpg
        delete-icon.svg
        edit-icon.svg
        like-active.svg
        like-inactive.svg
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

Такое разделение было выбрано на основе функциональности монолитного приложения, с учетом принципов DDD

