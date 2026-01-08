---
{"dg-publish":true,"permalink":"/mapeamento-tecnologico/mapeamento-tecnologico/"}
---


# Mapeamento de Projetos Open-Source e Soluções CBDC

> Escopo: Prospecção tecnológica sobre projetos governamentais e interbancários.
> 
> Foco: Controle, Conformidade (KYC/AML) e Privacidade Programável.

---

## 1. [[Hyperledger Besu\|Hyperledger Besu]] (EVM Permissionado)

**Visão Técnica:** Cliente Ethereum Java open-source. Preferido por governos que buscam compatibilidade com ferramentas de mercado (Solidity/EVM) mas exigem consenso determinístico ([[Hyperledger-Besu/QBFT\|QBFT]]) e finalidade imediata.

#### **A. Brasil: [[DREX\|DREX]] (Piloto do Real Digital)**

- **Status:** Piloto Avançado (Fase 2 em 2024/25).
    
- **O uso do Besu:** É a infraestrutura oficial do Banco Central do Brasil. A escolha deve-se à arquitetura baseada em Java (padrão bancário nacional) e suporte a múltiplos validadores institucionais.
    
- **Destaque Técnico:** É o maior teste de **programabilidade** do mundo, integrando Títulos Públicos Federais diretamente na chain para liquidação de ativos (DvP).
    

#### **B. Noruega: [[Norges Bank CBDC Sandbox\|Norges Bank CBDC Sandbox]]**

- **Status:** Pesquisa Técnica (Sandbox Open Source).
    
- **O uso do Besu:** A Noruega é o único país que abriu o código-fonte da sua CBDC. A sandbox oficial, disponível no GitHub, é construída inteiramente sobre Hyperledger Besu.
    
- **Destaque Técnico:** Foco em demonstrar a capacidade do Besu de lidar com alta vazão (throughput) mantendo privacidade básica. É a referência de código primária para pesquisadores da área.
    

#### **C. Israel e Hong Kong: [[Project Sela\|Project Sela]]**

- **Status:** Prova de Conceito (Concluído com o BIS).
    
- **O uso do Besu:** Implementaram o "Sela Ledger" usando uma instância permissionada baseada em EVM/Besu para testar uma CBDC de Varejo focada em cibersegurança.
    
- **Destaque Técnico:** Validou um modelo de "Intermediários de Acesso", onde o Banco Central opera os nós mas não tem acesso aos dados sensíveis dos usuários finais.
    

#### **D. Tailândia: [[Project Inthanon\|Project Inthanon]] (Fase 2)**

- **Status:** Concluído.
    
- **O uso do Besu:** O Banco da Tailândia explorou o Besu para a **tokenização de títulos** e gestão do ciclo de vida de ativos ("Bond Lifecycle").
    
- **Destaque Técnico:** Crucial para provar a eficácia de Smart Contracts com lógica Ethereum complexa em ambientes regulados.
    

#### **E. Espanha: [[Smart Money\|Smart Money]] (Iberpay)**

- **Status:** Piloto Bancário.
    
- **O uso do Besu:** A câmara de compensação espanhola (Iberpay) e os 5 maiores bancos do país utilizaram uma rede Besu (Rede-i) para distribuição de dinheiro programável.
    
- **Destaque Técnico:** Teste de estresse de latência no consenso [[IBFT-2.0\|IBFT-2.0]] para pagamentos instantâneos.
    

#### **F. França: [[Banque de France\|Banque de France]] (Wholesale Experiments)**

- **Status:** Série de testes (Project Jura, etc).
    
- **O uso do Besu:** Realizaram testes seminais de liquidação de títulos listados em bolsa usando uma blockchain baseada em Ethereum Permissionado.
    
- **Destaque Técnico:** Validaram a integração técnica de uma CBDC baseada em EVM com sistemas legados de entrega de títulos.
    

#### **G. União Europeia: [[EBSI\|EBSI]] (European Blockchain Services Infrastructure)**

- **Status:** Produção/Expansão.
    
- **O uso do Besu:** Rede oficial da Comissão Europeia para identidade digital e diplomas transfronteiriços. Roda exclusivamente em nós Besu.
    
- **Destaque Técnico:** Prova a robustez do protocolo para governança distribuída entre múltiplos países (nós espalhados por toda a Europa).
    

#### **H. América Latina: [[LACChain\|LACChain]] (BID)**

- **Status:** Produção.
    
- **O uso do Besu:** Uma das maiores redes permissionadas do mundo, utilizada pelo Banco Interamericano de Desenvolvimento para projetos de identidade e rastreabilidade.
    
- **Destaque Técnico:** Demonstra a escalabilidade geográfica e estabilidade da rede Besu em produção real.
    

---

## 2. [[R3 Corda\|R3 Corda]] (DLT P2P / Notary Service)

**Visão Técnica:** DLT baseada em JVM (Kotlin) que opera P2P. Não possui blocos globais; os dados existem apenas entre os participantes da transação, garantindo **privacidade nativa** e **finalidade legal**.

#### **A. Suíça: [[Project Helvetia\|Project Helvetia]] (Fase 1 e 2)**

- **Status:** Prova de Conceito Concluída (Referência Mundial).
    
- **O uso do Corda:** O Banco Nacional Suíço integrou a CBDC de Atacado diretamente com a [[SDX\|SDX]] (SIX Digital Exchange), bolsa digital construída nativamente em Corda.
    
- **Destaque Técnico:** Validou a **Liquidação Atômica** real, onde a entrega do token do ativo e o pagamento da CBDC ocorrem simultaneamente na mesma camada lógica.
    

#### **B. França e Suíça: [[Project Jura\|Project Jura]]**

- **Status:** Experimento Cross-Border Concluído.
    
- **O uso do Corda:** Utilizaram uma rede Corda com arquitetura de **Sub-redes** para conectar o Banque de France e o Banco Nacional Suíço.
    
- **Destaque Técnico:** Inovação em **Geo-localização de Dados**, garantindo que dados franceses ficassem em servidores na França e suíços na Suíça, mesmo na mesma rede lógica.
    

#### **C. Multi-Países: [[Project Dunbar\|Project Dunbar]] (BIS)**

- **Status:** Protótipo Internacional.
    
- **O uso do Corda:** Conectou Bancos Centrais da Austrália, Malásia, Singapura e África do Sul. Escolhido pelo modelo de privacidade P2P ("o que acontece entre dois bancos, fica entre dois bancos").
    
- **Destaque Técnico:** Uso de _CorDapps_ para automatizar conversão cambial e liquidação direta, reduzindo a necessidade de bancos correspondentes.
    

#### **D. Reino Unido: [[Bank of England Proofs\|Bank of England Proofs]]**

- **Status:** Provas de Conceito Diversas.
    
- **O uso do Corda:** O Banco da Inglaterra conduziu diversos testes focados em modelos de privacidade para uma potencial "Britcoin".
    
- **Destaque Técnico:** Validação de modelos de dados onde o Banco Central pode verificar a validade da oferta monetária sem ver os detalhes individuais das transações.
    

#### **E. Singapura: [[Project Ubin\|Project Ubin]] (Fase 2)**

- **Status:** Concluído (Seminal).
    
- **O uso do Corda:** Um dos primeiros estudos globais a validar o uso de DLT descentralizada para sistemas de Liquidação Bruta em Tempo Real (LBTR).
    
- **Destaque Técnico:** Comparativo de performance e privacidade de DLTs frente a sistemas centralizados.
    

---

## 3. [[Hyperledger Fabric\|Hyperledger Fabric]] (Modular / Chaincode)

**Visão Técnica:** Arquitetura modular altamente configurável. Não usa modelo de contas (UTXO/Account) nativo, mas sim _World State_ e _Chaincode_ (Go/Node). Foca em alta performance e canais privados.

#### **A. Arábia Saudita e Emirados Árabes: [[Project Aber\|Project Aber]]**

- **Status:** Piloto de Alta Disponibilidade Concluído.
    
- **O uso do Fabric:** Criação de uma moeda comum de liquidação entre os dois países. Escolhido pela arquitetura modular sem taxas de gás nativas.
    
- **Destaque Técnico:** **Resiliência Descentralizada**. Provou que o sistema continua operando mesmo se a infraestrutura de um dos Bancos Centrais falhar totalmente (Disaster Recovery).
    

#### **B. Caribe Oriental: [[DXCD\|DXCD]] (DCash)**

- **Status:** Produção (com interrupções passadas).
    
- **O uso do Fabric:** O Banco Central do Caribe Oriental (ECCB) utiliza uma versão privada baseada em Fabric para conectar 8 países insulares.
    
- **Destaque Técnico:** Foco em identidade e varejo via mobile. A rede expôs desafios de gestão de certificados em redes permissionadas (causando uma interrupção em 2022).
    

#### **C. China: [[e-CNY\|e-CNY]] (Yuan Digital)**

- **Status:** Implementação Massiva.
    
- **O uso do Fabric:** A arquitetura é descrita como híbrida, mas análises técnicas apontam o uso de conceitos do Fabric na camada de reconciliação entre bancos e o Banco Central.
    
- **Destaque Técnico:** **Concorrência Massiva**. Removeu o consenso pesado para focar em TPS (Transações Por Segundo), centralizando a validação final no Banco Popular da China (PBoC).
    

---

## 4. Redes Públicas e Híbridas (Stellar & Ripple)

**Visão Técnica:** Uso de tecnologias originalmente públicas, mas implementadas em versões privadas (Sidechains) ou com camadas de controle de ativos (Clawback/Auth) para atender regulação.

#### **A. Palau: [[Palau Stablecoin\|Palau Stablecoin]] (PSC)**

- **Status:** Piloto Fase 2.
    
- **O uso da Ripple:** Utilizam a **Ripple CBDC Platform**, uma sidechain privada do XRPL, dando ao governo controle total sobre emissão e congelamento.
    
- **Destaque Técnico:** Foco em custo energético irrisório e transações finais em 3-5 segundos, ideal para ambientes com infraestrutura limitada.
    

#### **B. Butão: [[Ngodrup Project\|Ngodrup Project]]**

- **Status:** Piloto em andamento.
    
- **O uso da Ripple:** O Banco Central do Butão utiliza a infraestrutura Ripple para testes de pagamentos transfronteiriços.
    
- **Destaque Técnico:** Exploração de **Tokenização de Ativos Reais** (commodities/energia) usando a CBDC como meio de liquidação.
    

#### **C. Ucrânia: [[e-Hryvnia\|e-Hryvnia]]**

- **Status:** P&D de Infraestrutura.
    
- **O uso da Stellar:** Parceria com a Stellar Development Foundation para criar infraestrutura de ativos virtuais.
    
- **Destaque Técnico:** Uso de recursos nativos do protocolo SCP (Stellar Consensus Protocol) como "Authorization Required" e "Clawback" para garantir conformidade regulatória em Camada 1.
    

#### **D. Brasil: [[Mercado Bitcoin\|Mercado Bitcoin]] (Interoperabilidade no DREX)**

- **Status:** Testes de Ponte (Bridge).
    
- **O uso da Stellar:** Participantes do piloto DREX (como MB) testaram a tokenização de ativos na rede pública Stellar conectada à rede permissionada Besu do Banco Central.
    
- **Destaque Técnico:** Validação de cenários de **Public-Private Bridge**, movendo valor entre ambientes regulados fechados e redes auditáveis públicas.

![Plataformas.png](/img/user/Plataformas.png)
