 # AGENTS.md

## 🧠 Purpose
This document defines how automated agents (and developers) should interact with the Aegis codebase.  
It establishes conventions, constraints, and expectations to ensure consistency, security, and maintainability.

---

## ⚙️ Project Overview
- Name: Aegis
- Stack: PHP (no framework), MySQL, Bootstrap, Font Awesome
- Architecture Style: Lightweight MVC-inspired structure
- Environment: Local dev → production deployment

---

## 📁 Directory Conventions
~~~ plaintext
app/
  Controllers/
    Controller.php
    Web/
      HomeController.php
      DashboardController.php
    Auth/
      LoginController.php
      RegisterController.php
      ForgotPasswordController.php
      ResetPasswordController.php
      LogoutController.php
    Admin/
      AdminDashboardController.php
      UserController.php
      RoleController.php
      PermissionController.php
      SettingsController.php
    Api/
      V1/
        AuthController.php
        UserController.php
        AnalyticsController.php
    User/
      ProfileController.php
      SettingsController.php
    Media/
      MediaController.php
      UploadController.php
    Security/
      CodeSecurityController.php
    System/
      HealthController.php
      BackupController.php
      DatabaseToolController.php
  Models/
  Modules/
    Admin/
      Dashboard/
      Users/
      Roles/
      Permissions/
    AI/
      Assistant/
      Analysis/
      Intelligence/
    Analytics/
    Api/
    Auth/
    Core/
    Dashboard/
    Integrations/
    Media/
      Manager/
    Messaging/
    Network/
      Designer/
    Notifications/
    Security/
      CodeSecurity/
    User/
      Manager/
      Profiles/
      Settings/
  Services/
  Repositories/
bootstrap/
config/
database/
  migrations/
  seeders/
  sql/
public/
  index.php
  assets/
    css/
    fonts/
    js/
    icons/
    img/
resources/
  assets/
    sass/
    js/
    css/
  views/
    admin/
      dashboard.php
    auth/
      login.php
      register.php
      forgot-pass.php
      reset-pass.php
      email-pass.php
    fields/
      email.php
      firstname.php
      lastname.php
      password.php
      username.php
    help/
      index.php
    layouts/
      base.php
      admin.php
      user.php
    pages/
      privacy.php
      terms.php
    partials/
      datatables.php
      editor.php
      footer.php
      header.php
      navigation.php
      styles.php
      scripts.php
    users/
      dashboard.php
      profile.php
      settings.php
routes/
  routes.php
scripts/
  .gitkeep
storage/
  logs/
  cache/
  sessions/
  data/
  backups/
.gitignore
.prettierignore
.prettierrc
.htaccess
composer.json
package.json
~~~
### Rules
- Business logic → app/
- Public entry point → public/index.php
- No direct access to internal folders
- Sensitive files must never live in public/

---

## 🔐 Security Rules

### Input / Output
- ALWAYS sanitize input (sanitize_*)
- ALWAYS escape output (e())
- NEVER trust user input

### Authentication
- Use password_hash() and password_verify()
- Never store plain-text passwords

### CSRF
- All forms must include csrf_token()
- All POST requests must verify with csrf_verify()

### Sessions
- Use secure session settings (HttpOnly, SameSite)
- Regenerate session IDs after login

---

## 🗄️ Database Rules

- Use PDO only
- Use prepared statements only
- No raw query concatenation

Example:
php $stmt = db()->prepare("SELECT * FROM users WHERE id = :id"); $stmt->execute(['id' => $id]); 

- Tables must use:
  - utf8mb4
  - InnoDB
- Always include:
  - created_at
  - updated_at

---

## ⚡ Coding Standards

- declare(strict_types=1); required in all PHP files
- Follow PSR-12 style where practical
- Functions must be small and focused
- No duplicate logic — extract helpers/services

---

## 🧩 Helper Usage

Use global helpers where appropriate:

- e() → escape output
- db() → database access
- redirect() → redirects
- json_response() → API responses
- csrf_token() / csrf_verify()
- env_health_check() for diagnostics

---

## 🌐 Frontend Rules

### CDN Policy
- Always use cdn.jsdelivr.net
- Prefer pinned versions in production
- Use @latest only in development

### UI Stack
- Bootstrap for layout
- Font Awesome for icons
- SweetAlert2 for alerts
- Tippy.js for tooltips

---

## 🔄 Configuration Rules

- Config stored in .toml or environment variables
- Never hardcode secrets
- Sensitive values must use env placeholders:
    password = "${DB_PASSWORD}"  

---

## 📊 Logging & Debugging

- Errors must be logged to storage/logs
- Never expose stack traces in production
- Use dd() only in development

---

## 🧪 Environment Health

- Use env_health_check() to validate:
  - PHP version
  - Extensions
  - DB connection
  - Writable directories

---

## 🚫 Forbidden Practices

- ❌ Direct SQL string interpolation
- ❌ Storing secrets in repo
- ❌ Mixing HTML + heavy PHP logic
- ❌ Using global state unnecessarily
- ❌ Writing to arbitrary filesystem paths

---

## 🧭 Agent Behavior Rules

Agents modifying this project must:

1. Follow existing structure (do not invent new patterns)
2. Prefer extending helpers/services over duplicating logic
3. Maintain backward compatibility unless instructed otherwise
4. Validate security implications before adding features
5. Keep code minimal and readable

---

## 🚀 Philosophy

> Keep it simple. Keep it secure. Keep it predictable.

Aegis is intentionally lightweight.  
Do not introduce unnecessary complexity, frameworks, or abstractions.

---

## 📌 Final Note

If unsure:
- Choose the simplest solution
- Favor clarity over cleverness
- Prioritize security over convenience

--
