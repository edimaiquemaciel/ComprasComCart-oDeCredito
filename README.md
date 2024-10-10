# Sistema de Controle de Cartão de Crédito

Este projeto é uma aplicação em Java que simula o controle de um cartão de crédito. Ele permite que o usuário faça compras com base em um limite de crédito e exibe uma lista das compras realizadas, além do saldo disponível no cartão.

## Funcionalidades

- Definir um limite de crédito para o cartão.
- Registrar compras e deduzir o valor do saldo disponível.
- Exibir uma lista ordenada das compras realizadas.
- Verificar o saldo restante no cartão.
- Impedir compras caso o saldo seja insuficiente.

## Tecnologias Utilizadas

- **Java 11** ou superior

## Como Executar

1. **Clone o repositório**:
   ```bash
   git clone https://github.com/edimaiquemaciel/ComprasComCartaoDeCredito.git
   ```

2. **Abra o projeto** na sua IDE favorita (Eclipse, IntelliJ IDEA, VSCode, etc.).

3. **Compile e execute** o arquivo `Principal.java`. O programa solicitará que você insira o limite do cartão e os detalhes das compras que deseja realizar.

4. **Exemplo de Execução**:
   O programa solicitará o limite do cartão e então pedirá que você insira a descrição e o valor das compras.

   Exemplo:
   ```bash
   Digite o limite do cartão: 
   1000

   Digite a descrição da compra: 
   Supermercado

   Digite o valor da compra: 
   200
   Compra realizada!

   Digite 0 para sair ou 1 para continuar
   1

   Digite a descrição da compra: 
   Restaurante

   Digite o valor da compra: 
   150
   Compra realizada!
   ```

   Quando o saldo do cartão não for suficiente, o programa exibirá a mensagem **"Saldo insuficiente!"** e encerrará o loop.

5. **Relatório Final**:
   Ao encerrar, o programa exibirá todas as compras realizadas e o saldo restante no cartão:

   ```bash
   **********************************
   COMPRAS REALIZADAS

   Restaurante - 150.0
   Supermercado - 200.0
   **********************************
   Saldo do cartão: 650.0
   ```

## Estrutura do Código

### 1. **Classe `Principal`**
   - Ponto de entrada do programa.
   - Interage com o usuário para definir o limite do cartão e registrar as compras.
   - Controla o fluxo de inserção de compras até que o saldo do cartão seja insuficiente ou o usuário escolha sair.

### 2. **Classe `Compra`**
   - Representa uma compra realizada com o cartão de crédito.
   - Contém a descrição e o valor da compra.
   - Implementa a interface `Comparable` para permitir a ordenação das compras com base no valor.

### 3. **Classe `CartaoDeCredito`**
   - Armazena o limite e o saldo do cartão.
   - Contém uma lista de compras realizadas.
   - Valida se uma compra pode ser realizada com base no saldo disponível.
   - Deduz o valor da compra do saldo disponível e a adiciona à lista de compras.

## Exemplo de Saída

Quando o programa é executado e o usuário realiza compras até atingir o limite, a saída será semelhante a esta:

```bash
Digite o limite do cartão: 
1000

Digite a descrição da compra: 
Livraria

Digite o valor da compra: 
250
Compra realizada!

Digite 0 para sair ou 1 para continuar
1

Digite a descrição da compra: 
Cinema

Digite o valor da compra: 
50
Compra realizada!

Digite 0 para sair ou 1 para continuar
1

Digite a descrição da compra: 
Roupas

Digite o valor da compra: 
800
Saldo insuficiente!

**********************************
COMPRAS REALIZADAS

Livraria - 250.0
Cinema - 50.0
**********************************
Saldo do cartão: 700.0
```

## Requisitos

- **Java 11** ou superior

## Possíveis Melhorias

- Adicionar validação para a entrada de valores (por exemplo, impedir que sejam inseridos valores negativos).
- Melhorar o sistema de persistência, salvando as compras realizadas em um arquivo para futuras consultas.
- Implementar um limite de parcelas para cada compra.

## Licença

Este projeto está licenciado sob os termos da licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.
