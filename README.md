# bruteforce-medusa-challenge.

## Objetivo
Este projeto simula, para fins didáticos, testes de autenticação com Medusa em serviços locais de laboratório no GitHub Codespaces.
## Ambiente utilizado
Laboratório executado em um GitHub Codespace com Ubuntu. Os testes foram feitos contra serviços locais do próprio Codespace (127.0.0.1).
## 1. Teste FTP
Alvo local: 127.0.0.1. O Medusa encontrou uma combinação válida para o usuário ftpuser na lista de teste; a senha do laboratório era uma credencial de teste.
## 2. Teste web (DVWA)
O DVWA foi configurado em nível baixo e testado apenas no ambiente local. O Medusa exibiu SUCCESS para uma tentativa, mas também retornou um erro; como o resultado não foi confirmado no formulário, ele é inconclusivo.
## 3. Teste SMB

 O compartilhamento local foi configurado. A consulta autenticada listou IPC$, mas não confirmou a listagem de share. O Medusa exibiu ACCOUNT FOUND junto de UNKNOWN ERROR CODE; por isso, o resultado é inconclusivo e não foi considerado confirmação independente.
 ## Wordlists
 Foram usadas listas pequenas com senhas genéricas, exclusivamente para testes no laboratório. Nenhuma senha pessoal foi incluída.
 ## Recomendações de mitigação
 FTP: preferir SFTP ou FTPS, usar senhas fortes e únicas e limitar tentativas de login. Aplicações web: aplicar limitação de tentativas, MFA e proteção CSRF. SMB: desativar SMB1, restringir o acesso à rede necessária e monitorar falhas de autenticação.
 ## Conclusão

 O laboratório permitiu praticar testes controlados e observar que resultados automatizados precisam ser validados. O teste FTP foi confirmado; os resultados web e SMB permaneceram inconclusivos. Os serviços foram testados localmente no Codespace.