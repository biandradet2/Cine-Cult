# Histórias de Usuário - Cine-Cult

## 1. Épico: Cadastro e Autenticação

### US01 - Cadastro de Novo Usuário
**História:** **Como** um novo visitante, eu **quero** me cadastrar utilizando meu e-mail e criando uma senha, **para** que eu possa criar uma conta no sistema.

**Critérios de Aceite:**
* O sistema deve apresentar um formulário solicitando e-mail e senha.
* O sistema deve validar se o e-mail inserido tem um formato válido.
* Ao finalizar o cadastro, o sistema deve bloquear o acesso às compras até a confirmação do e-mail.

### US02 - Confirmação de E-mail
**História:** **Como** um usuário recém-cadastrado, eu **quero** receber um e-mail de confirmação, **para** que eu possa validar minha conta e ativar meu login.

**Critérios de Aceite:**
* O sistema deve enviar automaticamente um e-mail com um link ou token de confirmação.
* Ao clicar no link/token, a conta do usuário deve ser ativada.
* Após a confirmação, o sistema deve liberar o acesso ao painel de compra de ingressos.

### US03 - Login no Sistema
**História:** **Como** um usuário cadastrado e validado, eu **quero** fazer login com meu e-mail e senha, **para** que eu possa acessar o painel de filmes e realizar compras.

**Critérios de Aceite:**
* O sistema deve autenticar as credenciais informadas.
* O login deve ser mantido salvo durante a sessão de navegação.

---

## 2. Épico: Compra de Ingressos

### US04 - Visualização do Catálogo de Filmes
**História:** **Como** um usuário logado, eu **quero** visualizar o painel de filmes disponíveis, com detalhes de data, horário, sala e preço, **para** que eu possa escolher a melhor sessão para mim.

**Critérios de Aceite:**
* O sistema deve exibir a listagem apenas de filmes em cartaz e com sessões ativas.
* As informações obrigatórias na tela são: Título, Data, Horário, Sala e Preço base.

### US05 - Seleção de Ingressos
**História:** **Como** um usuário logado, eu **quero** selecionar a quantidade de ingressos para um filme específico, **para** que eu possa garantir meus lugares na sala.

**Critérios de Aceite:**
* Ao clicar em um filme, o sistema deve exibir a quantidade de ingressos ainda disponíveis para a sessão.
* O sistema não pode permitir a seleção de uma quantidade de ingressos maior do que a capacidade restante da sala.
* O sistema deve exibir o valor total parcial baseado na quantidade escolhida.

---

## 3. Épico: Compra na Bomboniere

### US06 - Adição de Produtos da Bomboniere
**História:** **Como** um usuário comprando ingressos, eu **quero** visualizar os produtos da bomboniere, seus preços e estoque, **para** que eu possa adicionar lanches à minha compra.

**Critérios de Aceite:**
* A tela da bomboniere deve aparecer logo após a confirmação dos ingressos.
* O sistema deve exibir apenas produtos com estoque maior que zero.
* O usuário pode selecionar as quantidades desejadas de cada produto.

### US07 - Reserva Automática de Estoque
**História:** **Como** sistema, eu **quero** atualizar o estoque dos produtos da bomboniere automaticamente conforme a seleção do usuário, **para** que eu possa evitar a venda de produtos esgotados.

**Critérios de Aceite:**
* Ao selecionar um produto, o estoque disponível exibido na tela deve diminuir.
* Se o usuário remover o item da cesta antes do pagamento, o estoque deve retornar ao normal.

---

## 4. Épico: Checkout e Pagamento

### US08 - Resumo e Totalizador da Compra
**História:** **Como** um usuário no processo de checkout, eu **quero** visualizar um resumo completo da minha compra contendo ingressos e produtos da bomboniere, **para** que eu possa conferir os valores totais antes de pagar.

**Critérios de Aceite:**
* O sistema deve exibir a descrição e valor dos ingressos.
* O sistema deve exibir a descrição e valor dos itens da bomboniere.
* O sistema deve exibir o Valor Total (Soma de Ingressos + Produtos).

### US09 - Pagamento da Compra
**História:** **Como** um usuário finalizando a compra, eu **quero** poder escolher entre pagar com Pix ou Cartão de Crédito/Débito, **para** que eu possa concluir minha transação com o método da minha preferência.

**Critérios de Aceite:**
* O sistema deve oferecer as opções "Pix" e "Cartão de Crédito/Débito".
* O sistema deve processar o pagamento e, mediante sucesso, registrar a compra como "Finalizada".

---

## 5. Épico: Confirmação e Entrega

### US10 - Emissão de Ingresso Digital e Nota Fiscal
**História:** **Como** um cliente com a compra finalizada, eu **quero** receber um QR Code de acesso e a nota fiscal da compra por e-mail, **para** que eu possa entrar no cinema e retirar meus produtos na bomboniere.

**Critérios de Aceite:**
* O sistema deve gerar um QR Code único e rastreável atrelado àquela compra.
* O sistema deve enviar um e-mail contendo: O ingresso digital (QR Code) e a Nota Fiscal discriminando ingressos e produtos da bomboniere.

---

## 6. Épico: Avaliação de Filmes (Comunidade)

### US11 - Avaliação Exclusiva para Espectadores
**História:** **Como** um usuário que comprou o ingresso e assistiu ao filme, eu **quero** poder dar uma nota de 1 a 5 estrelas e publicar minha avaliação no site, **para** que eu possa compartilhar minha experiência.

**Critérios de Aceite:**
* O sistema deve verificar se o usuário logado possui um ingresso pago para aquele filme antes de liberar o campo de nota (estrelas).
* A avaliação, uma vez submetida, deve ficar pública na página do filme.

### US12 - Interação Social (Curtidas e Comentários)
**História:** **Como** um usuário da plataforma (tendo ou não assistido ao filme), eu **quero** poder curtir, comentar e interagir nas avaliações de outros usuários, **para** que eu possa participar das discussões da comunidade Cine-Cult.

**Critérios de Aceite:**
* A sessão de comentários/curtidas abaixo da avaliação de um usuário deve estar liberada para qualquer usuário com uma conta válida e logada.
* Usuários sem ingresso comprado para aquele filme específico podem interagir com as avaliações, mas não podem emitir uma nota de 1 a 5 estrelas.
