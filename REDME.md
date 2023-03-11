#### INSTALAÇÃO GIT

1. [Entre no site oficial do GIT](https://git-scm.com/downloads)
2. Escolha a opção Windows e o instalador será baixado automaticamente
3. Mantenha as opções pré selecionadas
4. Próximo
5. Instalar
6. Antes de finalizar a instalação, selecione a opção "Lauch Git Bash"
7. No Git Bash, verifique se o GIT está instalado:`git --version`
8. configurações iniciais:
   1. Configurar o nome do usuário:`git config --global user.name "Seu nome"`
   2. Configure o endereço de e-mail (o mesmo do GitHub):`git config --global user.email seu_email_do_GitHub@email.br`
   3. Verifique as configurações:`git config --list`
9. Instalação e configurações iniciais concluídas!

#### GERAR TOKEN DE ACESSO

1. Faça seu login no GitHub

2. Gere um token de acesso

    : Seu perfil >> Configurações >> Configurações do desenvolvedor >> Tokens de acesso pessoal >> Gerar novo token

   1. Nota: Ecolha um nome para o token
   2. Expiração: Sem expiração
   3. Selecionar escopos: Selecione todos os campos
   4. Gerar token

3. Copie uma String referente ao token

4. Salve em um lugar seguro que você consiga consultar posteriormente

5. Criação e configurações iniciais concluídas!

#### GERAR CHAVE SSH

1. Consulte a [documentação oficial](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)

2. Verifique se 

   existe alguma chave SSH

    em sua máquina:

   1. Sem Git Bash:`ls -al ~/.ssh`
   2. Se sim, para ser válido, o GitHub suporta qualquer um desses nomes de arquivos a seguir:
      - id_rsa.pub
      - id_ecdsa.pub
      - id_ed25519.pub

3. Caso não exista, gere uma chave SSH:

   1. Sem Git Bash:`ssh-keygen -t ed25519 -C "seu_email_do_GitHub@example.com"`
   2. Caso a *opção acima não funcione* :`ssh-keygen -t rsa -b 4096 -C "seu_email_do_GitHub@example.com"`
   3. Pressione Enter
   4. Pressione Enter
   5. Pressione Enter

4. Adicione a nova chave SSH na sua conta do GitHub:

   1. No Git Bash: Copie o conteúdo do arquivo id_ed25519.pub:`clip < ~/.ssh/id_ed25519.pub`
   2. [No GitHub](https://github.com/settings/keys) : Seu perfil >> Configurações >> Chaves SSH e GPG >> Nova chave SSH
   3. Cole o conteúdo da chave pública

5. Teste a conexão SSH:

   1. Sem Git Bash:`ssh -T git@github.com`
   2. `yes`

6. Criação e configurações iniciais concluídas!