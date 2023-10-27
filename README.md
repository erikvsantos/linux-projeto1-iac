
# DIO | Desafio de Projeto - Linux Experience

Repositório desenvolvido para Desafio de Projeto do curso **Linux Experience** da [Digital Innovation One](https://www.dio.me/).

## 🎯 Objetivo

Criar um script de criação de estrutura de usuários, diretórios e permissões.

Neste projeto temos 9 usuários, 3 departamentos, 4 diretórios e 3 grupos de permissões

| Departamentos | Usuários                    | Diretórios | Grupos de usuários |
|---------------|-----------------------------|------------|--------------------|
| Administração | carlos, maria, joao         | /adm       | GRP_ADM            |
| Vendas        | debora, sebastiana, roberto | /ven       | GRP_VEN            |
| Segurança     | josefina, amanda, rogerio   | /sec       | GRP_SEC            |
|               |                             | /publico   |                    |

### Grupos de Permissão

Existem três grupos de permissão:

1. **GRP_ADM**: Este grupo será proprietario do diretório **/adm** tendo as permissões leitura, escrita e Execução (rwx)
2. **GRP_VEN**: Este grupo será proprietario do diretório **/ven** tendo as permissões leitura, escrita e Execução (rwx)
3. **GRP_SEC**: Este grupo será proprietario do diretório **/sec** tendo as permissões leitura, escrita e Execução (rwx)


## 💻 Pré-requisitos

- instalação do Ubuntu Server

## ⚙️ Funcionalidades

**Etapas do Script**

- `Etapa 1 - Criando diretórios`: comando utilizado: ``` mkdir "Nome do Diretório" ```
- `Etapa 2 - Criando Grupos de Usuários`: comando utilizado: ``` groupadd "Nome do Grupo" ```
- `Etapa 3 - Criando usuários`: comando utilizado: ``` useradd "Nome do Usuário"-m -s /bin/bash -p $(openssl passwd -crypt Senha123) -G GRP_ADM ```

**-m**: utilizado junto ao comando **useradd** cria um diretório inicial do usuário (**/home**).

**-s /bin/bash**: Determina o nome do shell de logon do usuário.

## 🔍 Referências
- [Digital Innovation One]().
