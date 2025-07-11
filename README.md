# 🔐 Java Auth – Spring Boot + Google OAuth2 + JWT + React

A simple authentication boilerplate using **Java Spring Boot** for backend and **React** for frontend. It supports logging in with Google using OAuth2 and issues JWT tokens for secure API access. Easily extensible for other providers or custom logic.

## 🚀 Features

- Login via Google OAuth2 (Spring Security)
- JWT token generation (using jjwt)
- REST API endpoint to get user data (`/user`)
- CORS configured for local and production frontend
- React frontend (example), ready for integration
- Clean, extensible code (add more providers easily)
- Logout endpoint

## 🛠 Technologies Used

- **Backend:** Java, Spring Boot, Spring Security, jjwt
- **Frontend:** React (example structure)
- **OAuth2:** Google
- **JWT:** Secure token for API requests

## ⚡ Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/FoxerBN/java-auth.git
cd java-auth
```

### 2. Backend setup

- Set your Google OAuth2 credentials in `application.properties`:
  ```
  spring.security.oauth2.client.registration.google.client-id=your-client-id
  spring.security.oauth2.client.registration.google.client-secret=your-client-secret
  app.jwt.secret=your-jwt-secret-key
  app.frontend.url=http://localhost:3000
  ```
- Run backend:
  ```bash
  ./mvnw spring-boot:run
  ```
### 3. Frontend setup

- Use any React template, set up Google OAuth2 login and fetch `/user` endpoint.

### 4. Try the demo

(https://react-auth-henna.vercel.app)

## 📦 API Endpoints

- `GET /user` – returns user data (email, name, etc.)
- OAuth2 login URL: `/oauth2/authorization/google`
- Logout: `/logout`

## 🌱 Extending

- Add more OAuth2 providers in `SecurityConfig.java`
- Customize JWT payload in `TokenProvider.java`
- Extend user handling in `UserController.java`

## 💡 License

[MIT](LICENSE)

---

## Live Demo

👉 [Demo link](https://react-auth-henna.vercel.app/)
