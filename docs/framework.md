# 前端框架

## 前后端分离

## Vue vs React

### Hello World


``` html
<div id="app"></div>

<script>
  const { createApp, ref } = Vue;

  const App = {
    setup() {
      const message = ref('Hello World!');
      return {
        message
      }
    },
    template: 
      `<div>
        <h1>{{ message }}</h1>
      </div>`
  };

  const app = createApp(App);
  app.mount('#app');
</script>
```


``` html
<div id="root"></div>

<script type="text/babel">
  function App() {
    const [message, setMessage] = React.useState('Hello World!');

    return (
      <div>
        <h1>{ message }</h1>
      </div>
    );
  }

  const container = document.getElementById('root');
  const root = ReactDOM.createRoot(container);
  root.render(<App />);
</script>
```