# Adquisición en vivo de una máquina windows (Memoria Volatil y no volatil)

![Portada](./Imagenes/Portada.png)

**Autor:** Sergio Guerrero Merlo
## Índice

1. [Introducción](#introducción)
2. [Adquisición de evidencias](#adquisicion-de-evidencias)
3. [Triage](#triage)
4. [Adquisición de memoria RAM](#adquisición-de-memoria-RAM)
5. [Adquisición de una imagen del disco duro](#adquisición-de-una-imagen-del-disco-duro)
6. [Conclusión](#conclusión)


## Introducción

En este trabajo pretendemos aprender a utilizar varias herramientas de adquisición de evidencias digitales y de triage para poder obtener en experiencia sobre este tipo de proceso. La idea de este trabajo es adquirir una imagen de la memoria Ram de una máquina Windows y de su disco duro además de obtener información con el proceso de Triage.

## Adquisición de evidencias

Se nos pide la adquisición en vivo de memoria volátil y no volátil, siguiendo la metodología que hemos creado en un trabajo anterior en grupo, vamos a seguir el orden de volatilidad siguiente para ejecutar esta adquisición.

- 1. Registros, caché.
- 2. Tablas de enrutamientos, caché ARP, tabla de procesos, estadísticas del núcleo y memoria.
- 3. Sistemas de archivos temporales.
- 4. Disco duro.
 - 5. Datos de registro remoto (logs del sistema) y monitorización del sistema relevante en cuestión.
- 6. Configuración física y topología de la red.
- 7. Documentos y archivos.

Siguiendo este orden de volatilidad, primero sacaremos una imagen de la Ram y por último una imagen del disco duro de la máquina Windows.

## Triage

Según varias fuentes en internet, el Triage puede hacerse antes o después de la adquisición, en mi caso, lo haré antes.

Para hacer triaje voy a utilizar la herramienta IR Triage para sacar información como los registro y caché entre otros. La he ejecutado desde el disco duro externo para no sobrescribir posible información borrada en el disco duro. 

Lo primero que he hecho es rellenar el log del caso.

![1](./Imagenes/1.png)

Dejo marcado todo en cada categoría para hacer la recopilación tanto de los registros del sistema como información de la red. 

![2](./Imagenes/2.png)

He clicado en Run y esperado a que termine de hacer el Triaje. 

![3](./Imagenes/3.png)

He comprobado que la información ha sido adquirida de forma correcta y la he guardado en el disco duro externo.

![4](./Imagenes/4.png)

## Adquisición de memoria RAM

Después de hacer triage, voy a sacar una imagen de la memoria RAM utilizando el programa Belkasoft Live Ram Capturer. He especificado donde quiero que me guarda la imagen de la Ram  que será en el disco duro externo y dado clic en capture.

![5](./Imagenes/5.png)

Una vez clicado, he esperado a que termine para poder comprobar que se ha guardado la imagen de manera correcta en el disco duro externo.

![6](./Imagenes/6.png)

![7](./Imagenes/7.png)

## Adquisición de una imagen del disco duro

En esta parte del trabajo, sacaré una imagen completa del disco duro de la máquina con FTK Imager. Esta imagen la guardaré al igual que con el Triaje y la imagen de memoria Ram en el disco duro externo que he preparado con antelación para ello.

Lo primero que he hecho es clicar sobre File y dar en la opción de crear una imagen. Luego he marcado la opción de disco duro físico y he seleccionado el disco duro virtual donde está instalada la máquina.

![8](./Imagenes/8.png)

Después he especificado como formato para sacar la imagen AFF y rellenado la información referente a nuestro caso al igual que hice en IR Triage. 

He seleccionado la ruta de destino el disco duro externo y he fragmentado la imagen en partes de 3000MB. Como podemos ver en la imagen, he marcado las casillas para verificar después de la ejecución de este proceso que sea ha creado y la casilla de precálculo del progreso.

![9](./Imagenes/9.png)
Una vez terminada la adquisición,  he comprobado el resumen del proceso de creación de imagen.

![10](./Imagenes/10.png)

![11](./Imagenes/11.png)
## Conclusión

Después de haber hecho esta tarea, me ha quedado algo más claro este proceso de adquisición de evidencias digitales. He aprendido a utilizar varias herramientas para la fase de adquisición y para el triage.  Además he aprendido la importancia de mantener la información adquirida fuera de la máquina sobre la que estamos realizando este proceso para salvaguardar la integridad de la información que contiene.
