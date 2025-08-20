# clickjacking-lab
Un simple laboratorio de clickjacking

1) Abrir victima.html, esta web representa una web de un banco dónde hay un botón que al presionarlo transfiere dinero.

2) Abrir atacante.html, esta web representa la web desarrollada por un hacker malintencionado, este hacker ocultó el contenido real del banco detrás de la web ficticia, hay un botón para reproducir un video, pero al clickearlo en realidad se está clickeando el botón del banco (ya que el botón está debajo).

Modificando las opciones del CSS podemos jugar con los valores de opacity del tag <button> del body que es el botón falso del atacante y del tag <button> que está dentro del <iframe> el cual representa al banco. De esa manera podemos visualizar como un botón se colocó encima del otro.

También es importante notar el valor z-index, ya que es el encargado de posicionar los elementos "encima" o "debajo", si tenemos un botón con z-index:-2 y otro con z-index:1, el z-index:-2 estará por debajo del -1, 0, 1, 2, etc...
