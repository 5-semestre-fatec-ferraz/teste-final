# Resumo do que o **Prof. Alexander** está pedindo e como o trabalho funciona:

### 1. Qual é a ideia geral do trabalho?
Vocês vão fazer a **engenharia reversa dos testes** de um sistema de Login que está em PHP (o repositório da Aula 08 já está salvo na sua máquina em `/var/www/html/teste-software/Aula-08`).

> **Regra de Ouro do Professor ("Sem PHP na Execução"):**
> Os arquivos `.php` servem **apenas para leitura** nas Fases 1 e 2. Nas Fases 3 e 4, o grupo deve reproduzir e rodar esses testes em **outra linguagem** (ex.: Python com `pytest`, Java com `JUnit` ou JS com `Jest`). **Não é necessário** criar banco de dados ou servidor web: basta criar funções/classes simples isoladas que representem a regra de negócio e testar essas funções.

---

### 2. O que precisa ser entregue em cada prazo?

#### **Etapa 1: Fases 1 e 2 (Prazo: até 19/11 às 23h59)**
*Nesta etapa **não precisa programar** (e o professor liberou o uso de IA para ajudar na leitura).*
1. **Criar a planilha `Registro_Execucao_Testes_Login_Grupo_[Letra].xlsx`** com uma aba chamada `Execucao_Testes` contendo **10 colunas (A até J)**.
2. **Preencher as Colunas A até G** analisando os arquivos de teste atribuídos ao seu grupo:
   - **A:** ID do Caso de Teste (`CT-C01`, `CT-C02`...)
   - **B:** Arquivo de Origem (ex.: `Ref: EmailTest.php -> Novo: test_dominio.py`)
   - **C:** Nome do método/cenário de teste
   - **D:** Regra verificada (objetivo em português claro)
   - **E:** Pré-condições e dados de entrada usados no teste
   - **F:** Técnica de Teste (*Caminho Feliz*, *Teste Negativo*, *Partição de Equivalência* ou *Valor Limite*)
   - **G:** Fonte da Verdade / Oráculo (*o resultado esperado cobrado pelo `assert`*)
3. **Criar 2 Novos Casos de Teste** na planilha (marcados como `NOVO` na Coluna B) cobrindo brechas extras da camada do seu grupo.
4. **Criar 1 Diagrama PlantUML** (`@startuml ... @enduml`) mostrando o fluxo de decisão das regras do grupo (onde passa pelo *Caminho Feliz* e onde barra nos *Testes Negativos/Limites*).
   - *Nota:* Na sua pasta já existe um rascunho em [fluxo-teste.puml](/diagramas/fluxo-teste.puml) (e em Mermaid em [fluxo-teste.mmd](/diagramas/fluxo-teste.mmd)).
---

#### **Etapa 2: Fases 3 e 4 (Laboratório: 20/11 e entrega final até 27/11)**
1. **Implementar os testes (sem PHP):** Escrever funções simples com as regras mapeadas + os testes automatizados (os originais + os 2 novos) na linguagem escolhida.
2. **Preencher as Colunas H, I e J da planilha:**
   - **H:** Comportamento Real obtido ao rodar o teste
   - **I:** Veredito (`Passou`, `Falhou`, etc.)
   - **J:** Prova de Execução (linhas do arquivo de teste + log/print do terminal passando)
3. **Apresentar funcionando no laboratório:** Mostrar o código rodando ao vivo e saber apontar na tela onde estão os **Dados de Entrada**, a **Técnica de Teste** e a **Fonte da Verdade (`assert`)**.

---

### 3. Escopo do seu grupo?
No arquivo [grupo.md](/grupo.md) vocês estão identificados como **Equipe 3** (Josias, Brino, João, Fernando e José Maurício). No roteiro do professor, as equipes são divididas nas letras **A, B, C, D e E**:

* **Equipe 3 = Grupo C (Camada de Domínio e Sanitização. 12 casos de teste)**. 

