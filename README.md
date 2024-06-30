# Desafio Dio - Desenvolvendo um Menu Hamburguer e Morphing Menu com CSS Transitions



Neste projeto, criaremos um menu hambúrguer e um menu morphing usando CSS Transitions. Um menu hambúrguer é um tipo de menu de navegação comumente usado em dispositivos móveis, enquanto um menu morphing é um tipo de menu que muda de forma quando clicado. Usaremos CSS Transitions para criar animações suaves para esses menus.



### **Pré-requisitos**



- Conhecimento básico de HTML, CSS e JavaScript

  

### **Passos**



### **1. Criar um Menu HTML Básico**



Comece criando um menu HTML básico com um botão de hambúrguer e uma lista de itens de menu:

plaintext



```plaintext
<nav>
  <button class="hamburger">
    <span class="bar"></span>
    <span class="bar"></span>
    <span class="bar"></span>
  </button>
  <ul class="menu">
    <li><a href="#">Item 1</a></li>
    <li><a href="#">Item 2</a></li>
    <li><a href="#">Item 3</a></li>
  </ul>
</nav>
```



### **2. Adicionar Estilos CSS para o Menu Hambúrguer**



Agora, adicione estilos CSS para o menu hambúrguer. Isso inclui estilos para o botão do hambúrguer e as barras dentro do botão:

css



```css
.hamburger {
  display: block;
  position: relative;
  width: 30px;
  height: 30px;
  margin: 0 auto;
  cursor: pointer;
}

.hamburger .bar {
  display: block;
  position: absolute;
  width: 30px;
  height: 3px;
  background-color: #000;
  transition: all 0.3s ease-in-out;
}

.hamburger .bar:nth-child(1) {
  top: 0;
}

.hamburger .bar:nth-child(2) {
  top: 10px;
}

.hamburger .bar:nth-child(3) {
  top: 20px;
}
```



**3. Adicionar Estilos CSS para o Menu Morphing**



Em seguida, adicione estilos CSS para o menu morphing. Isso inclui estilos para o menu quando ele está oculto e quando está visível:

css

```css
.menu {
  display: none;
  position: absolute;
  top: 50px;
  left: 0;
  width: 100%;
  background-color: #fff;
  transition: all 0.3s ease-in-out;
}

.menu.active {
  display: block;
}
```



### **4. Adicionar JavaScript para Controlar o Menu**



Finalmente, adicione JavaScript para controlar o menu. Isso inclui alternar as classes `active` no botão do hambúrguer e no menu quando o botão é clicado:

javascript



```javascript
const hamburger = document.querySelector('.hamburger');
const menu = document.querySelector('.menu');

hamburger.addEventListener('click', () => {
  hamburger.classList.toggle('active');
  menu.classList.toggle('active');
});
```



### **Conclusão**



Neste projeto, criamos um menu hambúrguer e um menu morphing usando CSS Transitions. Esses tipos de menus são comumente usados em dispositivos móveis e podem ser usados para criar interfaces de usuário mais interativas e atraentes.
