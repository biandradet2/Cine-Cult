# Fluxos de Navegação - Cine-Cult

---

## Visão Geral do Sistema

O Cine-Cult é um sistema de bilheteria digital que vende ingressos para o cinema e também permite a compra de produtos da bomboniere de forma integrada.

---

## Fluxo de Cadastro e Login

1. Usuário acessa o sistema
2. Realiza o cadastro com e-mail e cria uma senha
3. O sistema envia um e-mail de confirmação de senha
4. Usuário confirma a senha via e-mail
5. Login é salvo e o acesso à compra de ingressos é liberado

---

## Fluxo de Compra de Ingressos

1. Usuário logado acessa o painel de filmes disponíveis
2. O sistema exibe:
   - Filmes disponíveis
   - Data, horário, sala e preço
3. Usuário clica no filme desejado
4. O sistema exibe:
   - Preço do ingresso
   - Quantidade de ingressos disponíveis (respeitando a capacidade da sala)
5. Usuário seleciona a quantidade de ingressos que deseja comprar

---

## Fluxo de Compra na Bomboniere

1. Após selecionar os ingressos, o sistema exibe:
   - Produtos disponíveis na bomboniere
   - Preço de cada produto
   - Estoque disponível
2. Usuário seleciona os produtos desejados
3. O sistema atualiza automaticamente o estoque conforme a seleção

---

## Fluxo de Checkout e Pagamento

1. Sistema exibe tela de pagamento com:
   - Totalizador de valores (ingressos + bomboniere)
   - Resumo completo da compra
2. Usuário escolhe a forma de pagamento:
   - Pix
   - Cartão de crédito/débito
3. Usuário confirma a compra
4. Sistema finaliza a compra

---

## Fluxo de Confirmação e Entrega

1. Após a compra ser finalizada, o sistema:
   - Gera QR Code/código de confirmação
   - Envia por e-mail:
     - Ingresso digital
     - Nota fiscal com todos os produtos adquiridos

---

## Fluxo de Avaliação de Filmes

1. Usuário assiste ao filme no cinema
2. Acessa o sistema novamente
3. O sistema libera avaliação apenas para usuários que compraram ingressos para a sessão
4. Usuário pode:
   - Dar uma nota de 1 a 5 estrelas
5. A avaliação é publicada no site
6. Outros usuários podem interagir com a avaliação (curtir, comentar, etc.)
7. Usuários que NÃO assistiram ao filme também podem comentar e interagir nas avaliações

---

## 📊 Fluxograma Resumido
