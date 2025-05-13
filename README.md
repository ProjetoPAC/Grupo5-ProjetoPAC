
# Projeto Disciplina: Requisitos de Software

Olá! Este repositório faz parte do projeto da disciplina de Requisitos de Software da UTFPR - Campus Cornélio Procópio. 

Link do Padlet: https://padlet.com/rafaeltrevizan1/padlet-requisitos-m4hi5xqmfty6z5n6

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

O SAQA é um PAC (Progrma de Auto Controle Digital), ou seja, o objetivo dele é auxiliar indústrias (no nosso caso, alimentícias) a terem um controle melhor da qualidade de sua linha de produção. Resumindo, nosso objetivo é aumentar o controle, organização dentro das indústrias alimentícias e diminuir o tempo que seria gasto com esses ajustes.

***1.4.  Público Alvo***

O público alvo do nosso Programa é donos de indústrias alimentícias.

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

| **Código** | **Descrição** |
|------------|---------------|
| **RF1**    | O Sistema deve permitir o gerenciamento de dados de produtos e processos, identificando claramente cada categoria (produto/processo) em interfaces e relatórios. |
| **RF2**    | O Sistema deve automatizar a coleta de dados do processo industrial, por meio de integração com sensores/APIs de máquinas, sem intervenção manual. |
| **RF3**    | O Sistema deve enviar notificações para usuários cadastrados, diariamente, caso parâmetros da produção estejam dentro dos limites pré-definidos. |
| **RF4**    | O Sistema deve enviar dados para webservices do governo, diariamente, em formato compatível e com autenticação válida. |
| **RF5**    | O Sistema deve gerar relatórios de parâmetros dos processos, com filtros por período, unidade industrial e métricas críticas. |
| **RF6**    | O Sistema deve armazenar histórico de todos os relatórios gerados, com capacidade de busca e exportação para análise posterior. |
| **RF7**    | O Administrador deve definir permissões para usuários do sistema, através de roles (ex: operador, gerente) e acesso a módulos específicos. |
| **RF8**    | O Sistema deve validar a integridade de parâmetros dos relatórios, usando assinatura digital ou checksum para evitar manipulação. |
| **RF9**    | O Sistema deve monitorar simultaneamente múltiplas unidades industriais, consolidando dados em um dashboard único. |
| **RF10**   | O Sistema deve garantir backup automático do histórico de dados e relatórios, em ambientes redundantes (cloud/local) com política de retenção. |

***2.2. Requisitos Não Funcionais***

| Código | Categoria      | Descrição                                                                 |
|--------|----------------|---------------------------------------------------------------------------|
| **RNF1**  | **Segurança**       | Autenticação com senha criptografada (ex: bcrypt).                        |
| **RNF2**  | **Usabilidade**     | Interface responsiva e compatível com dispositivos móveis.               |
| **RNF3**  | **Desempenho**      | Tempo de resposta inferior a 3 segundos em condições normais.            |
| **RNF4**  | **Escalabilidade**  | Suporte a múltiplas unidades e usuários sem reconfiguração.              |
| **RNF5**  | **Legal**           | Conformidade com a LGPD.                                                 |
| **RNF6**  | **Confiabilidade**  | Disponibilidade mínima de 99% e mecanismo de retry em falhas.            |
| **RNF7**  | **Integraçã**o      | Integração via REST com JSON e autenticação segura.                      |
| **RNF8**  | **Backup**          | Backups diários com retenção mínima de 90 dias e restauração rápida.     |
| **RNF9**  | **Testabilidade**  | Arquitetura modular com suporte a testes unitários e de integração.      |
| **RNF10** | **Documentação**    | Manual técnico, tutorial de uso e especificações das APIs.               |



***2.3. Perguntas***

*<Arquivo com as perguntas realizadas na entrevista .>*

***2.4. Entrevista***

*<Arquivo com as respostas do indivíduo entrevistado e link do drive com upload da gravação.>*

***2.5. Histórias do Usuário***

*<Imagem, arquivo (PDF), link com as Histórias de Usuário.>*

***2.6. Diagramas de Caso de Uso e Especificações***

*<Imagem, arquivo (PDF), link com Diagrama de Caso de Uso.>*

***2.7. Diagramas de Atividades***

*<Imagem, arquivo (PDF), link com Diagrama de Atividades.>*

***2.8. Matrizes de Rastreabilidade***

*<Imagem, arquivo (PDF), link com Matriz de Rastreabilidade.>*

***2.9. Protótipos***

*<Imagem, arquivo (PDF), link com Protótipo.>*

## Referências

*<Esta seção é destinada à descrição das referências utilizadas pelo documento, como por exemplo, URLs e livros. Ver exemplo a seguir:>*

[1] “Glossário da _USina_”, <_id_doc glossário_>, Versão <_versão_>. Localização: <_localização_>.
