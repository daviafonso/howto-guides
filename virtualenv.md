# Como Usar `virtualenv`

## Criar um Ambiente Virtual

1. **Instale o `virtualenv`** (se ainda não estiver instalado):
   ```sh
   pip install virtualenv
   ```

2. **Crie um novo ambiente virtual**:
   ```sh
   virtualenv nome_do_ambiente
   ```
   - Substitua `nome_do_ambiente` pelo nome desejado para o ambiente.

## Ativar o Ambiente Virtual

- **No Windows**:
  ```sh
  nome_do_ambiente\Scripts\activate
  ```

- **No macOS/Linux**:
  ```sh
  source nome_do_ambiente/bin/activate
  ```

## Verificar se o Ambiente Virtual Está Ativado

- **Verifique o Prompt**: O nome do ambiente deve aparecer no início da linha de comando (por exemplo, `(nome_do_ambiente)`).

- **Verifique o Python Ativo**:
  ```sh
  which python
  ```
  - O caminho deve apontar para o diretório `bin` do ambiente virtual (em sistemas Unix) ou `Scripts` (no Windows).

## Instalar Pacotes Dentro do Ambiente Virtual

1. **Instale pacotes com `pip`**:
   ```sh
   pip install nome_do_pacote
   ```

## Verificar os Pacotes Instalados

1. **Liste os pacotes instalados**:
   ```sh
   pip list
   ```

2. **Para ver detalhes específicos**:
   ```sh
   pip show nome_do_pacote
   ```
