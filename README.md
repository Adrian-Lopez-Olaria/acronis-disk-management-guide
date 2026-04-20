# 🖥️ Acronis Disk Management Guide (Backup · Restore · Clone · Tools)

## 📑 Índice

1. [Introducción y punto de partida](#-1-introducción-y-punto-de-partida)  
2. [Proceso de backup (copia de seguridad)](#-2-proceso-de-backup-copia-de-seguridad)  
3. [Evidencia del backup generado](#-3-evidencia-del-backup-generado)  
4. [Restauración del sistema](#-4-restauración-del-sistema)  
5. [Clonado de disco](#-5-clonado-de-disco)  
6. [Herramientas adicionales: borrado seguro](#-6-herramientas-adicionales-borrado-seguro)  
7. [Notas importantes](#-7-notas-importantes)  
8. [Aviso legal / responsabilidad](#-8-aviso-legal--responsabilidad)  

---

## 📌 1. Introducción y punto de partida

En esta guía se documenta el uso de **Acronis True Image** para realizar operaciones completas sobre discos: copia de seguridad, restauración, clonación y borrado seguro.

Todo el proceso se realiza mediante un **USB booteable**, lo que permite trabajar fuera del sistema operativo y garantizar la integridad de los datos.

Antes de comenzar, es importante comprobar el estado de los discos desde el sistema.

En la siguiente imagen se puede observar la estructura inicial, donde contamos con un disco principal con el sistema operativo y un segundo disco que utilizaremos como destino del backup:

![Estado discos](assets/CAPTURA1.png)

Una vez verificado esto, reiniciamos el equipo y arrancamos desde el USB de Acronis. En el menú de arranque seleccionamos la opción correspondiente para iniciar la herramienta:

![Boot](assets/CAPTURA2.png)

---

## 💾 2. Proceso de backup (copia de seguridad)

Una vez dentro del entorno de Acronis, accedemos a la opción de copia de seguridad desde el menú principal.

En la siguiente imagen se muestra la pantalla inicial donde seleccionamos **Backup → My Disks** para comenzar:

![Inicio](assets/CAPTURA3.png)

A continuación, debemos seleccionar el disco completo que queremos respaldar. Es importante incluir todas las particiones necesarias para el arranque del sistema.

Tal y como se observa en la imagen, seleccionamos la partición EFI, la unidad principal (C:) y la partición de recuperación:

![Particiones](assets/CAPTURA4.png)

El siguiente paso consiste en elegir dónde se guardará la copia de seguridad. Para ello, pulsamos en la opción de exploración y seleccionamos el disco destino:

![Ubicación](assets/CAPTURA5.png)

Después, definimos la ruta y el nombre del archivo de backup. En este caso, se guarda como `E:\Micopia.tibx`:

![Ruta](assets/CAPTURA6.png)

Una vez definida la ubicación, confirmamos que todo es correcto antes de continuar:

![Confirmación](assets/CAPTURA7.png)

Antes de ejecutar el proceso, Acronis muestra un resumen con toda la información de la copia que se va a realizar. Es recomendable revisarlo para evitar errores:

![Resumen](assets/CAPTURA8.png)

Finalmente, iniciamos el backup. Durante este proceso se copiarán todos los datos del sistema al archivo `.tibx`:

![Progreso](assets/CAPTURA9.png)

---

## 📂 3. Evidencia del backup generado

Una vez finalizado el proceso, podemos comprobar que el archivo de copia se ha generado correctamente en el disco destino.

En la siguiente imagen se muestra el archivo `.tibx` ya creado:

![TIBX](assets/CAPTURA10.png)

Este archivo contiene la imagen completa del sistema y será utilizado en procesos de restauración o migración.

---

## 🔄 4. Restauración del sistema

Para restaurar el sistema, accedemos a la opción de recuperación desde el menú principal de Acronis:

![Recovery](assets/CAPTURA14.png)

A continuación, seleccionamos el archivo de backup que queremos utilizar. En este caso, elegimos el archivo previamente creado:

![Seleccion backup](assets/CAPTURA15.png)

Después, indicamos el método de restauración. Para recuperar el sistema completo, seleccionamos la opción de restaurar discos y particiones completas:

![Método](assets/CAPTURA16.png)

En el siguiente paso, seleccionamos el punto de restauración. Esto permite elegir el momento exacto del backup si existen varias copias.

A continuación, seleccionamos qué elementos queremos restaurar, asegurándonos de incluir todas las particiones necesarias:

![Contenido](assets/CAPTURA18.png)

Por último, elegimos el disco destino donde se aplicará la restauración. Este paso es crítico, ya que se sobrescribirán todos los datos existentes en dicho disco:

![Destino](assets/CAPTURA19.png)

---

## 🔁 5. Clonado de disco

Acronis también permite clonar discos completos de forma directa.

Para ello, accedemos a la opción correspondiente desde el apartado de herramientas:

![Clone](assets/CAPTURA20.png)

Primero seleccionamos el disco de origen, que será el que contiene el sistema actual:

![Origen](assets/CAPTURA21.png)

Después, seleccionamos el disco de destino donde se copiarán los datos:

![Destino](assets/CAPTURA22.png)

A continuación, elegimos el tipo de clonación. En este caso, se selecciona la opción de reemplazar el disco en la misma máquina:

![Método](assets/CAPTURA23.png)

Finalmente, se muestra un resumen con los cambios que se aplicarán antes de ejecutar el proceso:

![Resumen](assets/CAPTURA24.png)

---

## 🧹 6. Herramientas adicionales: borrado seguro

Acronis incluye herramientas avanzadas para la eliminación segura de datos.

Desde el menú de herramientas accedemos a **DriveCleanser**, que permite borrar discos de forma irreversible:

![Tools](assets/CAPTURA11.png)

Seleccionamos el disco o partición que queremos limpiar:

![Disco](assets/CAPTURA12.png)

A continuación, elegimos el algoritmo de borrado. Cada uno ofrece distintos niveles de seguridad:

![Algoritmos](assets/CAPTURA13.png)

Algunos de los más utilizados son:

- **DoD 5220.22-M** → estándar militar con múltiples sobrescrituras  
- **Gutmann** → máximo nivel de seguridad (muy lento)  
- **Schneier** → equilibrio entre seguridad y rendimiento  
- **GOST** → estándar ruso  
- **VSITR** → estándar alemán  
- **Fast** → borrado rápido (menos seguro)  

Este tipo de borrado es útil para eliminar información sensible de forma definitiva.

---

## 🧠 7. Notas importantes

- No interrumpir ningún proceso en ejecución  
- Verificar correctamente los discos antes de operar  
- Backup, restauración y clonación sobrescriben datos  
- Incluir siempre particiones EFI y Recovery  
- SSD mejora considerablemente el rendimiento  

---

## ⚖️ 8. Aviso legal / responsabilidad

Este procedimiento ha sido realizado utilizando una **licencia oficial de Acronis True Image**.

La información proporcionada en este documento tiene fines **educativos y técnicos**.

El uso incorrecto de estas herramientas puede provocar:
- Pérdida de datos  
- Sobrescritura de discos  
- Fallos en sistemas  

El autor no se hace responsable del uso indebido de esta información.

Se recomienda realizar pruebas en entornos controlados antes de su uso en producción.

---

## 📦 Resultado final

Mediante este procedimiento se obtiene:

- Copia completa del sistema  
- Restauración funcional  
- Clonado de discos  
- Eliminación segura de datos  

Todo ello desde un entorno booteable con Acronis.
