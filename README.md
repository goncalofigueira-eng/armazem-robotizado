# Armazém Robotizado

UC de Projeto Integrado em Automação Industrial desenvolvido no ano letivo de 2022/2023, no CTeSP de Instalações Elétrica e Automação Industrial. O repositório reúne o esquema elétrico e o programa do robot Dobot de um armazém robotizado. E foi avaliado em 17 valores.

<img width="1672" height="941" alt="image" src="https://github.com/user-attachments/assets/f7f69468-44d7-4548-9a8b-ac42ca4f1cb9" />
Imagem meramente ilustrativa

## Problema

O projeto teve como objetivo desenvolver a documentação e a arquitetura de controlo de um armazém robotizado, integrando automação, robótica e pneumática. E realizar a montagem do projeto numa platine percebemos a necessidade de partir de um esquema elétrico bem elaborado e identificado para maior facilidade na montagem.

A necessidade específica que o sistema procurou resolver foi a evolução de um sistema automático de arrumação de componentes ou de peças para o armazém da ESTGA.

## Requisitos e limites

A arquitetura documentada inclui:

- Alimentação de entrada a 230 V, 50 Hz, com cabo `3G2,5 mm²`.
- Alimentação de controlo a 24 V DC, fornecida por uma fonte Mean Well DR com saída de 24 V DC e 3,2 A.
- PLC Siemens S7-1200, CPU 1214C AC/DC/RLY.
- Painel tátil Siemens KTP600 Basic Color PN.
- Comunicação PROFINET através de um switch Ethernet industrial Turck de cinco portas.
- Robô Dobot Magician (`dt-mg-4r005-02e`) com driver Maxon (`109982-VERSTAKER`).
- Sistema pneumático regulado para 6,5 bar, com eletroválvulas e cilindros equipados com sensores de fim de curso.
- Sinalização luminosa Schneider XVBC21B, com indicadores verde, laranja e vermelho.
- Proteções elétricas e relés de interface para os circuitos de comando.

## Abordagem

A solução foi estruturada em torno de um PLC Siemens S7-1200, responsável pelo controlo do sistema e pela comunicação com a interface HMI. O operador interage com o processo através do painel tátil Siemens KTP600.

A comunicação entre os dispositivos é suportada por uma rede PROFINET. A arquitetura integra ainda o robô Dobot Magician, os atuadores pneumáticos e os sensores de fim de curso, permitindo coordenar as ações mecânicas do sistema.

A alimentação de controlo a 24 V DC é fornecida por uma fonte dedicada. Os circuitos incluem proteções elétricas, relés de interface e sinalização luminosa para indicar o estado do sistema.

## Dificuldades e decisões

Uma das principais dificuldades foi a ausência de memória interna no robô para guardar o programa de controlo. Na altura, não estavam disponíveis cartões de memória compatíveis que permitissem contornar essa limitação.

Para manter o programa em funcionamento, optámos por não desligar o robô durante a operação. Como os sinais de controlo tinham de ser de baixa tensão, integrámos no projeto um Arduino dedicado à interface com o robô. O Arduino recebia os comandos enviados pela HMI e, de acordo com esses sinais, acionava a sequência de recolha da peça e a sua colocação na gaveta correspondente.

O Arduino era alimentado por uma pilha de 9 V.

## Resultado

O repositório contém o esquema elétrico do projeto elétrico do armazém robotizado, desenvolvido em EPLAN.

## Aprendizagem

O projeto permitiu trabalhar conceitos de automação industrial, arquitetura de controlo com PLC, comunicação Máquina-PC, interface HMI, robótica e comando pneumático.

Numa próxima versão deste mesmo projeto gostaríamos de criar muito mais gavetas para permitir uma variedade superior de elementos diferentes, e suprimir o Arduino referido do projeto.

## Autoria e enquadramento

- **Instituição:** Universidade de Aveiro — Escola Superior de Tecnologia e Gestão de Águeda (ESTGA).
- **Grupo:** Grupo 2.
- **Elementos:** Gonçalo Figueira, André C., Luiz G. e Tiago N.
- **Ano letivo:** 2022/2023.

## Conteúdo do repositório

- `Esquema_Eletrico/` — projeto elétrico do armazém robotizado, elaborado em EPLAN e disponibilizado em PDF.

## Autor

Gonçalo Figueira
