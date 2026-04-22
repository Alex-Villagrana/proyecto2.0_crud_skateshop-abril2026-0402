¡Excelente elección! Integrar Firebase con Flutter ha mejorado muchísimo gracias a la **CLI de FlutterFire**, pero todo comienza con tener las herramientas de base bien configuradas.

Aquí tienes la guía paso a paso para dejar tu entorno listo.

---

## 1. Software necesario: Node.js y NPM
Para instalar Firebase CLI, necesitas **Node.js**, el cual incluye automáticamente **NPM** (Node Package Manager).

### Cómo verificar si ya lo tienes
Abre tu terminal (PowerShell, CMD o Terminal de macOS/Linux) y escribe:
* `node -v`
* `npm -v`

> **¿Qué versión utilizar?** Se recomienda siempre la versión **LTS (Long Term Support)**. Actualmente, cualquier versión superior a la **18.x** o **20.x** funcionará perfectamente.

### Si no está instalado: Paso a paso
1.  **Descarga:** Ve al sitio oficial [nodejs.org](https://nodejs.org/).
2.  **Instalador:** Elige el instalador **LTS** para tu sistema operativo.
3.  **Instalación:** Ejecuta el archivo. **Importante:** Asegúrate de marcar la casilla que dice *"Automatically install the necessary tools"* o la que menciona agregar Node al **PATH**.
4.  **Reinicio:** Una vez finalizado, cierra y vuelve a abrir tu terminal para que reconozca los cambios.

---

## 2. Instalación de Firebase CLI (Global)
Una vez que tienes NPM, instalar las herramientas de Firebase es un solo comando. El parámetro `-g` indica que la instalación es **global**, permitiéndote usar los comandos en cualquier carpeta.

Escribe en tu terminal:
```bash
npm install -g firebase-tools
```

---

## 3. Comandos esenciales de Firebase

### Acceder con tu cuenta de Google
Para vincular tu terminal con tu consola de Firebase, usa:
```bash
firebase login
```
* Esto abrirá una ventana en tu navegador.
* Selecciona tu cuenta de Google y otorga los permisos.
* Si ya estabas logueado y quieres cambiar de cuenta, usa `firebase logout` primero.

### Cómo usar `firebase-tools`
Las herramientas de Firebase te permiten gestionar tus proyectos desde la consola. Algunos comandos clave son:

* **Listar proyectos:** `firebase projects:list` (Muestra todos tus proyectos en la consola).
* **Ayuda:** `firebase --help` (Si te pierdes con algún comando).

---

## 4. El "Toque Especial" para Flutter: FlutterFire CLI
Aunque preguntaste por Firebase CLI, para Flutter el estándar actual es usar **FlutterFire CLI**, que configura automáticamente los archivos `google-services.json` y `GoogleService-Info.plist`.

1.  **Instala la CLI de FlutterFire** (requiere tener Dart instalado):
    ```bash
    dart pub global activate flutterfire_cli
    ```
2.  **Configura tu App:** Dentro de la carpeta raíz de tu proyecto Flutter, ejecuta:
    ```bash
    flutterfire configure
    ```
    *Esto te pedirá seleccionar tu proyecto de Firebase y las plataformas (iOS, Android, Web) que quieres configurar.*

---

## Resumen de Comandos Rápidos

| Acción | Comando |
| :--- | :--- |
| **Instalar Firebase CLI** | `npm install -g firebase-tools` |
| **Iniciar sesión** | `firebase login` |
| **Verificar versión NPM** | `npm -v` |
| **Configurar Flutter** | `flutterfire configure` |

¿Ya tienes creado tu proyecto en la consola de Firebase o prefieres que te explique cómo crearlo desde la terminal?
