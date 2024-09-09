# Resolver Problemas Comuns no Git e GitHub

Este guia cobre alguns dos problemas mais comuns encontrados ao usar Git e GitHub e como resolvê-los.

## Rejeição ao Enviar Alterações (`git push`)

### Problema:
Você recebe uma mensagem de erro ao tentar enviar (`push`) suas alterações para o repositório remoto, indicando que o push foi rejeitado.

### Solução:
Isso geralmente acontece porque o repositório remoto contém commits que não estão no seu repositório local.
1. **Puxar Alterações do Repositório Remoto**:
   ```sh
   git pull origin main --rebase
   ```
   - Resolva quaisquer conflitos que possam ocorrer.
   - Após resolver os conflitos, adicione e faça commit das alterações:
     ```sh
     git add <arquivo>
     git rebase --continue
     ```
2. **Enviar Alterações para o Repositório Remoto**:
   ```sh
   git push -u origin main
   ```

## Conflitos ao Fazer Merge

### Problema:
Você enfrenta conflitos ao tentar mesclar (`merge`) branches ou durante um `rebase`.

### Solução:
1. **Identificar e Resolver Conflitos**:
   - Abra os arquivos em conflito no seu editor de texto.
   - Remova as marcas de conflito e ajuste o conteúdo conforme necessário.
   - Adicione os arquivos resolvidos:
     ```sh
     git add <arquivo>
     ```
2. **Continuar o Processo de Merge ou Rebase**:
   - Para merge:
     ```sh
     git commit
     ```
   - Para rebase:
     ```sh
     git rebase --continue
     ```

## Erro ao Clonar Repositório (`git clone`)

### Problema:
Você recebe um erro ao tentar clonar um repositório, como "Repository not found" ou "Permission denied".

### Solução:
1. **Verificar a URL do Repositório**:
   - Certifique-se de que você está usando a URL correta do repositório.
2. **Verificar as Credenciais**:
   - Se estiver usando SSH, verifique se sua chave SSH está corretamente configurada e adicionada ao GitHub.
   - Se estiver usando HTTPS, verifique suas credenciais de autenticação.

## Problemas com Branches

### Problema:
Você está tentando alternar (`checkout`) ou excluir (`delete`) um branch e encontra problemas.

### Solução:
1. **Alternar para um Branch**:
   ```sh
   git checkout <nome-do-branch>
   ```
2. **Excluir um Branch Local**:
   ```sh
   git branch -d <nome-do-branch>
   ```
3. **Excluir um Branch Remoto**:
   ```sh
   git push origin --delete <nome-do-branch>
   ```

## Mensagens de Erro ao Usar SSH

### Problema:
Você recebe um erro de autenticação ao tentar se conectar ao GitHub via SSH.

### Solução:
1. **Verificar a Chave SSH**:
   - Certifique-se de que sua chave SSH está configurada corretamente e adicionada ao seu agente SSH:
     ```sh
     ssh-add ~/.ssh/id_rsa
     ```
2. **Testar a Conexão SSH**:
   ```sh
   ssh -T git@github.com
   ```
