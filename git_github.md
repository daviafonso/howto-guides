# Como Usar Git e GitHub

## Configurar o Git

1. **Instalar o Git**:
   - Em sistemas baseados em Debian/Ubuntu:
     ```sh
     sudo apt-get install git
     ```
   - Em sistemas baseados em Red Hat:
     ```sh
     sudo yum install git
     ```
   - No Arch Linux:
     ```sh
     sudo pacman -S git
     ```
   - No macOS (usando Homebrew):
     ```sh
     brew install git
     ```

2. **Configurar o Nome e Email**:
   - Configure seu nome de usuário:
     ```sh
     git config --global user.name "Seu Nome"
     ```
   - Configure seu email:
     ```sh
     git config --global user.email "seuemail@example.com"
     ```

## Criar um Repositório Git

1. **Inicializar um Repositório Local**:
   - Navegue para o diretório do projeto e inicialize o repositório:
     ```sh
     cd caminho/do/seu/projeto
     git init
     ```

2. **Adicionar Arquivos ao Repositório**:
   ```sh
   git add .
   ```
   - Adiciona todos os arquivos no diretório atual.

3. **Fazer um Commit**:
   ```sh
   git commit -m "Mensagem do commit"
   ```

## Conectar a um Repositório no GitHub

1. **Criar um Repositório no GitHub**:
   - Vá para [GitHub](https://github.com/) e crie um novo repositório.

2. **Adicionar o Repositório Remoto**:
   ```sh
   git remote add origin https://github.com/usuario/nome_do_repositorio.git
   ```
   - Substitua `usuario` e `nome_do_repositorio` pelos seus detalhes.

3. **Enviar Alterações para o GitHub**:
   ```sh
   git push -u origin main
   ```

## Configurar SSH para GitHub

1. **Gerar uma Nova Chave SSH**:
   ```sh
   ssh-keygen -t rsa -b 4096 -C "seuemail@example.com"
   ```
   - Pressione Enter para aceitar o local padrão do arquivo.

2. **Adicionar a Chave SSH ao Agente**:
   ```sh
   eval "$(ssh-agent -s)"
   ssh-add ~/.ssh/id_rsa
   ```

3. **Adicionar a Chave SSH ao GitHub**:
   - Copie o conteúdo da chave pública:
     ```sh
     cat ~/.ssh/id_rsa.pub
     ```
   - Vá para [GitHub](https://github.com/settings/keys) e adicione uma nova chave SSH com o conteúdo copiado.

## Clonar um Repositório do GitHub

1. **Clonar um Repositório**:
   ```sh
   git clone git@github.com:usuario/nome_do_repositorio.git
   ```
   - Substitua `usuario` e `nome_do_repositorio` pelos detalhes do repositório que você deseja clonar.

## Atualizar o Repositório Local

1. **Baixar as Últimas Alterações**:
   ```sh
   git pull origin main
   ```

2. **Verificar o Status do Repositório**:
   ```sh
   git status
   ```

3. **Verificar o Histórico de Commits**:
   ```sh
   git log
   ```

## Branch `main` vs. `master`

- **Branch `master`**: Era o nome padrão para o branch principal em muitos repositórios Git. Isso reflete a convenção mais antiga usada pelo Git.

- **Branch `main`**: GitHub e outros provedores de hospedagem de código mudaram o nome padrão para `main` em novos repositórios para promover uma terminologia mais inclusiva. O Git agora permite que você defina o nome do branch principal de acordo com sua preferência.

Para ajustar o nome do branch principal em um repositório existente, você pode usar os seguintes comandos:

1. **Renomear o Branch Local**:
   ```sh
   git branch -m master main
   ```

2. **Atualizar o Branch Remoto**:
   ```sh
   git push -u origin main
   ```

3. **Atualizar o Branch Padrão no GitHub**:
   - Vá para o repositório no GitHub, acesse as configurações e atualize o branch padrão para `main`.

