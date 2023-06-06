Hola que tal?, un resumen de la clase (con algunas aclaraciones).

Para clonar el repositorio:

git clone https://github.com/platzi/curso-react-intro.git
Luego seguimos con la instalación de las dependencias:

npm i
Aquí una aclaración, en mi caso uso node 18 y me presento el siguiente error:

opensslErrorStack: [ 'error:03000086:digital envelope routines::initialization error' ],
  library: 'digital envelope routines',
  reason: 'unsupported',
Para solucionar esto elimine la carpeta node_modulesy package-lock.json aunque no solucionó el error pude encontrar unos cambios en los scripts de packge.json:

"start": "SET NODE_OPTIONS=--openssl-legacy-provider && react-scripts start",
    "build": "SET NODE_OPTIONS=--openssl-legacy-provider && react-scripts build",
Con esto ya se soluciono el primer problema que tuvé.
Continuando con la ejecución de la aplicación tuve el siguiente mensaje:

Line X: 'React' must be in scope when using JSX
Este mensaje nos dice que no React debe estar dentro del scope cuando usamos JSX, (aún no entiendo porque pasa esto si las extensiones estan con .js), pero bueno al final solucioné esta alerta importando React en App.js:

import React from 'react';
Luego de esto todo bien.