Aplicación de Mensajería SMTP con Tkinter

Una aplicación de escritorio desarrollada en Python utilizando **Tkinter** que permite enviar correos electrónicos de Gmail de forma sencilla y con una interfaz visual completamente renovada.

---

¿Qué cambió en la versión nueva?

Se realizó una refactorización integral del código original para corregir fallos técnicos de ejecución, mejorar la seguridad y darle una apariencia visual mucho más moderna y cuidada :D

---

 Errores corregidos respecto al código anterior

1. Rutas absolutas de imágenes rígidas
   * Antes: El código buscaba la imagen en una ruta fija local (`D:/EIGHTA/...`), lo que hacía que el programa fallara en cualquier otra computadora.
   * Ahora: Se utiliza una **ruta relativa** con un bloque `try...except` de seguridad. Si la imagen no está disponible, la app sigue funcionando mostrando un icono decorativo alternativo.

2. Fallo de autenticación con Gmail
   * Antes: Se intentaba conectar usando un texto plano ficticio (`"clave-personal"`).
   * Ahora: Se estructuró la variable para utilizar **Contraseñas de Aplicación de Google**, garantizando la conexión segura con el servidor SMTP.

3. Falta de manejo de excepciones
   * Antes: Si fallaba el envío o no había internet, el programa se cerraba abruptamente en la consola.
   * Ahora: Se capturan los errores (`smtplib.SMTPAuthenticationError` y excepciones generales) mostrando ventanas emergentes informativas (`messagebox`).

4. Envío sin validación
   * Antes: Se podía presionar el botón "Enviar" con el destinatario vacío.
   * Ahora: Se valida que el destinatario contenga una dirección válida antes de iniciar la conexión al servidor.

---

 Nuevas Funcionalidades

* Agenda de Contactos (`OptionMenu`): Menú desplegable con una lista de correos predefinidos. Al seleccionar un contacto, el campo de destinatario se autocompleta automáticamente.
* Mensajes de Alerta Claros: Notificaciones visuales para confirmar envíos exitosos o alertar sobre errores de contraseña o campos vacíos.
* Código más limpio: Se eliminaron las cadenas sueltas como comentarios y se normalizó la sintaxis estándar de Python (`#`).

---
 
 Cambios Estéticos y de Diseño

La interfaz gráfica fue rediseñada por completo pasando de un diseño básico a un estilo visual moderno y estilizado (*estética pastel / coquette*):

*  Paleta de Colores Armónica: Se definieron variables globales para los colores (`#fff0f3` para el fondo, `#ffb3c6` para acentos rosados y `#785964` para textos).
*  Dimensiones Ampliadas: Se expandió el tamaño de la ventana de `335x385` a `390x590` para evitar que los elementos se encimaran.
* Tipografía Renovada: Se reemplazó la fuente *Arial* por *Helvetica*, ajustando los pesos y tamaños para una jerarquía visual más clara.
*  Campos y Botones Estilizados:
  * Entradas de texto con color de fondo personalizado, bordes finos y relleno interno (`ipady`).
  * Tarjeta decorativa (`Frame`) para mostrar el correo del remitente.
  * Botón de envío rediseñado con cursor interactivo de mano (`cursor="hand2"`).

---

Requisitos e Instalación

1. Requisitos: Tener instalado Python 3.8 o superior.
2. Dependencias: Instalar la librería `Pillow` para la gestión de imágenes

Interfaz gráfica principal: <img width="490" height="685" alt="Interfaz grafica principal" src="https://github.com/user-attachments/assets/183a2a2e-6765-47a6-a9a0-2e5feab158a9" />


Resultado: <img width="612" height="295" alt="resultado" src="https://github.com/user-attachments/assets/6aac9b40-2d7d-491b-b628-b3c7488f1fff" />

