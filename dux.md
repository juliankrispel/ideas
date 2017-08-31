# Dux - A simple abstraction over redux connect

```js
Dux.registerActions(
  'todo',
  {
    addTodo,
    deleteTodo,
    updateTodo
  }
);

Dux.registerSelector(
  'todo',
  ({ todos }, ownProps) => ({ todos })
);

const Todos = Dux.connect('todo')(({ todos }) => (
  <ul>
    {todos.map(todo => (
      <Todo key={todo.id} {...todo} />
    ))}
  </ul>
));

const App = () => (
  <Provider dux={dux}>
    <Todos />
  </Provider>
)
```
