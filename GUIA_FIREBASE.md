# Conectar Hexamove a Firebase (10 minutos, gratis)

1. Entra a https://console.firebase.google.com con tu cuenta Google → **Crear un proyecto** → nombre `hexamove` (puedes desactivar Analytics).
2. **Build → Authentication → Comenzar → Anonymous (Anónimo) → Habilitar → Guardar.**
3. **Build → Firestore Database → Crear base de datos** → ubicación `southamerica-east1` (São Paulo) → modo **producción** → Habilitar.
4. En Firestore → pestaña **Reglas** → borra todo, pega el contenido de `firestore.rules` → **Publicar**.
5. Ícono de engranaje → **Configuración del proyecto** → baja a "Tus apps" → ícono web `</>` → registra la app (nombre `hexamove-web`, sin Hosting) → copia el bloque `firebaseConfig`.
6. Abre `firebase-config.js`, reemplaza `window.HEXA_FB = null;` por `window.HEXA_FB = { ...lo que copiaste... };`.
7. En tu repo de GitHub, sube `index.html` y `firebase-config.js` (Add file → Upload files). Espera 1–2 min.

Dónde ver los datos del proyecto: Firebase → Firestore → colección `usuarios` (un documento por persona con todo su avance) y `ranking` (puntos por semana).
