# Aplicação de Calculadora Simples

Esta é uma aplicação de calculadora simples construída usando Java Swing. A aplicação permite que os usuários realizem operações aritméticas básicas como adição, subtração, multiplicação e divisão. A interface do usuário foi projetada para ser intuitiva e fácil de usar.

## Funcionalidades

- **Adição**: Adiciona dois números.
- **Subtração**: Subtrai o segundo número do primeiro.
- **Multiplicação**: Multiplica dois números.
- **Divisão**: Divide o primeiro número pelo segundo.
- **Limpar**: Limpa todos os campos de entrada e saída.
- **Sair**: Encerra a aplicação.

## Interface do Usuário

A interface do usuário consiste nos seguintes componentes:

- **Campos de Entrada**: Dois campos de texto para inserir os valores a serem calculados (`txtvalor1` e `txtvalor2`).
- **Campo de Saída**: Um campo de texto para exibir o resultado do cálculo (`txttotal`).
- **Botões**:
  - `+` para adição
  - `-` para subtração
  - `x` para multiplicação
  - `/` para divisão
  - `Limpar` para limpar os campos
  - `Sair` para encerrar a aplicação

## Como Usar

1. **Inserir Valores**: Digite dois números nos campos `Valor 1` e `Valor 2`.
2. **Selecionar Operação**: Clique em um dos botões de operação (`+`, `-`, `x`, `/`).
3. **Ver Resultado**: O resultado será exibido no campo `Total`.
4. **Limpar Campos**: Clique no botão `Limpar` para limpar todos os campos.
5. **Encerrar Aplicação**: Clique no botão `Sair` para encerrar a aplicação.

## Visão Geral do Código

A classe principal `FrmCalculadora` estende `javax.swing.JFrame` e contém a lógica para inicializar os componentes e lidar com as ações do usuário. As operações aritméticas são implementadas dentro dos ouvintes de eventos dos respectivos botões.

### Inicialização

O método `initComponents` configura o layout e inicializa todos os componentes, incluindo rótulos, campos de texto e botões.

### Manipulação de Eventos

- **Adição**: 
  ```java
  private void btnsomaActionPerformed(java.awt.event.ActionEvent evt) {
      V1 = Double.parseDouble(txtvalor1.getText());
      V2 = Double.parseDouble(txtvalor2.getText());
      TOTAL = V1 + V2;
      txttotal.setText(String.valueOf(TOTAL));
  }
  ```

- **Subtração**: 
  ```java
  private void btnsubActionPerformed(java.awt.event.ActionEvent evt) {
      V1 = Double.parseDouble(txtvalor1.getText());
      V2 = Double.parseDouble(txtvalor2.getText());
      TOTAL = V1 - V2;
      txttotal.setText(String.valueOf(TOTAL));
  }
  ```

- **Multiplicação**: 
  ```java
  private void btnmultActionPerformed(java.awt.event.ActionEvent evt) {
      V1 = Double.parseDouble(txtvalor1.getText());
      V2 = Double.parseDouble(txtvalor2.getText());
      TOTAL = V1 * V2;
      txttotal.setText(String.valueOf(TOTAL));
  }
  ```

- **Divisão**: 
  ```java
  private void btndivActionPerformed(java.awt.event.ActionEvent evt) {
      V1 = Double.parseDouble(txtvalor1.getText());
      V2 = Double.parseDouble(txtvalor2.getText());
      TOTAL = V1 / V2;
      txttotal.setText(String.valueOf(TOTAL));
  }
  ```

- **Limpar Campos**: 
  ```java
  private void btnlimparActionPerformed(java.awt.event.ActionEvent evt) {
      txtvalor1.setText("");
      txtvalor2.setText("");
      txttotal.setText("");
  }
  ```

- **Encerrar Aplicação**: 
  ```java
  private void btnsairActionPerformed(java.awt.event.ActionEvent evt) {
      System.exit(0);
  }
  ```

## Como Executar

Para executar a aplicação, compile o arquivo Java e execute o método principal na classe `FrmCalculadora`. Certifique-se de que você tem o Java Development Kit (JDK) instalado em sua máquina.

```sh
javac FrmCalculadora.java
java FrmCalculadora
```
