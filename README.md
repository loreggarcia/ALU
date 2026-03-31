# Projeto: Unidade Lógica e Aritmética (ULA) de 8 bits

## Descrição do Projeto
Este projeto consiste no desenvolvimento de uma **Unidade Lógica e Aritmética (ULA)** de 8 bits, implementada no simulador **Digital**. A arquitetura segue o modelo de **Acumulador**, onde os resultados das operações são persistidos em um registrador principal para uso em cálculos sucessivos.

O projeto foi desenvolvido como parte da disciplina de Arquitetura de Computadores, sob orientação do **Prof. Rodrigo Nicola**.

---

## Arquitetura e Funcionamento

### 1. Registradores (AC e MQ)
Conforme as especificações do projeto, a ULA utiliza dois registradores de 8 bits:
* **AC (Acumulador):** Registrador principal que armazena o resultado de todas as operações e o realimenta para a entrada da ULA através do barramento `ACbus`.
* **MQ (Multiplier Quotient):** Registrador auxiliar utilizado para:
    * **Multiplicação:** Armazenar os 8 bits mais significativos (MSB).
    * **Divisão:** Armazenar o Quociente da operação (enquanto o AC armazena o Resto).

### 2. Unidade de Seleção (Opcode)
A escolha da operação é realizada através de um **Multiplexador (MUX)** de 8 entradas, controlado por um sinal de `Opcode`. As operações implementadas são:
* **Aritméticas:** Soma, Subtração, Multiplicação e Divisão.
* **Lógicas:** NAND e XOR.
* **Deslocamento:** Shift Left e Shift Right (Deslocamento Lógico).

### 3. Sinais de Status (Flags)
A ULA monitora constantemente o barramento de saída para fornecer informações de status ao processador:
* **Zero Flag (Z):** Implementada com uma porta NOR de 8 entradas, ativa quando o resultado é nulo.
* **Negative Flag (N):** Monitora o bit 7 (bit de sinal) do acumulador.
* **Carry Flag (C):** Indica o transbordamento (overflow) em operações de soma.

---

## Como Utilizar
1.  Abra o arquivo `ALU.dig` no simulador **Digital**.
2.  Inicie a simulação.
3.  Defina um valor na entrada **N**.
4.  Selecione a operação desejada através do **Opcode**.
5.  Pressione o botão de **Clock (C)** no registrador **AC** para gravar e acumular o resultado.
6.  Para operações de Multiplicação ou Divisão, observe também o registrador **MQ**.

---

## 🎥 Demonstração
[https://youtu.be/YDGzAldBYKk]

---

## 🎓 Autor
* **Nome:** Lorena Gabriela da Silva Garcia
