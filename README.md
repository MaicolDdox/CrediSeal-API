<p align="center">
  <a href="https://github.com/MaicolDdox/CrediSeal-API?tab=readme-ov-file target="_blank">
    <img src="docs/assets/logo.png" width="260" alt="Logo de CrediSeal API">
  </a>
</p>

[![GitHub](https://img.shields.io/badge/GitHub-MaicolDdox-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/MaicolDdox)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/maicol-duvan-gasca-rodas-4483923a4/?trk=public-profile-join-page)
[![Instagram](https://img.shields.io/badge/Instagram-@maicolddox__-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/maicolddox_?utm_source=qr&igsh=cTV6enRlMW05bjY3)
[![Discord](https://img.shields.io/badge/Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white)](https://discordapp.com/users/1425631850453270543)
[![Facebook](https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white)](https://www.facebook.com/profile.php?id=61586710675179&sk=about_contact_and_basic_info)


<p align="center">
  <strong>CrediSeal API</strong><br>
  API REST para emitir, verificar y gestionar credenciales digitales verificables con enfoque antifraude.
  (TODAVIA ESTA EN DESARROLLO - DISPONIBLE PROXIMAMENTE)
</p>

---

## Acerca de CrediSeal API

**CrediSeal API** es una API REST construida con **Laravel 12 + Sanctum** que permite a organizaciones (emisores) **emitir credenciales digitales verificables** (insignias/certificados) a usuarios (titulares), con **verificación pública**, **revocación con historial** y **auditoría** para garantizar trazabilidad y reducir fraude.

Este proyecto está diseñado para portafolio y demuestra:
- Autenticación por tokens con **Sanctum**
- Control de acceso por roles con **Spatie Laravel-Permission**
- Diseño de API orientado a seguridad
- Modelado de datos realista (organizaciones, plantillas, eventos, credenciales)
- Registro de verificaciones y auditoría de acciones críticas

---

## Características principales

- **Auth**: Registro / Login / Logout / manejo de tokens (Sanctum)
- **Organizaciones**: gestión de emisores y membresías
- **Eventos/Cursos**: contexto para emisión de credenciales
- **Plantillas**: flujo Borrador → Publicada
- **Emisión de credenciales**:
  - emisión individual
  - emisión masiva (batch)
- **Verificación pública** (sin autenticación) mediante `public_code`
- **Revocación** con motivo e historial
- **Auditoría** para acciones críticas (emitir, revocar, publicar, cambios de rol)
- Paginación, filtros y estructura consistente de respuestas

---

## Roles y permisos (máximo 3 roles)

### 1) Admin
- Administra organizaciones, ve auditoría global y configura reglas del sistema.

### 2) Issuer (Emisor)
- Crea eventos y plantillas, emite y revoca credenciales dentro de su organización.

### 3) Holder (Titular)
- Visualiza su “wallet” de credenciales y gestiona visibilidad/compartir (opcional).

> Los permisos se implementan con **Spatie Laravel-Permission** y se aplican en rutas/controladores.

---

## Guía rápida de instalación (local)

### Requisitos
- PHP >= 8.2 (recomendado para Laravel 12)
- Composer
- MySQL / PostgreSQL

### Pasos
1. Clona el repositorio
2. Instala dependencias con Composer
3. Configura `.env`
4. Ejecuta migraciones (y seeders si aplican)
5. Levanta el servidor y prueba con Postman/Insomnia

---

## Seguridad
Si encuentras una vulnerabilidad de seguridad, repórtala de forma privada:
- Email: **maicolindustriascode@gmail.com**

---

## Licencia
Este proyecto se publica bajo licencia **MIT**.
Ver el archivo [LICENSE](LICENSE).
