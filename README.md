# AlmaTaurina

MVP para la gestión integral de peñas taurinas: socios, cuotas, eventos y pagos. Frontend en Angular, backend/BaaS en Supabase y Stripe para cobros en fases posteriores.

## Requisitos

- Node.js >= 18.x
- npm >= 9.x (incluido con Node)
- Angular CLI >= 18 (instalar con `npm install -g @angular/cli@18`)

## Puesta en marcha

```bash
git clone https://github.com/AlejandroLatorre/AlmaTaurina.git
cd AlmaTaurina/alma-taurina-app
npm install
ng serve
```

La aplicación estará disponible en `http://localhost:4200/`.

## Verificación manual

1. `ng serve` compila sin errores y muestra "Compiled successfully" en la terminal.
2. Al abrir `http://localhost:4200` deberías ver la página inicial por defecto de Angular (logo + enlaces de recursos).
3. `git status` indica `nothing to commit, working tree clean`.
4. `git push` confirma que la rama `main` se ha publicado en el remoto `origin` (`AlejandroLatorre/AlmaTaurina`).

## Estructura inicial (pensada para escalar)

```
alma-taurina-app/
└── src/app/
    ├── core/        # servicios singleton, guards, interceptors
    ├── shared/      # componentes/pipes reutilizables
    ├── features/    # módulos por contexto (login, admin, peñista, ...)
    ├── app.routes.ts
    └── app.config.ts
```

Esta distribución permite sumar módulos por dominio sin reestructurar la base del proyecto durante los siguientes sprints.
