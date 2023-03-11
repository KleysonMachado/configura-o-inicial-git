# configura-o-inicial-git
Configuração para o Git
INSTALAÇÃO GIT
Entre no site oficial do GIT

  Escolha a opção Windows e o instalador será baixado automaticamente
  Mantenha as opções pré selecionadas 
  Próximo 
  Instalar
Antes de finalizar a instalação, selecione a opção "Lauch Git Bash"
No Git Bash, verifique se o GIT está instalado:git --version
configurações iniciais:
Configurar o nome do usuário:git config --global user.name "Seu nome"
Configure o endereço de e-mail (o mesmo do GitHub):git config --global user.email seu_email_do_GitHub@email.br
Verifique as configurações:git config --list
Instalação e configurações iniciais concluídas!
GERAR TOKEN DE ACESSO
Faça seu login no GitHub
Gere um token de acesso : Seu perfil >> Configurações >> Configurações do desenvolvedor >> Tokens de acesso pessoal >> Gerar novo token
Nota: Ecolha um nome para o token
Expiração: Sem expiração
Selecionar escopos: Selecione todos os campos
Gerar token
Copie uma String referente ao token
Aalve em um lugar seguro que você consiga consultar posteriormente
Criação e configurações iniciais concluídas!
GERAR CHAVE SSH
Consulte a documentação oficial
Verifique se existe alguma chave SSH em sua máquina:
Sem Git Bash:ls -al ~/.ssh
Se sim, para ser válido, o GitHub suporta qualquer um desses nomes de arquivos a seguir:
id_rsa.pub
id_ecdsa.pub
id_ed25519.pub
Caso não exista, gere uma chave SSH :
Sem Git Bash:ssh-keygen -t ed25519 -C "seu_email_do_GitHub@example.com"
Caso a opção acima não funcione :ssh-keygen -t rsa -b 4096 -C "seu_email_do_GitHub@example.com"
Pressione Enter
Pressione Enter
Pressione Enter
Adicione a nova chave SSH na sua conta do GitHub :
No Git Bash: Copie o conteúdo do arquivo id_ed25519.pub:clip < ~/.ssh/id_ed25519.pub
No GitHub : Seu perfil >> Configurações >> Chaves SSH e GPG >> Nova chave SSH
Cole o conteúdo da chave pública
Teste a conexão SSH:
Sem Git Bash:ssh -T git@github.com
yes
Criação e configurações iniciais concluídas!
