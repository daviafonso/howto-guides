# Comandos de Terminal Úteis para Desenvolvedores no Linux

## Navegação e Manipulação de Diretórios

- **Listar arquivos e diretórios**:
  ```sh
  ls
  ```
  - Adicione `-l` para listar com detalhes e `-a` para incluir arquivos ocultos:
    ```sh
    ls -la
    ```

- **Navegar para um diretório**:
  ```sh
  cd nome_do_diretorio
  ```

- **Voltar para o diretório anterior**:
  ```sh
  cd ..
  ```

- **Criar um novo diretório**:
  ```sh
  mkdir nome_do_diretorio
  ```

- **Remover um diretório**:
  ```sh
  rmdir nome_do_diretorio
  ```
  - Para remover diretórios não vazios, use:
    ```sh
    rm -r nome_do_diretorio
    ```

- **Mostrar o diretório atual**:
  ```sh
  pwd
  ```

- **Exibir a estrutura de diretórios**:
  - Instale `tree` se ainda não estiver instalado:
    - Em sistemas baseados em Debian/Ubuntu:
      ```sh
      sudo apt install tree
      ```
    - Em sistemas baseados em Red Hat:
      ```sh
      sudo yum install tree
      ```
    - No Arch Linux:
      ```sh
      sudo pacman -S tree
      ```
  - Para exibir a estrutura de diretórios:
    ```sh
    tree
    ```
  - Para especificar o número de galhos a serem visualizados:
    ```sh
    tree -L N
    ```
    - Substitua `N` pelo nível de profundidade desejado.

## Manipulação de Arquivos

- **Criar um novo arquivo**:
  ```sh
  touch nome_do_arquivo
  ```

- **Visualizar o conteúdo de um arquivo**:
  ```sh
  cat nome_do_arquivo
  ```
  - Use `less` ou `more` para visualização paginada:
    ```sh
    less nome_do_arquivo
    ```

- **Editar um arquivo**:
  - Use `nano`, `vim`, ou `code` (para VS Code):
    ```sh
    nano nome_do_arquivo
    vim nome_do_arquivo
    code nome_do_arquivo
    ```

- **Copiar um arquivo**:
  ```sh
  cp arquivo_origem arquivo_destino
  ```

- **Mover ou renomear um arquivo**:
  ```sh
  mv arquivo_origem arquivo_destino
  ```

- **Excluir um arquivo**:
  ```sh
  rm nome_do_arquivo
  ```

## Gerenciamento de Pacotes

- **Atualizar a lista de pacotes (Debian/Ubuntu)**:
  ```sh
  sudo apt update
  ```

- **Instalar um pacote (Debian/Ubuntu)**:
  ```sh
  sudo apt install nome_do_pacote
  ```

- **Atualizar pacotes instalados (Debian/Ubuntu)**:
  ```sh
  sudo apt upgrade
  ```

- **Remover um pacote (Debian/Ubuntu)**:
  ```sh
  sudo apt remove nome_do_pacote
  ```

- **Atualizar a lista de pacotes (Arch Linux)**:
  ```sh
  sudo pacman -Syu
  ```

- **Instalar um pacote (Arch Linux)**:
  ```sh
  sudo pacman -S nome_do_pacote
  ```

- **Remover um pacote (Arch Linux)**:
  ```sh
  sudo pacman -R nome_do_pacote
  ```

## Processos e Recursos do Sistema

- **Listar processos em execução**:
  ```sh
  ps aux
  ```

- **Buscar um processo específico**:
  ```sh
  pgrep nome_do_processo
  ```

- **Encerrar um processo**:
  ```sh
  kill PID
  ```
  - Substitua `PID` pelo identificador do processo.

- **Monitorar o uso de recursos do sistema**:
  ```sh
  top
  ```
  - Para uma visualização mais avançada, use `htop`:
    ```sh
    htop
    ```

## Git

- **Clonar um repositório**:
  ```sh
  git clone https://github.com/usuario/nome_do_repositorio.git
  ```

- **Adicionar alterações**:
  ```sh
  git add .
  ```

- **Fazer um commit**:
  ```sh
  git commit -m "Mensagem do commit"
  ```

- **Enviar alterações para o repositório remoto**:
  ```sh
  git push origin main
  ```

- **Baixar as últimas alterações do repositório remoto**:
  ```sh
  git pull origin main
  ```

## Busca e Filtragem

- **Buscar texto dentro de arquivos**:
  ```sh
  grep "texto" nome_do_arquivo
  ```
  - Para buscar recursivamente em diretórios:
    ```sh
    grep -r "texto" nome_do_diretorio
    ```

- **Encontrar arquivos com um padrão específico**:
  ```sh
  find /caminho/do/diretorio -name "padrão"
  ```

## Redes e Conectividade

- **Verificar a conectividade com um servidor**:
  ```sh
  ping endereco_do_servidor
  ```

- **Exibir informações sobre a rede**:
  ```sh
  ifconfig
  ```
  - Em sistemas mais recentes, pode ser necessário usar `ip`:
    ```sh
    ip addr
    ```

- **Testar a conectividade com uma porta específica**:
  ```sh
  nc -zv endereco_do_servidor porta
  ```

