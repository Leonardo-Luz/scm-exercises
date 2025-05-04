# Avaliação 1

* Curso: Tecnólogo ADS
* Disciplina: Sistemas de Gerência de Configuração (2025)
* Professor: Roger Urdangarin
* Aluno(a): Leonardo Luz

## Questões

1) (Questão) O que é a gerência de configuração e quais são as suas 6 subáreas?

- Gerência de Código Fonte
- Engenharia de Build
- Configuração do Ambiente
- Controle de Mudanças
- Gerenciamento de Releases
- Deployment

2) (Questão) Quais critérios determinam que um artefato de software deve ser classificado como Item de Configuração (IC), e cite três exemplos mencionados?

* Cada um dos elementos que são criados durante o desenvolvimento do software. Exemplos:
- um documento de texto
- uma especificação do sistema
- um arquivo de código-fonte

3) (Questão) Quais as duas estratégias mais comuns para realizar o versionamento do código fonte no que diz respeito a infra-estrutura (bases, repositórios)?

Repositório Remoto e Repositório Local.

4) (Questão) O que deve acontecer para que uma nova versão para um item de configuração seja criada no repositório?

Deve ocorrer o checkout.

5) (Questão) Como as fases do ciclo de vida de software (Requisitos, Desenvolvimento, Testes, Implantação e Manutenção), relacionam-se com a gerência de configuração?

A gerência de configuração controla e acompanha as mudanças em cada fase do ciclo de vida de software. Em cada etapa (requisitos, desenvolvimento, testes, implantação e manutenção), ela garante que as versões dos artefatos sejam rastreadas, controladas e auditáveis.

6) Estudo de Caso: **Caos na TechFlow Solutions**

A TechFlow Solutions é uma empresa de desenvolvimento de software de médio porte que cria aplicativos customizados para diversos clientes. A empresa tem 50 desenvolvedores trabalhando em múltiplos projetos simultaneamente. Porém, a TechFlow atualmente não usa nenhum sistema de Gerenciamento de Configuração de Software. A seguir uma lista de problemas recorrentes identificados no cotidiano da TechFlow:

1. Alterações de código perdidas: Desenvolvedores sobrescrevem o trabalho uns dos outros ao mesclar arquivos manualmente por e-mail ou pastas compartilhadas.

2. Falta de rastreabilidade: Bugs aparecem em produção, mas ninguém sabe qual mudança os causou.

3. Conflitos em dados compartilhados – Várias equipes modificam a mesma biblioteca compartilhada sem coordenação, causando falhas na integração.

4. Atualizações simultâneas – Dois desenvolvedores corrigem o mesmo bug independentemente, e uma alteração sobrescreve a outra correção feita no mesmo código.

5. Falhas graves em releases (Entregas do Sistema) – A versão errada de um módulo é implantada, causando quedas e defeitos no funcionamento do sistema no ambiente da Produção.

- Abaixo o relato de um incidente crítico ocorrido com a empresa e um de seus clientes:

O cliente da TechFlow, SafeBank, solicitou um patch de segurança urgente. Duas equipes trabalharam na correção: A Equipe A salvou suas alterações em um arquivo compactado patch_final_v2. A Equipe B salvou a deles em outro arquivo zipado, patch_final_FIX_REAL. A administração dos sistemas implantou em uma janela de instalação o patch_final_v2, que estava incompleto causando uma queda do sistema, a qual custou ao SafeBank um prejuízo estimado de US$ 500.000 em tempo de inatividade. Considerando as informações anteriores responda adequadamente às questões abaixo:

1. (Questão) Como um sistema de controle de versão (ex.: Git, Mercurial) poderia evitar o problema de "alterações de código perdidas" descrito no estudo de caso?

Um sistema de controle de versão rastreia todas as alterações de código, permitindo que os desenvolvedores trabalhem em diferentes partes do código simultaneamente sem sobrescrever o trabalho um do outro. Ao mesclar as alterações, o sistema detecta possiveis conflitos que podem ser corrigidos, prevenindo a perda de código.

2. (Questão) Quais práticas de GCS ajudariam a empresa TechFlow a rastrear qual desenvolvedor introduziu um bug em produção?

Controle de versão (Git) e logs detalhados de alterações.

3. (Questão) Explique como um repositório remoto (como o GitHub) pode resolver os problemas de "dados compartilhados" e "atualização simultânea".

Um repositório remoto como o GitHub permite que várias pessoas trabalhem no mesmo código simultaneamente, sem sobrescrever o trabalho umas das outras.  Ele armazena todas as versões do código, permitindo o acompanhamento das alterações e a resolução de conflitos de forma organizada.  Cada pessoa faz suas alterações em sua própria cópia, e depois as envia para o repositório central.
