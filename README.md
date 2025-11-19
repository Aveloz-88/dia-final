# Publicar el sitio

Este repositorio contiene una página estática `index.html` (junto con recursos locales). Para hacerla pública y accesible desde cualquier dispositivo puedes usar GitHub Pages. A continuación están las instrucciones rápidas y un workflow de GitHub Actions ya incluido para desplegar automáticamente al hacer push al repositorio.

Pasos mínimos (GitHub Pages):

1. Crea un repositorio nuevo en GitHub (público o privado según prefieras).
2. En tu máquina, inicializa git y sube los archivos:

```powershell
cd "C:\Users\Admin\Desktop\proyecto"
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/<TU_USUARIO>/<TU_REPO>.git
git push -u origin main
```

3. En GitHub, ve a `Settings > Pages` y activa GitHub Pages si no se activa automáticamente. Cuando uses el workflow incluido, GitHub Pages publicará desde la rama `gh-pages` gestionada por Actions.

4. Espera unos minutos después del primer push: tu sitio estará disponible en `https://<TU_USUARIO>.github.io/<TU_REPO>/`.

Despliegue automático (workflow):
- He incluido un workflow de GitHub Actions (`.github/workflows/pages.yml`) que construye y publica los artefactos al branch de Pages cuando hagas push a `main`.

Alternativa rápida (Netlify):
- Puedes arrastrar y soltar la carpeta `proyecto` en https://app.netlify.com/drop para publicar inmediatamente sin necesidad de git.

Si quieres, puedo generar también un archivo `CNAME` para un dominio personalizado si ya lo tienes.

Si quieres que haga el push por ti necesitaré acceso a tu cuenta o un repo vacío al que pueda subir, pero por razones de seguridad esto lo harás tú con los pasos anteriores.

Dime si quieres que:
- Reemplace `https://example.com` en la navegación por la URL real una vez publicada, o
- Genere también un `CNAME` (si tienes dominio propio).

---
Autor: Erick X. Veloz
