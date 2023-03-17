#1. Descripción del problema:
Un telescopio Cherenkov o CT, es un detector de rayos gamma de muy alta energía desde la
superficie terrestre. Dichos rayos gamma no llegan hasta la superficie de la tierra, si no que
cuando llegan a la atmósfera terrestre, interactúan con ella, produciendo cascadas de
partículas subatómicas, conocidas como lluvias de aire o de partículas. Estas partículas de
energía ultra alta pueden viajar más rápido que la luz en el aire, creando un destello azul,
conocido como "luz Cherenkov", similar al boom sónico generado por un avión que excede la
velocidad del sonido. Aunque la luz se extiende sobre un área grande (250 m de diámetro), la
cascada solo dura unas mil millonésimas de segundo, la cual es demasiado débil para ser
detectada por el ojo humano, pero no demasiado débil para un CT.
El telescopio está formado por un gran espejo segmentado que enfoca la radiación de
Cherenkov en una matriz de tubos fotomultiplicadores. Estos fotomultiplicadores están
acoplados a electrónica rápida que amplifica, digitaliza y almacena la imagen de la cascada y
además, los grandes espejos y las cámaras de alta velocidad de CT detectarán el destello de
luz e visualizarán la cascada generada por los rayos gamma para estudiar más a fondo sus
fuentes cósmicas.
Es por esto que es necesario diferenciar estadísticamente entre los fotones causados por
gammas primarios (señal) de las imágenes de lluvias hadrónicas iniciadas por rayos cósmicos
en la atmósfera superior (fondo o background).
#2. Dataset
Para resolver dicho problema se utilizará la base de datos “MAGIC Gamma Telescope”, en la
cual los datos fueron generados con un programa llamado Corsika, que sirve para simular
lluvias de aire.
Este dataset cuenta con las siguientes características:
● Es un problema de Clasificación
● No tiene datos faltantes
● Total de Muestras: 19.020
● Número de atributos: 10
● Número de clases: 2
● Donante: Institute of Computer Science
● Fecha de donación de la BD: 2007-05-01
Está compuesto por las siguientes variables de entrada:
1. longitud: semieje mayor de la elipse
2. ancho: semieje menor de elipse
3. tamaño: Suma del contenido de todos los píxeles [recuento de fotones]

4. conc2: proporción de la suma de los dos píxeles más altos sobre el tamaño
5. conc1: relación entre el píxel más brillante y el tamaño
6. pdist: distancia desde el píxel más brillante hasta el centro, a lo largo del eje mayor
7. m3 de largo: tercera raíz a lo largo del eje mayor
8. m3trans: tercera raíz a lo largo del eje menor
9. alfa: ángulo del eje mayor con el vector al origen
10. dist: distancia desde el origen al centro de la elipse
Además de esto, cuenta con dos variables de salida, que son Gamma (signal) y Hadron
(background)
