======== INSTALACION ========

Requerimientos:

- Cmake (X)
- glad (X)
- glfw (X)
- Visual Studio & Compilador de C++ (X)

[ Ya estan instalados en la carpeta "OpenGL Libs" ]

=== Como instalarlo? ===

- Abrir Visual Studio, es importante para conseguir todo funcionando.
- Crear un nuevo proyecto. (Un proyecto vacio de C++)
- Crear una carpeta en el proyecto, que se llame "Libraries" (o puedes ponerle cualquier nombre)
- Crear 2 carpetas mas, una llamada "include" y otra "lib"
- Extraer el .zip de glfw que se encuentra en la carpeta "OpenGL Libs"
- Abrir CMake.

## Configuraciones de CMake ##

- Seleccionar la carpeta extraida de glfw en el parametro de el codigo fuente.
- Crear dentro de la carpeta extraida de glfw una carpeta llamada "build" y seleccionarla en el parametro de compilacion de archivos binarios.
- Tocar el boton "Configure".

ATENCION: fijese que los parametros insertados sean los siguientes:
-------- Parametros --------
- Visual Studio 16 2019 (En el generador del proyecto)
- Usar compiladores nativos predeterminados
----------------------------

- Tocar en "finish"
- Tocar en "configure" otra vez
- Tocar en "generate" y cuando termine, cerrar CMake.

## Compilar GLFW ##

- Abrir la carpeta "build" dentro de glfw y abrir el archivo GLFW.sln
- Compilar la solucion de GLFW

## Copiar Bibliotecas ##

- Abrir "glfw", de ahi abrir "build", despues "src", despues "Debug".
- Cortar "glfw3.lib" y pegar en la carpeta "lib" de tu proyecto (IMPORTANTE)

- En la carpeta principal de glfw, abrir la carpeta "include" y cortar y pegar la carpeta GLFW en tu carpeta "include" de tu proyecto

## Configurar Glad ##

- Abrir glad.zip y abrir "include"
- Copiar las 2 carpetas (glad, KHR) en la carpeta "include" de tu proyecto.
- Despues, en la carpeta principal de glad, abrir "src" y copiar el archivo glad.c en la carpeta PRINCIPAL de tu proyecto.

=== Como configurar Visual Studio ===

- En la imagen adjunta se vera como debe estar configurado ( En los parametros tapados, colocar la carpeta de inclusion y librerias de tu proyecto)
![Image](https://github.com/HankB-o-t/opengl-setup-libs/blob/main/Properties.PNG)

- Despues, en Vinculador/Linker y en Entrada/Input, añadir estas 2 librerias:

glfw3.lib
opengl32.lib

- ULTIMO PASO: agarrar el archivo glad.c de tu proyecto y agregarlo en los archivos de origen de tu proyecto.

