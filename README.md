# Laboratorio de física VR con Three.js

Este proyecto contiene un ejemplo de realidad virtual desarrollado con Three.js y WebXR.

El usuario puede entrar a la escena con manos compatibles, apuntar a las piezas y agarrarlas con un pellizco. La escena incluye cinco formas —cubos, prismas triangulares, esferas, cilindros y toros— que responden a gravedad, masa, rebote, fricción y velocidad angular.

El acabado visual usa una dirección de videojuego arcade: materiales físicos con metalizado, brillo de capa transparente, emisión de color y una iluminación ambiental cian/magenta. Cada forma tiene una combinación propia para poder distinguirla mientras cae o se lanza.

## Física incluida

- Gravedad de `-9.81 m/s²`.
- Contacto con el suelo y límites laterales invisibles.
- Separación iterativa entre cuerpos para evitar que se superpongan.
- Impulsos de rebote y fricción al chocar.
- Arrastre cinemático: al soltar una pieza conserva la velocidad de la mano para poder lanzarla.

Las colisiones usan una esfera envolvente por pieza. Esto mantiene el demo liviano y estable en WebXR, aunque no calcula contacto exacto entre las caras de un cubo o un prisma. Para una simulación de producción con mallas complejas convendría sustituir esta capa por un motor dedicado como Rapier o Cannon-es.

## Uso

Sirve el directorio con un servidor local y abre `index.html` en un navegador compatible con WebXR. La interfaz de la escena y el botón de entrada a VR están traducidos al español.
