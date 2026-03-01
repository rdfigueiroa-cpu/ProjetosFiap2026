# Entrega 2 - Estimativa de Custos AWS (FarmTech)

Este diretório contém a análise comparativa de custos para a infraestrutura de nuvem da solução FarmTech, utilizando a Calculadora de Preços da AWS.

## 1. Configuração de Hardware Selecionada
Para atender aos requisitos técnicos solicitados, a configuração abaixo foi aplicada em ambas as regiões:

- **Instância:** t3a.micro (Família t3a - Processadores AMD)
- **Especificações:** 2 vCPUs e 1 GiB de Memória RAM
- **Armazenamento:** 50 GB de EBS (General Purpose SSD - gp3)
- **Modelo de Pagamento:** On-Demand (Utilização de 100% no mês)
- **Sistema Operacional:** Linux

> **Nota Técnica:** Embora a calculadora sugira a instância `t4g.nano` como a de menor custo absoluto, ela foi descartada por possuir apenas 0.5 GiB de RAM, o que não atenderia ao requisito mínimo de 1 GiB do projeto.

## 2. Comparativo de Custos Mensais
- **Região US East (N. Virginia):** $10,86 USD
- **Região South America (São Paulo):** $18,62 USD

## 3. Decisão Final e Justificativa
A região selecionada para a implementação da solução FarmTech é **South America (São Paulo)**.

**Justificativa:**
A escolha baseia-se no equilíbrio entre conformidade e performance:
1. **Latência:** A proximidade geográfica com os sensores de campo no Brasil reduz o tempo de resposta na coleta e processamento de dados.
2. **Conformidade Legal (LGPD):** Garante a soberania dos dados ao manter as informações sensíveis da operação agrícola em território nacional, atendendo a possíveis restrições regulatórias.
3. **Desempenho:** A configuração `t3a.micro` oferece o balanço ideal de custo-benefício para rodar os scripts de análise (conforme detalhado na Entrega 1) com a memória RAM exigida.
