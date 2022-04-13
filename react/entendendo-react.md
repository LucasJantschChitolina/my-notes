# Entendendo o React

---

### Library vs Framework

---

**Library**: conjunto de funcionalidades focada em resolver um tipo de problema

- date-fns
- axios

**Framework**: conjunto de funcionalidades que resolve vários tipos de problemas

- Angular
- Vue.js

### O que é o React?

---

**Biblioteca** para construção de interfaces (UI’s). Cuida única e exclusivamente das interfaces das aplicações

A parte de requisições, rotas, estilização, animação são providas por todo o ecossistema e comunidade por volta do React.

- [react router](https://v5.reactrouter.com/)
- [material ui](https://mui.com/pt/https://mui.com/pt/)
- [redux](https://redux.js.org/)
- [framer motion](https://www.framer.com/motion/)
- [styled components](https://styled-components.com/)

### React é multiplataforma

---

- **ReactDOM** para aplicações web
- **React Native** para apps mobile
- **React Native** Windows para apps windows

Exemplo de ReactDOM:

![Untitled](entendendo-react-src/Untitled.png)

---

### Componentes

---

Componentes permitem você dividir a UI em partes independentes, reutilizáveis e pensar em cada parte isoladamente. o React permite definirmos componentes como classes (*class components*) ou como funções

Exemplo do uso de componentes na interface do Github:

![Untitled](entendendo-react-src/Untitled%201.png)

Componentes são criados usando o JSX, que é a habilidade de usar HTML dentro de Javascript

**Functional Components**

```jsx
import React from 'react';

function App(){
	return <h1>Componente Funcional</h1>;
}
```

**Class Components**

```jsx
import React from 'react';

class App extends React.Component {
	render() {
		return <h1>Componente de Classe</h1>;
	}
}
```

**Exemplo de componente um pouco mais complexo:**

```jsx
import React from 'react';

import logo from './logo.png';
import './styles.css';

function App(){
	return (
		<div>
			<header>
				<img src={logo} />
			</header>
			<aside>Sidebar</aside>
			<section>Timeline</section>
			<aside>Explore</aside>
		</div>
	);
}
```

Para o código acima, não está havendo a separação de componentes, o ideal seria separá-los em arquivos: Header.js, Sidebar.js, Timeline.js, Explore.js.

### Os navegadores

---

Porém, apesar de tudo, o navegador não vai entender o código acima. Tudo precisa ser transpilado pelo **Babel**

![Untitled](entendendo-react-src/Untitled%202.png)

Assim como o **Webpack** vai pegar todos os nossos arquivos e converter para um bundle.js e manter os arquivos de imagem e .css

![Untitled](entendendo-react-src/Untitled%203.png)

### Por que usar o React?

---

- Reutilização de componentes (aumento de velocidade e produtividade)
- Facilidade de manutenção e escalabilidade
- LOWA (Learn Once, Write Anywhere)