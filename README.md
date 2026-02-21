#  🔐PWD Safe (Español)
Un gestor de contraseñas sencillo y seguro construido en Python con Tkinter y Cryptography. Permite generar, almacenar y gestionar contraseñas de manera local con cifrado fuerte, todo dentro de una interfaz gráfica moderna con tema oscuro.

## Características

* 🔑 **Almacenamiento seguro**: Las contraseñas se cifran usando `Fernet` y una clave derivada de la contraseña maestra.
* 🖥️ **Interfaz gráfica amigable**: Basada en **Tkinter**, con soporte para tema oscuro.
* 🔄 **Gestión de contraseñas**: Guardar, editar, eliminar y buscar entradas.
* 🎯 **Generador de contraseñas**: Crea contraseñas fuertes y aleatorias.
* 📋 **Copiar al portapapeles con temporizador**: Copia usuario o contraseña y se elimina automáticamente después de 20 segundos.
* 🔒 **Bloqueo de aplicación**: Bloquea la app manual o automáticamente tras 5 minutos de inactividad.
* 🗂️ **Local storage**: Las contraseñas se guardan localmente en archivos cifrados (`pw.enc`).


## Requisitos

* Python 3.8 o superior
* Paquetes:

```bash
pip install cryptography
```

> Tkinter viene incluido con la mayoría de instalaciones de Python.


## Instalación

1. Clona el repositorio:

```bash
git clone https://github.com/tuusuario/password-manager.git
cd password-manager
```

2. Instala las dependencias:

```bash
pip install cryptography
```

## Uso

Ejecuta la aplicación:

```bash
python main.py
```

1. Ingresa tu **contraseña maestra**.

   * Si es la primera vez, se creará un archivo `salt.bin` para derivar la clave de cifrado.
2. Guarda nuevas contraseñas indicando **Sitio**, **Usuario** y **Contraseña**.
3. Genera contraseñas seguras con el botón **Generate password**.
4. Consulta, edita o elimina entradas desde la ventana **View saved**.
5. Copia usuario o contraseña al portapapeles con auto-borrado de 20 segundos.
6. Bloquea la aplicación con el botón 🔒 o automáticamente tras 5 minutos.


## Archivos

* `pw.json` → Archivo temporal con datos descifrados (se borra al cifrar).
* `pw.enc` → Archivo cifrado que almacena todas las contraseñas.
* `salt.bin` → Salt aleatoria usada para derivar la clave desde la contraseña maestra.


## Seguridad

* Las contraseñas nunca se almacenan en texto plano.
* Se usa `PBKDF2HMAC` con SHA256 y 390,000 iteraciones para derivar la clave de cifrado.
* Los datos solo se descifran en memoria durante la sesión de la app.


## Capturas de pantalla


<img width="582" height="327" alt="image" src="https://github.com/user-attachments/assets/eb5256b0-9066-4e0b-a588-9c7213cad3e5" />

<img width="1650" height="850" alt="image" src="https://github.com/user-attachments/assets/cca80402-34a8-4c6d-88e9-83134bb598ee" />

<img width="996" height="742" alt="image" src="https://github.com/user-attachments/assets/2b7fbbcf-9fed-41b2-a862-aa037e0b8c21" />

<img width="543" height="314" alt="image" src="https://github.com/user-attachments/assets/5b9abffe-f628-4e5f-a91b-d340acfbfd04" />


## Licencia

Este proyecto está bajo la licencia Apache 2.0 .
Cualquier uso personal y educativo es bienvenido.
