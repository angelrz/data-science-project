# Proyecto Ciencia de Datos en la Toma de Decisiones en las Organizaciones

## Requisitos

- Linux: Python 3.10
- Windows: Python 3.12 - 3.14
- Git
- VS Code con soporte de Jupyter, o Jupyter Notebook/Lab instalado localmente

## Clonar y preparar en Linux

```bash
git clone https://github.com/angelrz/data-science-project.git
cd data-science-project/

py -m venv venv
source env/bin/activate

python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

## Configurar el entorno en Windows

### Clonar el repositorio (CMD por defecto)

```cmd
git clone https://github.com/angelrz/data-science-project.git
cd data-science-project/
```

### 1. Crear el nuevo entorno virtual (CMD por defecto)

```cmd
py -m venv venv
```

### 2. Activar el entorno (CMD por defecto)

```cmd
.\venv\Scripts\activate.bat
```

Si prefieres PowerShell, usa estas instrucciones alternativas:

```powershell
# Clonar (PowerShell alterno)
git clone https://github.com/angelrz/data-science-project.git
cd data-science-project/

# Crear entorno (PowerShell alterno)
py -m venv venv

# Activar entorno (PowerShell alterno)
.\venv\Scripts\Activate.ps1
```

Si PowerShell da error de política al activar, ejecuta una sola vez:
```powershell
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope Process
```

### 3. Instalar dependencias (válido en CMD y PowerShell)

```cmd
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
```

### 4. Desactivar el entorno virtual

Para cerrar/desactivar el entorno virtual tanto en CMD como en PowerShell, ejecuta:

```cmd
deactivate
```

> [!NOTE]
> Si `pip` intenta compilar `numpy` o `matplotlib` en Windows, recrea el entorno con una versión soportada de Python.
> El archivo `requirements.txt` ya selecciona versiones compatibles por intérprete, pero evita mezclar un entorno viejo con otra versión de Python.

## Ejecutar el notebook

### Opción 1: En VS Code

1. Abre la carpeta del proyecto en VS Code.
2. Abre `main.ipynb`.
3. Selecciona el kernel del entorno virtual `env`.
4. Ejecuta todas las celdas del notebook de arriba hacia abajo.

### Opción 2: Con Jupyter local

```bash
source env/bin/activate
jupyter notebook
```

Luego abre `main.ipynb` y ejecuta todas las celdas.

## Datos

El notebook ya está configurado para leer los archivos desde la carpeta `data/`

## Dependencias

Las librerías necesarias están listadas en `requirements.txt`.

## Notas importantes

- No instales paquetes dentro del notebook con `!pip install`; usa el archivo `requirements.txt`.
- Si VS Code marca errores de importación, verifica que el kernel activo sea el del entorno `env` y reinstala dependencias con `python -m pip install -r requirements.txt`.
- Si el notebook muestra mapas incompletos, vuelve a ejecutar desde la primera celda después de reiniciar el kernel.
