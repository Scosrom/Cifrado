# Código AES
 
**Advanced Encryption Standard (AES)**, también conocido como "*Rijndael*", es un esquema de cifrado por bloques adoptado como un estándar de cifrado por el gobierno de los "Estados Unidos", creado en Bélgica. Desde 2006, el ***AES*** es uno de los algoritmos más populares usados en criptografía simétrica.

## Trayectoria

El cifrado fue desarrollado por dos criptólogos belgas, [***Joan Daemen***](joanDaemen.md) y [***Vincent Rijmen***](vicent.md), ambos estudiantes de la "**Katholieke Universiteit Leuven**", y fue enviado al proceso de selección ***AES*** bajo el nombre "*Rijndael*", como parte de un concurso, de donde fueron los más votados tras varias [*conferencias*](condyConfe.md), que se realizaron a lo largo de 3 años que duró el proyecto de selección creado por el *Instituto Nacional de Normas y Tecnología (NIST)*. El cuál realizó este concurso comenzando en 1997 para escoger un algoritmo de cifrado capaz de proteger información sensible durante el siglo XXI.

## Descripción del cifrado

Estrictamente hablando, AES no es precisamente Rijndael (aunque en la práctica se los llama de manera indistinta) ya que Rijndael permite un mayor rango de tamaño de bloques y longitud de claves; AES tiene un tamaño de bloque fijo de 128 bits y tamaños de llave de 128, 192 o 256 bits, mientras que Rijndael puede ser especificado por una clave que sea múltiplo de 32 bits, con un mínimo de 128 bits y un máximo de 256 bits.

La mayoría de los cálculos del algoritmo AES se hacen en un campo finito determinado.

AES opera en una matriz de 4×4 bytes, llamada state (algunas versiones de Rijndael con un tamaño de bloque mayor tienen columnas adicionales en el state).

## Pseudocódigo

- Expansión de la clave usando el esquema de claves de Rijndael.
- Etapa inicial:
  
  **1.- AddRoundKey**
  
- Rondas:

  **1.- SubBytes:**  en este paso se realiza una sustitución no lineal donde cada byte es reemplazado con otro de acuerdo a una tabla de búsqueda.
  
  ![image](subBytes.png)
  
  **2.- ShiftRows:**  en este paso se realiza una transposición donde cada fila del «state» es rotada de manera cíclica un número determinado de veces.
  
  ![image](shiftRowa.png)
  
  **3.- MixColumns:**  operación de mezclado que opera en las columnas del «state», combinando los cuatro bytes en cada columna usando una transformación lineal.
  
  ![image](mixColumns.png)
  
  **4.- AddRoundKey:**  cada byte del «state» es combinado con la clave «round»; cada clave «round» se deriva de la clave de cifrado usando una iteración de la clave.
  
  ![image](addRoundkey.png)

- Etapa final:

  **1.- SubBytes**
  
  **2.- ShiftRows**
  
  **3.- AddRoundKey**
  
## Seguridad
  
Los criptógrafos están constantemente investigando AES en busca de debilidades, tratando de encontrar nuevas técnicas y aprovechando la tecnología que se les presenta. Esto es esencial, porque si los académicos no lo probaron a fondo, los delincuentes o los estados nacionales podrían encontrar una manera de descifrarlo sin que el resto del mundo lo supiera. Hasta ahora, los investigadores solo han descubierto rupturas teóricas y ataques de canal lateral.

Hasta el momento no se han registrado ataques exitosos conocidos en la vida real, sin embargo, la rápida evolución de la tecnología podría plantear amenazas potenciales en el futuro.

## Ejemplos de su uso

- VPN (Redes Privadas Virtuales)
- WIFI
- Aplicaciones móviles
- Herramientas de archivo y compresión
- Componentes del sistema operativo
- Bibliotecas de lenguajes de programación
- Administradores de contraseñas
