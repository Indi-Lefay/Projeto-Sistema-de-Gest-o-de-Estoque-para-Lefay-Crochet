# 🧶 **Estoque da Loja de Crochê - Gerenciamento de Produtos** 🧵

Bem-vindo ao meu **projeto de gestão de estoque** para a minha lojinha de **crochê**! Aqui, você vai encontrar o sistema que estou criando para **organizar meus chaveiros, amigurumis** e todas as outros projetos da minha loja de crochê!

## 🚀 **O que já está pronto?**

Este é o **sistema de estoque** da minha loja de crochê, que já conta com algumas funcionalidades:

### 1. **Cadastro de Produtos**
Agora consigo cadastrar todos os meus produtos de crochê (chaveiros, amigurumis, etc.) de forma fácil e organizada! Com o sistema, posso inserir:
- Nome do produto
- Categoria (por exemplo, chaveiro, amigurumi)
- Preço de venda
- Quantidade em estoque
- Materiais usados (pra não esquecer de nenhum detalhe fofinho!)

### 2. **Exibição dos Produtos**
Apesar de a interface ainda não estar pronta, o banco de dados já está super organizadinho! Em breve, poderei visualizar todos os meus produtos de crochê e ver como anda o estoque, tudo na palma da mão.

### 3. **Exportação para Excel**
Essa é uma das funcionalidades que já consegui implementar, e é **maravilhosa** para organizar e salvar os dados. Com **Pandas**, posso exportar o estoque para um arquivo Excel, perfeito para backup e análises rápidas!

### 4. **Google Colab para Análises**
Ah, e o melhor de tudo é que dá para rodar tudo no **Google Colab** para facilitar o processo, fazer análises e **gerar o Excel** de qualquer lugar. Super prático!

---

## 🧩 **Tecnologias Usadas**

- **Python**: A linguagem de programação queridinha, que torna tudo possível!
- **SQLite**: Um banco de dados simples e eficaz para armazenar todos os meus dados.
- **Pandas**: A biblioteca **mágica** que me ajuda a exportar os dados para Excel.
- **HTML/CSS**: Futuro uso para a interface do web app (isso ainda está por vir, mas já estamos quase lá!).

---

## 🛠️ **Como Rodar o Projeto para analise**

### 📦 **Pré-requisitos**
O  código pode ser rodado tanto no terminal quanto no Google Colab.Logo:

Antes de rodar o projeto, é bom garantir que você tenha o **Python** instalado. Para verificar se você tem, basta rodar o seguinte comando no terminal:

```bash
python --version
```

### 🧑‍💻 **Instalando as Dependências**

Primeiro, instale as dependências necessárias no seu terminal com o comando abaixo:

```bash
pip install pandas sqlite3
```

### 🚀 **Rodando o Código no Google Colab**

Agora, se você quer rodar o código diretamente no Google Colab (e ver como tudo funciona no ambiente online), basta fazer o seguinte:

1. **Carregue o banco de dados do SQLite para o Colab**.
2. **Execute o código para exportar o estoque para um arquivo Excel**:

```python
import sqlite3
import pandas as pd

def conectar():
    conexao = sqlite3.connect("estoque.db")
    return conexao

# Função de exportação para Excel
def exportar_para_excel():
    conexao = conectar()
    df = pd.read_sql_query("SELECT * FROM produtos", conexao)
    conexao.close()
    df.to_excel("estoque_loja_croche.xlsx", index=False)
    print("Arquivo Excel gerado com sucesso!")
```

### 💾 **O que vai acontecer?**

Ao rodar esse código, você vai gerar o arquivo **`estoque_loja_croche.xlsx`**, que vai salvar todos os seus produtos e suas informações de estoque em um arquivo Excel, pronto para ser analisado!

---

## 🚧 **Atividades Futuras** ✨

Este projeto está ainda em **desenvolvimento**! Algumas das funcionalidades que estou planejando adicionar:

1. **Web App com Flask**: Vou criar um web app fofinho para a loja, onde vou poder **cadastrar produtos** e **visualizar o estoque** com uma interface bem bonitinha.
2. **Melhorias na Interface**: Em breve, vou ajustar a interface com **HTML** e **CSS** para deixar tudo bem organizadinho e visualmente encantador! 🖥️✨
3. **Controle Completo de Estoque**: Adicionar funções para **atualizar**, **remover** produtos e até criar um sistema de **categorias** para organizar ainda mais os meus produtos.
4. **Autenticação de Usuário**: Em breve, vou adicionar um sistema de **login** para poder controlar o acesso ao estoque e garantir que só pessoas autorizadas façam alterações.
5. **Relatórios e Análises**: Criar relatórios para **analisar vendas**, **estoque** e muito mais. 
---

## 🎯 **Objetivo do Projeto**

Este projeto foi criado com muito amor para ajudar na **gestão do estoque da minha loja de crochê**. A ideia é **organizar**, **controlar** e **analisar** os produtos, para que eu possa ter um melhor controle do meu negócio, de uma forma super prática e divertida!

---
