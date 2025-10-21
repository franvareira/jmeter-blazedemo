# 🧪 Projeto de Testes de Performance – JMeter

Este repositório contém um conjunto de **testes de performance** desenvolvidos com o **Apache JMeter**, voltado à análise de carga e pico de requisições em uma aplicação de compra de passagens (BlazeDemo).  

O projeto foi estruturado para facilitar a **execução, análise e documentação** dos resultados obtidos.

---

## 🗂️ Estrutura do Projeto

```
📦 Raiz do Projeto
├── 📁 docs/               → Documentações e análises detalhadas
│   └── Analise_Resultados.md
│
├── 📁 imgs/               → Imagens e gráficos para relatórios e README
│   ├── percentil.PNG
│   └── carga.PNG
│
├── 📁 projeto/            → Arquivos principais do JMeter
│   ├── BlazeDemo - Compra de Passagem.jmx  # Script de testes
│   ├── data.csv                              # Massa de dados utilizada
│   └── jmeter.log                            # Log de execução
│
├── 📁 relatorios/         → Resultados e relatórios de execução
│   ├── carga/             # Evidências de testes de carga realizados localmente
│   ├── pico/              # Evidências de testes de pico realizados localmente
│   ├── html/              # Relatório HTML completo (JMeter Dashboard)
│   └── results.jtl        # Log principal dos resultados (JTL)
│
└── README.md
```

---

## 🚀 Como Executar os Testes

1. **Pré-requisitos**
   - Java 8+ instalado e configurado  
   - Apache JMeter (versão compatível com Java 8)  

2. **Executar o script**
   ```bash
   jmeter -n -t "projeto/BlazeDemo - Compra de Passagem.jmx" -l "relatorios/results.jtl" -e -o "relatorios/html"
   ```

3. **⚠️ Importante antes de gerar o relatório HTML**
   - O JMeter **não gera o relatório** se a pasta de destino **não estiver vazia**.  
   - Antes de executar o comando acima, **esvazie a pasta `relatorios/html/`**:
     ```bash
     rm -rf relatorios/html/*
     ```
   - O relatório gerado estará disponível em:
     ```
     relatorios/html/index.html
     ```

---

## 📊 Resultados e Análises

Os diretórios `relatorios/carga/` e `relatorios/pico/` contêm **evidências de execuções realizadas localmente**.  
Essas execuções serviram como **base para a análise de resultados** documentada em [`Analise_Resultados`](/docs/Analise_Reseultados.md).

A pasta `relatorios/html/` contém o **relatório HTML gerado localmente**, utilizado como referência visual para análise de desempenho.

### Exemplos de Gráficos

| Gráfico | Descrição |
|----------|------------|
| ![Percentil](/imgs/percentil.png) | Distribuição dos tempos de resposta |
| ![Throughput](/imgs/carga.png) | Taxa de requisições por segundo |

---

## 🧰 Tecnologias Utilizadas

- [Apache JMeter](https://jmeter.apache.org/)
- Java 8  
- Relatórios HTML (JMeter Dashboard)
- CSV Data Config para parametrização de massa

---

## 🧾 Autor

👤 **Francielle Vareira**   
📧 [LinkedIn](https://www.linkedin.com/in/franciellevareira/)

---
