
# US-012 - Cadastrar membros na plataforma

## Cenários de teste priorizados:
- [ ] Campos obrigatórios:
* Dado que o usuário acessa a página de registro
* Quando o usuário preenche apenas "Email" e "Senha"
* Então o sistema exibe uma mensagem de erro indicando que "Nome" e "Sobrenome" são obrigatórios

- [ ] Formato de e-mail:
* Dado que o usuário acessa a página de registro
* Quando o usuário preenche o campo "Email" com um formato inválido (ex: "email.com")
* Então o sistema exibe uma mensagem de erro indicando o formato incorreto do e-mail

- [ ] Formato de telefone (se fornecido):
* Dado que o usuário acessa a página de registro
* Quando o usuário preenche o campo "Telefone" com um formato inválido (ex: letras)
* Então o sistema exibe uma mensagem de erro indicando o formato incorreto do telefone
 - [ ] Registro bem-sucedido:
* Dado que o usuário acessa a página de registro
* Quando o usuário preenche "Nome", "Sobrenome", "Email" e "Senha" corretamente
* Então o sistema exibe uma mensagem de sucesso e envia um e-mail de confirmação

- [ ] Senha forte:
* Dado que o usuário acessa a página de registro
* Quando o usuário preenche o campo "Senha" com uma senha fraca (ex: "123456")
* Então o sistema exibe uma mensagem de erro indicando os critérios para uma senha forte

- [ ] E-mail de confirmação:
* Dado que o usuário se registrou com sucesso
* Quando o sistema processa o registro
* Então um e-mail de confirmação é enviado para o endereço fornecido
 - [ ] Link de descadastramento:
* Dado que o usuário recebeu o e-mail de confirmação
* Quando o usuário clica no link de descadastramento no e-mail
* Então o sistema remove o usuário da lista de e-mails e confirma a ação

-----

# US-015 - Recomendações

## Cenários de teste priorizados:

- [ ] Quantidade de recomendações:
* Dado que o usuário acessa a página inicial
* Quando a seção "Recomendações do Dia" é carregada
* Então o sistema exibe entre 4 e 5 filmes recomendados

- [ ] Conteúdo das recomendações:
* Dado que o usuário acessa a página inicial
* Quando a seção "Recomendações do Dia" é carregada
* Então cada recomendação inclui capa, título

- [ ] Atualização diária:
* Dado que é um novo dia
* Quando o usuário acessa a página inicial
* Então a seção "Recomendações do Dia" é atualizada com novos filmes (diferentes dos do dia anterior)

- [ ] Falha na atualização:
* Dado que a API do IMDB está indisponível
* Quando o sistema tenta atualizar as recomendações
* Então as recomendações do dia anterior são mantidas
