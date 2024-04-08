# Javascript
## Como rodar os testes

No terminal, execute os comandos:

```bash
cd javascript
yarn
yarn test
```

Ou usando o NPM:

```bash
cd javascript
npm install
npm test
```
Decisões tomadas no processo de resolução do desafio:

Passo 1:
Primeira ação necessária foi a de remover os CS's indisponíveis garantindo que ficassem somente os disponíveis para atenderem os clientes.
Para isso, utilizei o método filter() que permite que filtremos um array utilizando outro array como parâmetro e retornei um novo array contendo apenas os CS's livres.

Passo 2:
Utilizei o método sort() para ordenar os CS'S e os clientes de maneira que o score fique ascendente. Essa decisão foi necessária pois irá ajudar a cumprir as regras de negócio exigidas: de que o cliente com menor score deve ser antendido pelo CS's de menor score compatível a ele e que alguns clientes podem ficar sem atendimento caso não existam CS's com nivel adequado para atende-los.

Passo 3: 
Criei uma nova estrutura de map() para armazenar quais clientes serão atendidos por CS e usei o método set() para atribuir o ID do array customerSuccessAvaiable da nova estrutura.

Passo 4:
Adicionei um loop que percorre o array costumers e compara com o array customerSuccessAvaiable os scores. Caso o score do cliente seja menor ou igual ao CS ele atribui o cliente ao CS. Se o CS atual não tiver score para atendê-lo ele vai passar para o próximo e se caso não haja nenhum CS com score suficiente para atendê-lo o laço é interrompido, tendo em vista que clientes com scores maiores que ele também não terão CS's aptos a atendê-los.

Passo 5:
Através de um forEach() percorri o array  customerSuccessMatch para descobrir qual CS possuía o maior número de clientes associado. Caso o CS atual tenha o maior valor a variável CustomerSuccesswithMoreCustomers armazena seu ID e pula pro próximo. Se existirem dois CS's com quantidade máxima igual o laço retorna 0 de acordo com as regras de negócio. 

