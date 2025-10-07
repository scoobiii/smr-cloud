# Nomenclatura Técnica das Configurações de Sistema

Este documento detalha as configurações de sistema mencionadas no projeto, atribuindo-lhes nomenclaturas técnicas padronizadas e descrevendo seus componentes chave, especialmente aqueles relacionados à recuperação e armazenamento de calor e frio.

## 1. Configurações de Ciclos S-CO₂

Com base nos documentos fornecidos (`sprint_1_glossario_exergia.md` e `sprint_2_python_refprop.md`), as configurações de ciclo S-CO₂ podem ser identificadas e nomeadas da seguinte forma:

| Configuração Solicitada | Nome Técnico (Baseado nos Sprints) | Descrição e Componentes Chave |
|:------------------------|:-----------------------------------|:------------------------------|
| **1a**                  | **Ciclo Brayton Simples S-CO₂**    | A configuração mais básica do ciclo Brayton com CO₂ supercrítico. Inclui turbina, compressor e um cooler principal. Não possui recuperador de calor interno, resultando em menor eficiência térmica e maior rejeição de calor no cooler. |
| **1b**                  | **Ciclo Brayton Simples S-CO₂ com Recuperador** | Uma variação do ciclo Brayton simples que incorpora um recuperador de calor (Rec.) para transferir calor do fluxo pós-turbina para o fluxo pós-compressor, aumentando a eficiência térmica. Ainda assim, a rejeição de calor no cooler principal é significativa. |
| **2**                   | **Ciclo Brayton S-CO₂ com Recompressão** | Esta configuração utiliza um recompressor para dividir o fluxo de CO₂ pós-recuperador, direcionando uma parte para um compressor adicional. Isso otimiza a recuperação de calor e reduz a carga no cooler principal, melhorando a eficiência. Inclui HTR (High Temperature Recuperator) e LTR (Low Temperature Recuperator). |
| **3**                   | **Ciclo Brayton S-CO₂ com Intercooling e Recuperação** | Considerada a configuração mais eficiente para este projeto. Apresenta um compressor de múltiplos estágios com um intercooler entre eles. O calor rejeitado no intercooler é de média temperatura, ideal para ser aproveitado por um chiller de absorção. Inclui HTR, LTR e intercooler. |
| **4**                   | **Ciclo Brayton S-CO₂ com Intercooling, Recuperação e ORC Integrado** | Esta configuração estende a Configuração 3 com a adição de um Ciclo Rankine Orgânico (ORC) para recuperar calor de baixa temperatura adicional, aumentando ainda mais a eficiência global do sistema. O ORC utiliza um fluido orgânico para converter calor residual em trabalho útil. |

## 2. Componentes de Recuperação e Armazenamento

Os documentos também detalham componentes específicos para recuperação e armazenamento de energia térmica e de refrigeração:

| Componente Específico | Nome Técnico | Descrição e Função no Sistema |
|:----------------------|:-------------|:------------------------------|
| **Recuperador de Calor** | **Recuperador (Rec.), HTR (High Temperature Recuperator), LTR (Low Temperature Recuperator)** | Trocadores de calor que transferem energia térmica do fluxo quente de saída da turbina para o fluxo frio de entrada do reator, otimizando a eficiência do ciclo S-CO₂. |
| **Storage Heat para Chiller a Absorção** | **Heat Storage (Armazenamento de Calor)** | Sistema de armazenamento de energia térmica, tipicamente tanques de água pressurizada, que armazena o calor de média temperatura recuperado do intercooler do ciclo S-CO₂. Garante um fornecimento contínuo e estável de calor para o chiller de absorção, desacoplando a geração da demanda. |
| **Trocador de Calor para Data Cloud Server Liquid Cooling** | **CDU (Coolant Distribution Unit)** | Unidade de Distribuição de Refrigerante. Este equipamento gerencia o fluxo de líquido refrigerante (água gelada ou fluido dielétrico) entre o circuito principal de refrigeração e os servidores do data center, removendo o calor diretamente dos componentes de TI. |
| **Cooling Storage para Data Cloud Server Liquid Cooling** | **Cooling Storage (Armazenamento de Frio) / Banco de Gelo (Ice Bank)** | Sistema que armazena capacidade de refrigeração, geralmente na forma de gelo, para atender a picos de demanda do data center, fornecer redundância ou operar durante períodos de manutenção do chiller. Utiliza o calor latente de fusão da água para um armazenamento compacto e eficiente. |

Esta categorização e nomenclatura serão utilizadas para estruturar o paper técnico, garantindo clareza e precisão na descrição de cada elemento do sistema integrado.
