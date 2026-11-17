# Armazém Robotizado 🏭[cite: 415]

Repositório dedicado à documentação técnica e projeto de automação industrial de um **Armazém Robotizado**.

---

## 👥 Autoria e Enquadramento
* **Instituição**: Universidade de Aveiro – Escola Superior de Tecnologia e Gestão de Águeda (ESTGA).
* **Grupo 2**: 
  * André XXX
  * Gonçalo Alexandre Silva Figueira (n.º mec: 109 438)
  * Luiz XXX
  * Tiago XXX
* **Ano de Fabrico / Projeto**: 2022/2023.

---

## ⚡ Especificações Elétricas
* **Alimentação de Entrada**: 230V 50 Hz ($3G2,5~mm^2$).
* **Tensão de Controlo**: 24 V DC.
* **Fonte de Alimentação**: Mean Well DR (Entrada: 230Vac / Saída: 24Vdc 3.2A).
* **Proteções e Comando**: Disjuntores/diferenciais (ex.: `-02QF20`, `-02QF90`) e relés de interface Finder (série 40.52 24VDC).

---

## 💻 Arquitetura de Controlo e Comunicação
* **PLC**: Siemens S7-1200 (CPU 1214C AC/DC/RLY).
* **HMI**: Painel tátil Siemens KTP600 Basic Color PN.
* **Rede de Comunicação**: Switch Ethernet Industrial Turck de 5 portas com suporte PROFINET.

---

## 🤖 Robótica e Sistema Pneumático
* **Robô**: Dobot Magician (`dt-mg-4r005-02e`) com driver Maxon (`109982-VERSTAKER`)[cite: 427].
* **Pneumática**: Unidade de tratamento de ar comprimido regulada a 6.5 Bar, eletroválvulas pneumáticas (`-07YV20`, `-07YV30`) e cilindros com sensores de fim de curso.
* **Sinalização**: Baliza sinalizadora Schneider XVBC21B (com luzes verde, laranja e vermelha)[cite: 423, 428].

---

## 📂 Conteúdo do Repositório
* `Esquema_Eletrico/`: Ficheiro PDF com o projeto EPLAN do armazém robotizado.
