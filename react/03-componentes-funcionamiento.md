Lo primero en hacer es eliminar los elementos del componente App.js, dejandolo con la siguiente estructura:

import React from 'react'
import logo from './platzi.webp';
import './App.css';

function App() {
  return (
    <div className="App">
    <TodoItem />
    <TodoItem />
    <TodoItem />
      
    </div>
  );
};
function TodoItem() {
  return (
    <li>
      <span>V</span>
      <p>Llorar con la Lorona</p>
      <span>X</span>
    </li>
  );
}

export default App;
Ahora debajo del div, agregamos un componente <TodoCounter />
<TodoSearch /> y luego agregamos un contenedor de los `` llamandolo

  <TodoItem />
  <TodoItem />
  <TodoItem />
<TodoList/>
Luego al final agregamos el boton <CreateTodoButton />.
Ahora toca crear los componentes que fuimos construyendo (En el caso de tener el error por React debemos importarlo también se puede usar el shorcout imr ojo que necesita tener la extensión de react):

Componente TodoCounter
import React from 'react'

function TodoCounter() {
  return (
    <h1>Haz completado 3 de 5 TODOS</h1>
  );
}

export { TodoCounter };
Componente TodoList
En el caso de este componente enviamos las propiedades o prop's para ir renderizando los TODO’s

import React from 'react'

function TodoList(props) {
  return (
    <ul>
      {props.children}
    </ul>
  )
}

export { TodoList };
Componente Todo Search
import React from 'react'

function TodoSearch() {
  return (
    <input placeholder="Buscar..." />
  )
}

export { TodoSearch };
Componente TodoItem
Este componente lo separamos del componente App.js

import React from "react";

function TodoItem() {
  return (
    <li>
      <span>V</span>
      <p>Llorar con la Lorona</p>
      <span>X</span>
    </li>
  );
}

export { TodoItem };

Componente TodoButton
import React from "react";

function CreateTodoButton() {
  return <button>+</button>;
}

export { CreateTodoButton };
Componente App Final
import React from "react";
import { TodoCounter } from "./TodoCounter";
import { TodoSearch } from "./TodoSearch";
import { TodoList } from "./TodoList";
import { TodoItem } from "./TodoItem";
import { CreateTodoButton } from "./CreateTodoButton";
import "./App.css";

function App() {
  return (
    <div className="App">
      <TodoCounter />
      <TodoSearch />

      <TodoList>
        <TodoItem />
        <TodoItem />
        <TodoItem />
      </TodoList>

      <CreateTodoButton />
    </div>
  );
}


export default App;