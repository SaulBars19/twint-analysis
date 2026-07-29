# Cómo publicar este análisis desde VS Code

## 1. Prepara Git

Abre la carpeta del proyecto en VS Code y luego abre una terminal integrada:

```bash
git --version
```

Si Git está instalado, verás su número de versión.

Configura tu identidad únicamente si todavía no lo has hecho:

```bash
git config --global user.name "Saul Barrientos"
git config --global user.email "TU_EMAIL_DE_GITHUB"
```

## 2. Crea el repositorio en GitHub

En GitHub:

1. Haz clic en **New repository**.
2. Usa un nombre como `twint-analysis`.
3. Añade una descripción, por ejemplo:
   `Interactive fundamental and strategic analysis of TWINT AG.`
4. Selecciona **Public**.
5. No añadas README, licencia ni `.gitignore`, porque ya están incluidos aquí.
6. Crea el repositorio.

## 3. Sube el proyecto desde VS Code

Desde la terminal integrada, dentro de esta carpeta:

```bash
git init
git add .
git commit -m "Publish TWINT fundamental and strategic analysis"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/twint-analysis.git
git push -u origin main
```

Sustituye `TU_USUARIO` por tu nombre de usuario real de GitHub.

## 4. Activa GitHub Pages

En tu repositorio de GitHub:

1. Abre **Settings**.
2. Entra en **Pages**.
3. En **Build and deployment**, selecciona **Deploy from a branch**.
4. Selecciona la rama `main`.
5. Selecciona la carpeta `/ (root)`.
6. Guarda los cambios.

La dirección tendrá normalmente esta estructura:

```text
https://TU_USUARIO.github.io/twint-analysis/
```

## 5. Actualiza el enlace del README

En `README.md`, reemplaza:

```text
https://<your-github-username>.github.io/twint-analysis/
```

por tu URL real. Después ejecuta:

```bash
git add README.md
git commit -m "Add live GitHub Pages link"
git push
```

## 6. Cómo subir cambios futuros

Cada vez que edites el análisis:

```bash
git add .
git commit -m "Describe brevemente el cambio"
git push
```

GitHub Pages volverá a publicar automáticamente la versión actualizada.

## Recomendaciones para que el repositorio se vea profesional

- Añade una captura del dashboard al README cuando tengas la URL definitiva.
- Usa una descripción corta y clara en la sección **About** del repositorio.
- Añade temas como `finance`, `fintech`, `payments`, `twint`, `data-analysis`, `equity-research` y `chartjs`.
- Fija el repositorio en tu perfil de GitHub.
- Comparte directamente la URL de GitHub Pages en CV, LinkedIn y candidaturas.

## Problemas frecuentes

### La página aparece en blanco

Comprueba que el archivo principal se llama exactamente `index.html` y está en la raíz del repositorio.

### Los gráficos no aparecen

El informe carga Chart.js desde internet. Verifica que el navegador tenga conexión y que ninguna extensión esté bloqueando el CDN.

### Git rechaza el push

Verifica que la URL remota sea correcta:

```bash
git remote -v
```

Para corregirla:

```bash
git remote set-url origin https://github.com/TU_USUARIO/twint-analysis.git
```
