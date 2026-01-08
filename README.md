# Sentinela_Digital_Ciberseguranca-
Simulação de defesa cibernética contra ataques de enxame de IA, com foco em análise comportamental e logging
# 🛡️ Sentinela Digital: Defesa Cibernética contra Enxames de IA

## Sobre o Projeto

Este projeto foi desenvolvido como parte dos meus estudos em **Inteligência Artificial e Big Data na PUC-GO**, com um foco especial em **Cibersegurança** (na perspectiva de um "Hacker do Bem"). Ele explora a crescente ameaça dos "enxames de ciberataques" impulsionados por IA, conforme alertado por empresas como a Lumu Technologies para 2026.

O objetivo é demonstrar, através de uma simulação prática em Python, como as defesas tradicionais podem falhar contra ataques coordenados e como a análise comportamental e o cruzamento de dados são cruciais para construir sistemas de segurança mais resilientes.

## O Problema: A Era dos Enxames de IA (2026)

Relatórios recentes [1] preveem que, até 2026, a Inteligência Artificial Generativa industrializará o cibercrime, permitindo que atacantes lancem "enxames" de ataques autônomos. Estes ataques são caracterizados por:

*   **Automação Ofensiva Total:** IAs agindo como "generais" comandando exércitos de "drones" autônomos, varrendo redes em busca de vulnerabilidades.
*   **Phishing Hiper-Personalizado:** IAs cruzando dados vazados (Big Data) para criar e-mails de phishing indistinguíveis de comunicações legítimas.
*   **Malware Polimórfico:** Vírus que reescrevem seu próprio código constantemente, tornando antivírus baseados em assinaturas ineficazes.

Contra essa ameaça, defesas baseadas em regras fixas ou na análise humana são lentas e ineficazes.

## A Solução: O Sentinela Digital (Evolução)

Desenvolvi um algoritmo de defesa em Python, apelidado de "Sentinela Digital", que evoluiu em duas fases para combater a sofisticação dos ataques:

### Fase 1: Sentinela Básico (Bloqueio por IP)

Uma primeira versão do Sentinela implementava um bloqueio simples baseado no limite de requisições por IP em uma janela de tempo. No entanto, esta abordagem falhou miseravelmente contra um ataque simulado de "enxame" que utilizava rotação rápida de IPs (botnets).

### Fase 2: Sentinela Híbrido (Análise Comportamental - IP + Usuário)

Reconhecendo a falha da defesa inicial, o Sentinela foi aprimorado para realizar uma **análise comportamental híbrida**, correlacionando tentativas de acesso não apenas por IP, mas também pelo **usuário alvo**. Mesmo com IPs rotativos, o sistema agora é capaz de identificar que uma mesma conta de usuário está sob ataque massivo, bloqueando os IPs coordenadamente.

Esta evolução demonstra o princípio de que, na era da "Guerra de Algoritmos", a defesa precisa ser tão inteligente e adaptável quanto o ataque, utilizando **Big Data** para identificar padrões anômalos que um humano não conseguiria.

## Stack Tecnológica

*   **Python:** Linguagem principal para o desenvolvimento do algoritmo.
*   **`collections.defaultdict`:** Para armazenar logs de acesso em memória.
*   **`datetime` e `timedelta`:** Para controle de tempo e janelas de análise.
*   **`logging`:** Para registro profissional de eventos e auditoria do sistema.
*   **Tratamento de Exceções:** Para robustez e resiliência do código.

## Como Rodar o Projeto

1.  **Clone o repositório:**
    ```bash
    git clone https://github.com/SEU_USUARIO/Sentinela_Digital_Ciberseguranca.git
    cd Sentinela_Digital_Ciberseguranca
    ```
    *(Substitua `SEU_USUARIO` pelo seu nome de usuário do GitHub e `Sentinela_Digital_Ciberseguranca` pelo nome exato do seu repositório )*

2.  **Execute o script Python:**
    ```bash
    python sentinela_defesa_v2.py
    ```

3.  **Verifique os logs:** As mensagens serão exibidas no console e salvas no arquivo `sentinela_defesa.log` na mesma pasta.

## Resultados Esperados

Ao executar o script, você observará:

*   Acessos legítimos sendo permitidos.
*   O início de um ataque de "enxame" com IPs rotativos.
*   Alertas de `WARNING` indicando que uma conta está sob ataque massivo.
*   Mensagens de `ERROR` e bloqueio de IPs pelo Sentinela Híbrido.
*   Um relatório final com o `Total de IPs Banidos`.
*   O registro detalhado de todos os eventos no arquivo `sentinela_defesa.log`.

## Próximos Passos e Melhorias Futuras

Este projeto é uma prova de conceito. Futuras melhorias podem incluir:

*   **Persistência de Dados:** Integração com um banco de dados (ex: SQLite, PostgreSQL) para armazenar logs de forma duradoura.
*   **Interface Gráfica:** Desenvolvimento de uma interface simples para visualização dos ataques e bloqueios.
*   **Machine Learning:** Implementação de modelos de ML (ex: Scikit-Learn) para detecção de anomalias mais complexas e preditivas, indo além de regras fixas.
*   **Integração com APIs de Threat Intelligence:** Para enriquecer os dados de análise.

## Referências

[1]: https://www.terra.com.br/noticias/ia-produzira-enxames-de-ciberataques-em-2026-aponta-lumu,9dc4c4dffac2e7cd15fd2de6f01651626s0a0kuw.html "Lumu Technologies. \"IA produzirá enxames de ciberataques em 2026, aponta Lumu\". Disponível em:"

