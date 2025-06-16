
# Projeto Disciplina: Requisitos de Software

Olá! Este repositório faz parte do projeto da disciplina de Requisitos de Software da UTFPR - Campus Cornélio Procópio. 

> 🔗[Clique aqui para acessar o link do nosso Padlet!](https://padlet.com/rafaeltrevizan1/padlet-requisitos-m4hi5xqmfty6z5n6)

## 1. Introdução

***1.1.  Nome do Grupo***

| Participantes         | GitHub                                  |
|-----------------------|------------------------------------------|
| Felipe Gomes          | https://github.com/felipe-gomes0        |
| João Vitor Romani     | https://github.com/joaovitorrom          |
| Rafael Moraes         | https://github.com/trevizanrafael       |
| Samuel Ueno           | https://github.com/SamuelUenoUTFPR       |
| Werickson Souza       | https://github.com/Wericksonsd       |  

***1.2.  Nome do Sistema***

SAQA - Sistema Automatizado de Qualidade Alimentar

***1.3.  Propósito do Sistema***

O SAQA é um PAC (Programa de Auto Controle Digital), ou seja, o objetivo dele é auxiliar indústrias (no nosso caso, alimentícias) a terem um controle melhor da qualidade de sua linha de produção. Resumindo, nosso objetivo é aumentar o controle e organização dentro das indústrias alimentícias, otimizando o tempo gasto com essas atividades.

***1.4.  Público Alvo***

O público alvo do nosso Programa são executivos de indústrias alimentícias.

***1.5. Descrição dos usuários***

|<sub>PERFIL</sub>|<sub>Administrador do Sistema</sub>|<sub>Administrador da Empresa</sub>|<sub>Funcionário</sub>|
| :---: | :---: | :---: | :---: |
|<sub>Função</sub>|<sub>Garantir o funcionamento do sistema</sub>|<sub>Monitorar relatórios e métricas</sub>|<sub>Realizar tarefas específicas</sub>|
|<sub>Porcentagem de Usuários</sub>|<sub>2%</sub>|<sub>3%</sub>|<sub>95%</sub>|
|<sub>Faixa Etária</sub>|<sub>[25, 45]</sub>|<sub>[30, 55]</sub>|<sub>[18, 50]</sub>|
|<sub>Gênero</sub>|<sub>70% M, 30% F</sub>|<sub>70% M, 30% F</sub>|<sub>80% M, 20% F</sub>|
|<sub>Afinidade com a Tecnologia</sub>|<sub>90%</sub>|<sub>75%</sub>|<sub>60%</sub>|
|<sub>Frequência com que usará o sistema</sub>|<sub>Quando necessário</sub>|<sub>Diariamente</sub>|<sub>Diariamente</sub>|

***Personas:***
![1](https://github.com/user-attachments/assets/a922d68c-8eb2-452f-b06e-bf67a7e95064)
![2](https://github.com/user-attachments/assets/7a614170-d567-43e5-be8b-55e9151a8ebb)

***Cenário: Antes***

O cenário antes era de dificuldade em manter a conformidade dos Procedimentos Operacionais, além disso, todos as tarefas eram feitas por humanos manualmente, o que levava a um maior número de erros humanos. Além disso, o trabalho era excessivamente repetitivo e manual, então era dífical manter a motivação da equipe no trabalho.

***Cenário: Depois***

Com a aplicação a empresa conseguiu manter a equipe motivada, houve um aumento da produtividade e eficiência, além da diminuição de erros e mitigação de custos desnecessários. Além disso, nosso sistema trouxe a comodidade da integração com os web-services do governo, evitando a necessidade de trabalho manual para isso. A organização documental foi otimizada, pois o sistema possui um banco de dados capaz de gerar relatórios de forma automatizada.  

## 2. Documentos gerais no repositório

***2.1. Requisitos Funcionais***

| **Código** | **Descrição** | Depende de | **Prioridades** | 
|------------|---------------| ---------- | --------------- |
| **RF1**    | O Sistema deve permitir o gerenciamento de dados de produtos e processos, identificando claramente cada categoria (produto/processo) em interfaces e relatórios. | RF2, RF5, RF6 | **M** |
| **RF2**    | O Sistema deve automatizar a coleta de dados do processo industrial, por meio de integração com sensores de máquinas selecionados pelo usuário, sem intervenção manual. | | **M** |
| **RF3**    | O Sistema deve enviar notificações para usuários cadastrados, diariamente, caso parâmetros da produção estejam dentro dos limites pré-definidos pelo usuário. | RF2, RF5, RF6, RF8 | **S** |
| **RF4**    | O Sistema deve enviar dados para webservices do governo, diariamente, em formato compatível e com autenticação válida. (Verificar na **entrevista**) | RF2, RF5,RF6, RF8  | **M** |
| **RF5**    | O Sistema deve gerar relatórios de parâmetros dos processos, com filtros por período, unidade industrial e métricas críticas. | RF2 | **M** |
| **RF6**    | O Sistema deve armazenar histórico de todos os relatórios gerados, com capacidade de busca e exportação para análise posterior. | RF2, RF5 | **S** |
| **RF7**    | O Administrador do sistema será capaz de definir permissões para usuários do sistema, através de roles (ex: administrador, funcionário) e acesso a módulos específicos. | | **M** |
| **RF8**    | O Sistema deve validar a integridade de parâmetros dos relatórios, usando assinatura digital ou checksum para evitar manipulação. | RF2, RF5, RF6 | **S** |
| **RF9**    | O Sistema deve monitorar simultaneamente múltiplas unidades industriais, consolidando dados em um dashboard único. | RF2, RF4, RF6, RF8 | **C** |
| **RF10**   | O Sistema deve garantir backup automático do histórico de dados e relatórios, em ambientes redundantes (cloud/local) com política de retenção. | RF2, RF5, RF6, RF8  | **M** |

***2.2. Requisitos Não Funcionais***

| Código | Categoria      | Descrição                                                                 | Depende de | Prioridades |
|--------|----------------|---------------------------------------------------------------------------|------------|-------------|
| **RNF1**  | **Segurança**       | Autenticação com senha criptografada (ex: bcrypt, biblioteca de criptografia hash).                |     RNF2, RNF5, RNF6          | **M** 
| **RNF2**  | **Usabilidade**     | Interface responsiva e compatível com dispositivos móveis.        |               | **C**
| **RNF3**  | **Desempenho**      | Tempo de resposta inferior a 3 segundos, baseado no limite de requisições do sistema.     |     RNF2, RNF5, RNF6, RNF8         | **M**
| **RNF4**  | **Escalabilidade**  | Suporte a múltiplas unidades e usuários sem reconfiguração.       |     RNF2, RNF5, RNF6, RNF8          | **M**
| **RNF5**  | **Legal**           | Conformidade com a LGPD.                                          |      RNF2         | **M**
| **RNF6**  | **Confiabilidade**  | Disponibilidade mínima de 99% e mecanismo de retry em falhas.     |      RNF2, RNF5         | **M**
| **RNF7**  | **Integraçã**o      | Integração via REST com JSON e autenticação segura.               |               | **M**
| **RNF8**  | **Backup**          | Backups diários com retenção mínima de 90 dias e restauração rápida. |     RNF2, RNF5, RNF6       | **M**
| **RNF9**  | **Testabilidade**  | Arquitetura modular com suporte a testes unitários e de integração. |     RNF2, RNF4, RNF6, RNF8          | **S**
| **RNF10** | **Documentação**    | Manual técnico, tutorial de uso e especificações das APIs. |       RNF2, RNF5, RNF6, RNF8                | **S**



***2.3. Perguntas***

 > As perguntas se encontram no arquivo [perguntas.md](perguntas.md)!

***2.4. Entrevista***

| **Pergunta** | **Resposta** |
|-------------|--------------|
| Como é realizado atualmente o controle de qualidade na sua indústria? | A maioria das indústrias hoje não tem procedimentos formalizados de controle de qualidade, e o MA está começando a exigir isso. Normalmente, as empresas normalmente têm testes, como um teste laboratorial, olfativo, sensitivo, etc. Porém, a grande maioria não tem um procedimento padrão para isso, e, pior ainda, isso não é documentado, que é justamente o que o MA quer. |
| Quais são as maiores dificuldades enfrentadas no registro dos procedimentos dos PACs? | Partindo do princípio que 90% das indústrias hoje sequer tem um PAC, e, os 10% que tem, tem em planilhas impressas, no papel mesmo. No caso do entrevistado, no começo da indústria eram 93 planilhas que precisavam ser preenchidas manualmente todos os dias. Além desse trabalho todo, a informação do papel você não consegue extrair nada. No papel, acontece até mais erros que acertos. |
| Com que frequência ocorrem erros humanos ou esquecimentos no processo manual? | No papel, acontece até mais erros que acertos. |
| Como é feita a integração com órgãos do governo atualmente? Existem dificuldades ou atrasos? | Hoje, quase nenhuma indústria possui uma integração digital com os órgãos do governo. A integração das que têm PAC manual (papel) é com algum fiscal indo presencialmente, porém, mesmo que seja no papel, o mapa de produção de forma digital. |
| Quais funcionalidades você considera indispensáveis em um sistema de controle de qualidade alimentar? | O software precisa ser prático para operadores, porque muitas vezes o operador pode ser um semi-analfabeto que não vai entender muito bem a tecnologia, então tem que ser fácil e intuitivo. |
| Você considera importante a geração automática de alertas e relatórios? Por quê? | Importante sim, fundamental talvez não. Alerta é bom no sentido de, por exemplo, alguma verificação foi esquecida antes do dia acabar, aí lançaria uma notificação por push. E o relatório deve ser retirado quando quiser. |
| O que espera da integração automática com os Web Services do Governo Federal? | Atender a legislação, e o MA quer ter a possibilidade de fiscalizar a empresa sem precisar ir até ela. |
| Como gostaria que fosse o acesso ao histórico e busca por relatórios antigos? | Um requisito de muita importância, precisa conseguir os relatórios muito facilmente e rapidamente, esse é o objetivo do sistema. |
| Quais perfis de usuário você enxerga utilizando o sistema? (Administrador, Gerente, Operador, etc.) | Um bom sistema nesse sentido, não deveria se prender a isso, por exemplo, você poderia criar o cargo que quisesse e dar a ele as permissões que você quisesse. Nesse caso, o usuário da aplicação que conseguiria fazer isso tranquilamente, criar cargos conforme sua necessidade. |
| Que tipo de permissões ou acessos diferentes são necessários para cada perfil? | Como dito anteriormente, você deveria criar como quiser os cargos, e darem como fosse necessário as permissões. |
| Existe necessidade de treinamento para os usuários? Qual o nível de familiaridade deles com tecnologia? | São usuários com nível de tecnologia muito básico. |
| Que tipo de notificações são úteis para sua operação diária? | Alertas em caso de necessidade de terminar uma verificação. |
| Com que frequência você precisa de relatórios de produção e qualidade? | Diário. |
| Quais filtros e critérios são importantes nos relatórios (ex: período, unidade, parâmetros críticos)? | Depende da necessidade e cada caso do cliente, mas tem que poder filtrar pelas opções que quiser. |
| Quais sistemas ou máquinas você gostaria de integrar ao SAQA? | O custo de integrar máquinas medidoras é muito alto, para uma empresa pequena, não compensa nem um pouco, compensaria o trabalho manual de colocar na aplicação. Porém, empresas maiores, que possuem um capital maior e um maior mapa de produção, talvez compense. Então, seria outra coisa particular. |
| Existem APIs, sensores ou outros sistemas já em uso que deveriam ser integrados? | API apenas do governo. |
| Quais dados devem ser coletados automaticamente, sem intervenção manual? | Vai na mesma linha particular do primeiro item. |
| Quais preocupações de segurança você tem em relação ao sistema e aos dados? | O sistema tem que garantir que ninguém possa excluir ou alterar dados após que um monitoramento seja feito. Além disso, deve existir um sistema para verificar que, se porventura, alguém alterar ou apagar algum dado, tenho que conseguir saber quem foi. |
| Como deve ser feita a autenticação de usuários? Alguma preferência por métodos (senha, 2FA, etc.)? | A autenticação deve ser feita da maneira mais prática possível, não é necessário nenhuma autenticação muito maluca por não conter dados tão sensíveis. |
| Qual o tempo máximo aceitável de indisponibilidade do sistema? | Também outro caso que é particular de cada empresa. Se falar para um negócio pequeno que vai ficar uma hora sem o sistema, tudo certo. Porém, imagina se fosse com uma grande do mercado, como a Nestlé. |
| Com que frequência você considera adequado realizar backups dos dados? | Diário. |
| Em caso de falha, qual é o tempo máximo aceitável para restauração do sistema? | Horas. |
| O sistema deve suportar múltiplas unidades industriais? Como imagina o gerenciamento entre elas? | Seria uma funcionalidade a mais no sistema, porém, para o MA independente de ser o mesmo dono, mesma cidade ou mesmo CNPJ, não pode-se misturar entre dois “polos”. |
| Os usuários costumam acessar o sistema por desktop, tablet ou celular? | Todos os dispositivos. |
| Existe a necessidade de uma interface responsiva para dispositivos móveis? | Sim, com certeza. |
| Existem restrições de conectividade ou locais com acesso à internet limitado? | Hoje, todo lugar tem internet, porém, o sistema tem que conseguir performar seu melhor mesmo com uma pequena banda disponível. |
| Existem requisitos legais específicos que precisam ser atendidos além da LGPD? | Requisitos do MA. |
| Como o sistema pode ajudar a garantir a conformidade com essas normas? | O sistema ajuda no sentido de tirar as empresas dos PAC’s de papel, que podem-se perder, rasurar, entre outros. |


> 🔗[Clique aqui para acessar a gravação da entrevista completa!](https://drive.google.com/drive/folders/1iZ17ZPM2bwHytDvZfxwTb5VDQ5ByjceX)

***2.5. Histórias do Usuário***

| **ID**  | **Quem**                      | **O que**                                                                                                 | **Por quê**                                                                                                  |
|---------|-------------------------------|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| HU1     | Como usuário                  | Quero adicionar dados de produtos e processos                                                             | Para facilitar o controle e análise de informações em interfaces e relatórios                                |
| HU2     | Como gestor industrial        | Quero que o sistema colete automaticamente dados do processo industrial via integração com sensores       | Para evitar a intervenção manual e garantir precisão nas informações                                         |
| HU3     | Como usuário                  | Quero receber notificações diárias se os parâmetros de produção estiverem dentro dos limites definidos    | Para monitorar facilmente a conformidade e agir rapidamente em caso de anomalias                             |
| HU4     | Como gestor industrial        | Quero que o sistema envie dados diários para webservices do governo, em formato compatível e autenticado  | Para atender exigências legais e garantir a conformidade regulatória                                         |
| HU5     | Como usuário                  | Quero gerar relatórios de parâmetros dos processos, filtrando por período, unidade e métricas críticas    | Para analisar dados relevantes de forma segmentada e tomar decisões informadas                              |
| HU6     | Como usuário                  | Quero acessar o histórico dos relatórios com capacidade de busca e exportação                             | Para realizar análises posteriores e auditorias quando necessário                                            |
| HU7     | Como administrador de sistema | Quero definir permissões de acesso para os usuários, atribuindo roles e módulos específicos               | Para garantir segurança e controle de acesso adequado às informações e funcionalidades do sistema           |
| HU8     | Como gestor industrial        | Quero que o sistema valide a integridade dos relatórios usando assinatura digital ou checksum             | Para assegurar que os dados não foram manipulados e garantir confiança nas informações                      |
| HU9     | Como gestor industrial        | Quero monitorar múltiplas unidades industriais simultaneamente                                            | Para obter uma visão completa e rápida do desempenho de todas as unidades                                    |
| HU10    | Como usuário                  | Quero que o sistema faça backup automático dos dados e relatórios                                         | Para garantir a disponibilidade, segurança e recuperação das informações em caso de falha                   |

***2.6. Diagramas de Caso de Uso e Especificações***

![Imagem do WhatsApp de 2025-06-15 à(s) 23 11 01_8038560c](https://github.com/user-attachments/assets/7418dc78-6af3-4b27-8ecc-7678ab527ea4)
![Imagem do WhatsApp de 2025-06-15 à(s) 23 10 13_ddcc8a55](https://github.com/user-attachments/assets/b4510143-b860-4b62-9cb9-b523f7a9e1cf)
![Imagem do WhatsApp de 2025-06-15 à(s) 23 11 11_99643ecc](https://github.com/user-attachments/assets/dee5e144-75c9-4a3f-9746-48ba86ca890a)


***2.7. Diagramas de Atividades***

![REGISTRO DO PAC](https://github.com/user-attachments/assets/c0beadbb-1b66-4d79-bc87-384e3796654d)
![image](https://github.com/user-attachments/assets/f9aa823b-f6fd-4edc-8e56-051ca079031b)
![diagrama de atividades registro de dados](https://github.com/user-attachments/assets/2dd2fc6b-7ffa-43d7-9259-895eb108a6f7)



***2.8. Matrizes de Rastreabilidade***

A matriz indica com um "**X**" quais Casos de Uso são necessários para satisfazer cada Requisito.

**Requisitos Funcionais vs. Casos de Uso**

| **Requisito Funcional** | **UC1** | **UC2** | **UC3** | **UC4** | **UC5** | **UC6** | **UC7** |
| :---------------------- | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: |
| **RF1** - Gerenciar dados de produtos e processos |         |         | **X** |         |         |         | **X** |
| **RF2** - Automatizar coleta de dados (sensores)   | **X** |         |         |         |         |         |         |
| **RF3** - Enviar notificações de conformidade      |         | **X** |         |         |         |         |         |
| **RF4** - Enviar dados para webservices do governo |         |         |         | **X** |         |         |         |
| **RF5** - Gerar relatórios parametrizados          |         | **X** |         | **X** |         |         |         |
| **RF6** - Armazenar histórico de relatórios        |         | **X** |         | **X** |         |         |         |
| **RF7** - Definir permissões de usuários (roles)   |         |         |         |         | **X** | **X** |         |
| **RF8** - Validar integridade de relatórios        |         |         |         | **X** |         |         |         |
| **RF9** - Monitorar múltiplas unidades             | **X** | **X** | **X** |         |         |         | **X** |
| **RF10** - Realizar backup automático              |         |         | **X** | **X** |         |         |         |


**Requisitos Não Funcionais vs. Casos de Uso**

| **Requisito Não Funcional** | **UC1** | **UC2** | **UC3** | **UC4** | **UC5** | **UC6** | **UC7** |
| :--------------------------- | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: | :-----: |
| **RNF1** - Segurança (Criptografia de senha) |         |         |         |         | **X** |         |         |
| **RNF2** - Usabilidade (Interface responsiva) | **X** | **X** | **X** | **X** | **X** | **X** | **X** |
| **RNF3** - Desempenho (Resposta < 3s)       | **X** | **X** | **X** | **X** | **X** | **X** | **X** |
| **RNF4** - Escalabilidade (Múltiplas unidades) | **X** | **X** | **X** | **X** |         |         | **X** |
| **RNF5** - Legal (Conformidade com LGPD)    |         |         | **X** |         | **X** | **X** |         |
| **RNF6** - Confiabilidade (Disponibilidade 99%)| **X** | **X** | **X** | **X** | **X** | **X** | **X** |
| **RNF7** - Integração (API REST)            | **X** | **X** |         | **X** |         |         |         |
| **RNF8** - Backup (Diários com retenção)    | **X** |         | **X** | **X** | **X** | **X** | **X** |
| **RNF9** - Testabilidade (Arquitetura modular)| **X** | **X** | **X** | **X** | **X** | **X** | **X** |
| **RNF10** - Documentação (Manuais e API)     | **X** | **X** | **X** | **X** | **X** | **X** | **X** |


***3.0. Protótipos***

> 🔗[Clique aqui para acessar a apresentação do nosso protótipo!](Mockup-apresentação.pdf)

***3.1. Pitch***
> 🔗[Clique aqui para conferir nossa apresentação em formato de Pitch!](PitchSAQA.pdf)

## Referências

- SOMMERVILLE, Ian. Engenharia de software. 9. ed. São Paulo, SP: Pearson Prentice Hall, 2011.

- Guedes, T. A. UML 2 – Uma abordagem Prática. 2. ed. São Paulo: Novatec, 2011.

- Reinehr, Sheila. Engenharia de requisitos. Disponível em: Minha Biblioteca, Grupo A, 2020.

