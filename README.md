# ⏰ Relógio Digital com Cronômetro e Alarme - Intel 8085

Este repositório contém o código-fonte e arquivos relacionados ao projeto de um **Relógio Digital com funcionalidades de Cronômetro e Alarme**, desenvolvido em **Assembly para o microprocessador Intel 8085**, como parte da disciplina de **Microcontroladores** do curso de **Engenharia de Computação** do Instituto Federal de Minas Gerais - Campus Bambuí.

## 🛠️ Tecnologias e Ferramentas

- **Assembly 8085**
- **Simulador Abacus**
- **Microprocessador Intel 8085 (emulação)**

## 📋 Funcionalidades

- Contagem sequencial de tempo (relógio) em horas e minutos.
- Cronômetro com contagem regressiva ativado de três formas:
  - Valor manual (via interrupção RST 5.5).
  - Tempo pré-definido de **15 minutos** (via RST 6.5).
  - Tempo pré-definido de **30 minutos** (via RST 7.5).
- Alarme visual com LEDs ativados ao final do cronômetro.
- Desativação do alarme via interrupção `TRAP`.
- Manipulação de pilha com salvamento/restauração dos registradores.

## 📂 Estrutura do Projeto

- `relogio_digital.asm` — Código-fonte em Assembly.
- `relogio_digital.hex` — Arquivo compilado para uso no simulador.
- `Relatório - Andressa e Hugo.pdf` — Documento completo com o desenvolvimento, testes e análise do projeto.

## ▶️ Como Executar

1. Abra o simulador **Abacus**.
2. Importe o arquivo `relogio_digital.hex`.
3. Execute o programa e utilize as interrupções para ativar o cronômetro:
   - RST 5.5: permite digitar manualmente o tempo.
   - RST 6.5: inicia o cronômetro com 15 minutos.
   - RST 7.5: inicia o cronômetro com 30 minutos.
4. O alarme será ativado visualmente ao final da contagem regressiva.
5. Utilize a interrupção **TRAP** para desativar o alarme e retornar ao modo relógio.

## 📌 Endereços de Interrupções Customizados

| Interrupção | Endereço  |
|-------------|-----------|
| RST 5.5     | 20F1H     |
| RST 6.5     | 20F7H     |
| RST 7.5     | 2108H     |
| TRAP        | 2119H     |

## 👩‍💻 Desenvolvedores

- **Andressa Lopes**
- **Hugo César**

## 📜 Licença

Projeto acadêmico desenvolvido para fins educacionais. Uso livre para estudo e extensão.

---

