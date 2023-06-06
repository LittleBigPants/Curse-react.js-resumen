¿Cómo escuchamos los eventos en React?
…
Una de las formas es añadiendo “onclick” a nuestro elemento, parecido a la forma que lo realizábamos convencionalmente en HTML y JS, con la diferencia que en React utilizaremos camelCase, ósea “onClick”.
Todo lo que empiece con “on” en React será considerado un Evento, es decir, todo lo que comience con "on" será transformado a un AddEventListener (Escuchador de Eventos), es importante tener en cuenta que el valor que recibirá nuestro Evento, debe ser encapsulado dentro de una función para que se ejecute correctamente.