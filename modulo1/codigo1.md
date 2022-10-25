# Código ADFGVX

![Ejemplo criptoanálisis ADFGVX_2](https://user-images.githubusercontent.com/114906778/197470081-76eeea95-8e05-43a9-9e7a-f1cfda9e3ddf.png)

  Fue inventado por **Fritz Nebel**(1891-1977) en 1917. 
  
  
  Fue escogida por el Alto Mando alemán como la más segura para cifrar sus comunicaciones durante la Primera Guerra Mundial. Pero más tarde sería descifrada
  por el criptógrafo francés **Georges Painvin**.
  
  
  Las lertas ADFGVX fueron elegidas para dar nombre a líneas y columnas en la matriz de sustitución debido a que debian ser retrasmitidas por telégrafo o por radio de 
  onda corta, y en ambos casos, empleando el alfabeto Morse. En esta alfabeto las letras A,D,F,G,V,X y X son muy distintas por lo que se reducía la probabilidad de errores de transmisión.
  
  Se trata de la última cifra importante aparecida antes del desarrollo de las máquinas criptográficas. 
  
  ## Método
  
  se basaba en una tabla de 5 filas y 5 columnas. En las 25 cuadrículas (5 x 5) de esa tabla se colocaban de forma aleatoria las 26 letras del alfabeto inglés pero como hay una letra más que cuadrículas, la "I" y la "J" compartían una misma casilla.
  
  ![Tabla ADFGX_1](https://user-images.githubusercontent.com/114906778/197818141-acd7f5d6-21ee-4b92-920f-4cfcd577832c.png)
  
  Tanto el emisor como el receptor debían utilizar la misma tabla.
  
  ###EJEMPLO
  
  - En primer lugar sustituimos cada letra por su equivalente en la tabla. 

Por ejemplo la letra "E" seria "FF"

![Tabla ADFGX_2](https://user-images.githubusercontent.com/114906778/197822832-e629b11c-e3c6-4914-971b-6e8bd3004970.png)

Si ciframos la palabra Sandra seria: 
  
  |Texto a cifrar|    ADFGVX         |
  | ------------ | ----------------- |
  | Sandra       | GD DD GA DF DX DD |
  
  - En segundo lugar añadimos una palabra en clave para alterar el orden de las Columnas. 

  | Clave         | C L A V E|
  | ------------- | -------- |
  | Texto a cifrar| G D D D G|
  |               | A D F D X|
  |               | D D      |
  
  - En tercer lugar ordenamos alfabeticamente la palbra clave que hemos utilizado, arrastando con ella la columna completa: 

|A C E L V|
| ------- |
|D G G D D|
|F A X D D|
|  D   D  |
 
 - Y, finalmente, para obtener el texto cifrado leeríamos las columnas de izquierda a derecha y de arriba a abajo

| CLAVE |
| ----- |
| DF, GA, DG, XD, DD, DD |

Para descifrar el mensaje basta con seguir estos mismos pasos en sentido inverso. 


