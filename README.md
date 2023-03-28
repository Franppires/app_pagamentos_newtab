Projeto individual: React


O objetivo é construir uma aplicação que simula o envio de dinheiro para uma outra pessoa, via cartão de crédito.
Fluxo das telas
Na primeira tela terá uma listagem de usuários, onde a pessoa pode clicar em algum usuário da lista para realizar o pagamento. Quando clicado em um usuário é então aberto um modal de pagamento, contendo as informações do usuário de destino, a opção de selecionar um cartão de crédito e um botão de pagar. O usuário deve então digitar o valor, escolher o cartão e clicar em pagar. Para realização do pagamento deve-se chamar um endpoint de pagamento que aprovará/recusará a transação. E então deve-se mostrar na tela o modal de pagamento concluído com sucesso ou o de erro.
Screenshots:
Lista de usuários


Modal de pagamento e listagem de cartões


Modal de pagamento concluído com sucesso



Modal de erro no pagamento


Cartões para exibir
O cartão válido vai aprovar a transação no backend;
let cards = [
  // valid card
  {
    card_number: '1111111111111111',
    cvv: 789,
    expiry_date: '01/18',
  },
  // invalid card
  {
    card_number: '4111111111111234',
    cvv: 123,
    expiry_date: '01/20',
  },
];
Transação
Endpoint: https://run.mocky.io/v3/533cd5d7-63d3-4488-bf8d-4bb8c751c989
Método: POST
// Payload:

interface TransactionPayload {
  // Card Info
  card_number: string;
  cvv: number;
  expiry_date: string;

  // Destination User ID
  destination_user_id: number;

  // Value of the Transaction
  value: number;
}
Obs: Por se tratar de um mock o endpoint sempre retornará o mesmo payload, sucesso no pagamento, independente do cartão
Usuários
Endpoint: https://www.mocky.io/v2/5d531c4f2e0000620081ddce
Método: GET
// Payload:

interface User {
  id: number;
  name: string;
  img: string;
  username: string;
}


Divisão de atividades

Abaixo sugerimos uma divisão de atividades que pode facilitar sua organização e desenvolvimento do projeto.

ATIVIDADE 1 – REACT:
Desenvolvimento da página de listagem de usuários

ATIVIDADE 2 – REACT:
Desenvolvimento das páginas de pagamentos e recibos

Prazos das atividades

Para as atividades, considerando uma dedicação de 3 a 4 horas por dia, estimamos que seja possível que você consiga realizá-las em aproximadamente uma semana cada. Se conseguir antes, fantástico! O prazo para terminar este módulo você já conhece.

Sempre que tiver dúvidas, lembre-se dos nossos recursos no Discord e facilitadores para te apoiar.

Você deverá enviar o link do seu repositório no Github e da página publicada (Github Pages ou Netlify) com as atividades solicitadas no formulário da plataforma.

