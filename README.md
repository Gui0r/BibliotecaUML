### Documentação do Código

#### **1. Documentação das Classes e Métodos**

##### **Classe `ItemBiblioteca`**
- **Descrição**: Classe base para itens na biblioteca, como livros e usuários.
- **Atributos**:
  - `titulo`: Armazena o título do item (no caso de um livro) ou o nome (no caso de um usuário).
- **Métodos**:
  - `__init__(self, titulo)`: Inicializa o item com um título ou nome.

##### **Classe `Livro`**
- **Descrição**: Representa um livro na biblioteca.
- **Herança**: Herda de `ItemBiblioteca`.
- **Atributos**:
  - `autor`: Nome do autor do livro.
  - `isbn`: Código ISBN do livro.
- **Métodos**:
  - `__init__(self, titulo, autor, isbn)`: Inicializa o livro com um título, autor e ISBN, chamando o construtor da classe base.

##### **Classe `Usuario`**
- **Descrição**: Representa um usuário da biblioteca.
- **Herança**: Herda de `ItemBiblioteca`.
- **Atributos**:
  - `matricula`: Número de matrícula do usuário.
- **Métodos**:
  - `__init__(self, nome, matricula)`: Inicializa o usuário com um nome e matrícula, chamando o construtor da classe base.

##### **Classe `Biblioteca`**
- **Descrição**: Gerencia a coleção de livros e usuários da biblioteca.
- **Atributos**:
  - `livros`: Lista de objetos `Livro` cadastrados na biblioteca.
  - `usuarios`: Lista de objetos `Usuario` cadastrados na biblioteca.
- **Métodos**:
  - `__init__(self)`: Inicializa a biblioteca com listas vazias para livros e usuários.
  - `adicionar_livro(self, livro)`: Adiciona um livro à lista de livros.
  - `adicionar_usuario(self, usuario)`: Adiciona um usuário à lista de usuários.

##### **Classe `GerenciadorDePedidos`**
- **Descrição**: Gerencia pedidos de empréstimos de livros pelos usuários.
- **Atributos**:
  - `biblioteca`: Referência à instância da classe `Biblioteca`.
  - `pedidos`: Lista de pedidos de empréstimos feitos por usuários.
- **Métodos**:
  - `__init__(self, biblioteca)`: Inicializa o gerenciador com uma referência à biblioteca.
  - `solicitar_livro(self, usuario, livro)`: Solicita um livro para um usuário, adicionando o pedido à lista se o livro estiver disponível.

##### **Classe `BibliotecaApp`**
- **Descrição**: Interface gráfica do aplicativo de biblioteca.
- **Atributos**:
  - `root`: Janela principal do aplicativo.
  - `biblioteca`: Instância da classe `Biblioteca`.
  - `main_frame`: Frame principal que contém os botões de navegação.
- **Métodos**:
  - `__init__(self, root)`: Inicializa a interface gráfica com a janela principal e configura os botões de navegação.
  - `cadastro_livro(self)`: Exibe a tela para cadastrar um novo livro.
  - `cadastro_usuario(self)`: Exibe a tela para cadastrar um novo usuário.
  - `visualizar_livros(self)`: Exibe a lista de livros cadastrados.
  - `visualizar_usuarios(self)`: Exibe a lista de usuários cadastrados.
  - `voltar(self, frame)`: Volta à tela principal de navegação.

#### **2. Descrição das Funcionalidades**

O programa é uma aplicação de biblioteca com interface gráfica que permite gerenciar o cadastro de livros e usuários. As funcionalidades principais incluem:

- **Cadastro de Livros**: Permite adicionar novos livros à biblioteca, especificando o título, autor e ISBN.
- **Cadastro de Usuários**: Permite adicionar novos usuários à biblioteca, especificando o nome e a matrícula.
- **Visualização de Livros**: Exibe uma lista de todos os livros cadastrados na biblioteca.
- **Visualização de Usuários**: Exibe uma lista de todos os usuários cadastrados na biblioteca.

#### **3. Guia de Execução**

1. **Inicialização**:
   - O programa começa executando o bloco `if __name__ == "__main__":`, onde a instância da classe `BibliotecaApp` é criada, iniciando a interface gráfica.
   - A janela principal `root` é criada, e a aplicação entra em loop com `root.mainloop()`.

2. **Navegação Inicial**:
   - A interface gráfica exibe um menu principal com botões para cadastrar livros, cadastrar usuários, visualizar livros e visualizar usuários.

3. **Cadastro de Livros**:
   - Ao clicar em "Cadastrar Livro", a tela de cadastro de livros é exibida. O usuário pode inserir as informações do livro e salvar, voltando à tela principal em seguida.

4. **Cadastro de Usuários**:
   - Similar ao cadastro de livros, o usuário pode clicar em "Cadastrar Usuário", inserir as informações e salvar.

5. **Visualização de Livros e Usuários**:
   - O usuário pode visualizar a lista de livros ou usuários cadastrados. Para voltar à tela principal, há um botão "Voltar".

6. **Finalização**:
   - O usuário pode encerrar o programa fechando a janela principal.

#### **4. Manual de Instalação e Uso**

##### **Dependências**
- `tkinter`: Biblioteca padrão do Python para interfaces gráficas. Não é necessária instalação adicional se estiver utilizando uma versão padrão do Python.

##### **Instalação**
1. **Instalação do Python**:
   - Certifique-se de que o Python 3.x está instalado em sua máquina.
   - Para verificar a instalação, execute `python --version` ou `python3 --version` no terminal.

2. **Instalação de Dependências**:
   - Caso utilize uma versão personalizada do Python ou precise instalar o `tkinter`, você pode fazê-lo com o comando:
     ```bash
     sudo apt-get install python3-tk
     ```

##### **Inicialização**
1. **Rodando o Programa**:
   - Navegue até o diretório onde o arquivo do código está localizado.
   - Execute o programa com o comando:
     ```bash
     python biblioteca_app.py
     ```

##### **Uso**
1. **Iniciando o Programa**:
   - Ao executar o programa, uma janela com o menu principal será aberta.
  
2. **Cadastrando Livros e Usuários**:
   - Clique em "Cadastrar Livro" para adicionar novos livros.
   - Clique em "Cadastrar Usuário" para adicionar novos usuários.
  
3. **Visualizando Livros e Usuários**:
   - Use os botões "Visualizar Livros" e "Visualizar Usuários" para ver os dados cadastrados.
  
4. **Encerrando o Programa**:
   - Para encerrar, feche a janela principal ou pressione `Ctrl+C` no terminal onde o programa está rodando.
