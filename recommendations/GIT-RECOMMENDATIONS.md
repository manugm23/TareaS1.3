# Git: Gestión de versiones

Git es una herramienta para guardar y controlar los cambios en tu código.

## 1) Cambiar el remoto (origin)

El "remoto" es donde se guarda tu código en internet (GitHub, GitLab, etc).

**Pasos:**
1. Copia el URL de tu repositorio nuevo.
2. Abre la terminal en tu proyecto.
3. Ejecuta:
```bash
git remote set-url origin https://github.com/tu-usuario/tu-nuevo-repo.git
```

**Para verificar que cambió:**
```bash
git remote -v
```

## 2) Nunca programes directamente en `main`

`main` es la rama principal, la versión "lista para usar". Siempre debes trabajar en ramas nuevas.

## 3) Usa ramas feature desde develop

**Flujo recomendado:**

1. **Crea una rama `develop`** (una sola vez):
```bash
git checkout -b develop
git push -u origin develop
```

2. **Crea una rama feature desde develop:**
```bash
git checkout develop
git pull origin develop
git checkout -b feature/nombre-tu-feature
```

**Nombres de ramas útiles:**
- `feature/menu-navegacion`
- `feature/seccion-hero`
- `feature/formulario-contacto`

3. **Trabaja en tu rama:**
```bash
git add .
git commit -m "Descripción de los cambios"
git push origin feature/nombre-tu-feature
```

4. **Cuando termines, haz un Pull Request (PR)** en GitHub:
   - Ve a tu repositorio en GitHub.
   - Verás un botón de "Compare & pull request".
   - Describe qué hiciste.
   - Sube el PR.

5. **Fusiona con develop:**
   - Revisa los cambios.
   - Haz clic en "Merge pull request".
   - Elimina la rama cuando termine.

**Resumen visual:**
```
main (versión final)
  ↑
develop (versión de desarrollo)
  ↑
feature/mi-funcionalidad (donde trabajas)
```

## 4) Comandos Git básicos útiles

- `git status`: ve el estado actual.
- `git log --oneline`: ve el historial de cambios.
- `git branch -a`: ve todas las ramas.
- `git checkout nombre-rama`: cambia de rama.

---

## 5) Consejos finales

- Usa Git desde el principio, aunque sea un proyecto pequeño.
- Haz commits frecuentes con mensajes claros.
- Siempre trabaja en ramas, no en `main`.
- Si te pierdes, pregunta a alguien o busca en Google.

---

Si quieres, puedo añadir ejemplos extra o resolver dudas sobre Git.
