Static: al añadir left: 50px a .c1 no se mueve nada. Con position: static, que es el valor por defecto, las propiedades top, right, bottom y left se ignoran, así que el cuadro sigue en su sitio normal.

Relative: c2 con position: relative, top: 20px y left: 50px se desplaza 20px hacia abajo y 50px hacia la derecha respecto a donde estaría normalmente. Pero el hueco original se conserva: el texto de debajo no se mueve, porque para el resto de elementos c2 sigue estando en su sitio de siempre.

Absolute: c3 con position: absolute, top: 0 y right: 0 salta a la esquina superior derecha de la página (o de la ventana), porque no tiene ningún antecesor posicionado. Al añadir position: relative a .contenedor, c3 pasa a colocarse en la esquina superior derecha del contenedor, dentro de su borde. Además, c3 sale del flujo normal y no deja hueco: el contenedor se hace más bajo y el texto de debajo sube, como si c3 no estuviera.

z-index: con c2 en top: -40px sube y tapa una parte de c1, y c2 se ve por encima porque los elementos posicionados se pintan encima de los que no lo están. Para que c1 quede por encima de c2 he puesto a c1 position: relative con z-index: 2 y a c2 z-index: 1.