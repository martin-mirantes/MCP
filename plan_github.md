# Plan Detallado para Configurar `.gitignore` e Inicializar Repositorio de GitHub para un Proyecto Python

**Fase 1: Creación del archivo `.gitignore` para Python**

1.  **Contenido del `.gitignore` (a crear en modo Code):**
    ```gitignore
    # Python
    __pycache__/
    *.py[cod]
    *$py.class
    *.so
    .Python
    build/
    develop-eggs/
    dist/
    downloads/
    eggs/
    .eggs/
    lib/
    lib60/
    parts/
    sdist/
    var/
    wheels/
    pip-wheel-metadata/
    share/python-wheels/
    *.egg-info/
    .installed.cfg
    *.egg
    MANIFEST

    # Virtualenv
    .env
    .venv
    env/
    venv/
    ENV/
    env.bak/
    venv.bak/

    # Databases
    *.sqlite3
    *.sqlite3-journal

    # IDEs and editors
    .idea/
    # .vscode/  (Comentado por si prefieres versionar la configuración de VSCode)
    *.swp
    *~
    *.sublime-project
    *.sublime-workspace

    # Logs and Cache
    *.log
    .cache/
    htmlcov/
    .tox/
    .nox/
    .coverage
    .coverage.*
    .pytest_cache/

    # Jupyter Notebook
    .ipynb_checkpoints

    # Secrets (example, adjust as needed)
    # local_settings.py
    # secrets.json
    ```
2.  **Acción (en modo Code):** Escribir este contenido en un archivo llamado `.gitignore` en la raíz del proyecto (`/home/martp/supabase`).

**Fase 2: Inicialización del Repositorio Git Local (en modo Code)**

1.  **Acciones (en modo Code):** Ejecutar los siguientes comandos en la terminal, en el directorio raíz del proyecto:
    *   `git init`
    *   `git add .gitignore` (una vez creado)
    *   `git add .`
    *   `git commit -m "Initial commit con .gitignore para Python"`

**Fase 3: Guía para la Creación del Repositorio en GitHub**

1.  **Instrucciones para el usuario:**
    *   Ve a [https://github.com/new](https://github.com/new).
    *   Ingresa un nombre para tu repositorio (por ejemplo, el nombre de tu proyecto).
    *   Opcionalmente, añade una descripción.
    *   Asegúrate de que esté seleccionado "Público" o "Privado" según tu preferencia.
    *   **Importante:** NO selecciones "Initialize this repository with a README", "Add .gitignore", o "Choose a license" en esta etapa, ya que estamos configurando esto localmente.
    *   Haz clic en "Create repository".
    *   Una vez creado, GitHub te mostrará una página con la URL de tu nuevo repositorio. Será algo como `https://github.com/tu-usuario/tu-repositorio.git`. Copia esta URL.

**Fase 4: Conexión y Subida al Repositorio de GitHub (en modo Code)**

1.  **Acciones (en modo Code, después de que el usuario proporcione la URL):** Ejecutar los siguientes comandos en la terminal:
    *   `git remote add origin URL_DEL_REPOSITORIO_COPIADA_DE_GITHUB`
    *   `git branch -M main` (para asegurar que la rama principal se llame `main`)
    *   `git push -u origin main` (para subir tus archivos a GitHub)

**Diagrama del Flujo (Mermaid):**

```mermaid
graph TD
    A[Inicio: Solicitud del usuario] --> B[Definir .gitignore para Python];
    B --> C[Escribir archivo .gitignore (Modo Code)];
    C --> D[Ejecutar: git init (Modo Code)];
    D --> E[Ejecutar: git add .gitignore (Modo Code)];
    E --> F[Ejecutar: git add . (Modo Code)];
    F --> G[Ejecutar: git commit -m "Initial commit..." (Modo Code)];
    G --> H[Instruir al usuario para crear repo en GitHub y obtener URL];
    H --> I{Usuario proporciona URL del repo};
    I --> J[Ejecutar: git remote add origin <URL> (Modo Code)];
    J --> K[Ejecutar: git branch -M main (Modo Code)];
    K --> L[Ejecutar: git push -u origin main (Modo Code)];
    L --> M[Fin: Proyecto en GitHub con .gitignore];