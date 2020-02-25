### Conceitos abordados:

1.  Instalar React Hooks.
2.  Transformar State em useState.
3.  Transformar componentDidMount em useEffect.
4.  Realocar props.

___

### Desrição do projeto:

Converter a forma clássica de usar Redux (através de class) para React Hooks.

Projeto Inicial: https://github.com/MaisDennis/GoStack10.0-Modulo-07

Um website 'Rocketshoes', que tem uma lista de produtos (tênis). O site permite adicionar os produtos ao 'Carrinho'. Na página do Carrinho,  podemos alterar a quantidade de cada produto, remover o produto e temos o retorno do valor subtotal e total de produtos em R$.

### Iniciando o projeto:

1.  json-server server.json -p 3333
2.  yarn start

### Convertendo classe (React Hooks)

1.  Converter todas as classes do modulo07
2.  Instalar Hooks.
    ```
    yarn add eslint-plugin-react-hooks -D
    ```
3.  .eslintrc.js
    1.  plugins, rules.
4.  Home/index.js
    1.  Tem componentDidMount e State.
    2.  Transformar class em function.
    3.  remover { component } from 'react';
    4.  import e criar useState.
    5.  componentDidMount -> useEffect:
        1.  import useEffect.
        2.  async componentDidMount -> useEfffect
        3.  obs. setState -> setProducts, loadProducts, [] ao final (componentDidMount)
    6.  tirar render()
    7.  const { products } = this.state; -> const [ products, setProducts ] = useState([]);
    8.  const { amount } = this.props; -> function Home( { amount }) {
    9.  const { addToCartRequest } = this.props; -> function Home( { amount, addToCartRequest }) {
    9.  Usar apenas return()
    10. e não tem mais this: this.handleAddProduct(product.id)



