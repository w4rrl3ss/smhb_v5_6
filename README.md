# System Monitoring Tool               

<img width="222" alt="system_monitor_hyper_logo" src="https://github.com/user-attachments/assets/3a2eb494-9951-4c0e-80f2-a34fe1d5c2ff" />


Uma ferramenta avançada de monitoramento de sistema que fornece informações detalhadas sobre o uso de recursos do computador, com interface gráfica (GUI).

![image](https://github.com/user-attachments/assets/78c507d1-a8aa-4b5e-a2bf-8803f686eb41)

![image](https://github.com/user-attachments/assets/62d82e53-52cd-428f-9627-b1333281067e)

![smhb_01](https://github.com/user-attachments/assets/904beb4c-6bdf-48d3-9dd6-e4995bc0b2da)

## 🏗️ Arquitetura do Sistema
Para entender a estrutura e componentes do sistema, consulte a documentação de [Arquitetura do Sistema](https://w4rrl3ss.github.io/smhb_v5_6/system_architecture.html).

![image](https://github.com/user-attachments/assets/9ae78071-e81b-4a9e-a641-aa7d50f729e8)

## 📌 Visão Geral

Este script monitora em tempo real:
- Uso de CPU (por núcleo e agregado)
- Memória RAM e Swap
- Utilização de disco
- Atividade de rede
- Processos em execução
- 

Gera relatórios HTML estilizados com Bootstrap e gráficos interativos.

![image](https://github.com/user-attachments/assets/da37926e-ec34-4216-a90f-2c5c52a0c163)

## 🛠️ Tecnologias Utilizadas

- Python 3.8+
- Bibliotecas principais:
  - `psutil` - Coleta de métricas do sistema
  - `tkinter` - Interface gráfica
  - `matplotlib` - Visualização de dados
  - `Bootstrap` (HTML) - Relatórios formatados

## 🏗️ Estrutura do Código

![image](https://github.com/user-attachments/assets/56d80311-36f6-4420-b5da-265efa5540f9)

### 📦 Importações Principais
```python
import psutil
import platform
import tkinter as tk
from tkinter import ttk, messagebox
import matplotlib.pyplot as plt
import argparse

⚙️ Configuração
Arquivo config.json armazena preferências do usuário

Valores padrão incluídos para primeira execução

🚨 Sistema de Alertas
Monitora condições críticas:

Vazamentos de memória

Uso excessivo de CPU

Consumo alto de memória

Swap utilization

📊 Classe Principal - SystemMonitor
python
Copy
class SystemMonitor:
    def __init__(self):
        self.config = self.load_config()
        self.alert_manager = AlertManager()
        
    def get_system_info(self):
        """Coleta informações abrangentes do sistema"""
        # Implementação...
    
    def monitor_system(self):
        """Loop principal de monitoramento"""
        # Implementação...

🖥️ Interface Gráfica - SystemMonitorGUI
python
Copy
class SystemMonitorGUI:
    def __init__(self):
        self.root = tk.Tk()
        self.setup_gui()
        
    def setup_gui(self):
        """Configura todos os elementos da interface"""
        # Implementação...

🚀 Funcionalidades
Monitoramento em Tempo Real
Gráficos dinâmicos de uso de recursos

# Ferramenta de Monitoramento de Sistema

Uma ferramenta completa de monitoramento de recursos do sistema com suporte a interface gráfica (GUI) e linha de comando (CLI), relatórios detalhados e capacidades de alerta.

## 📖 Visão Geral
Este script fornece informações detalhadas sobre o uso de recursos do computador através de uma interface gráfica (GUI) e linha de comando (CLI). Monitora:
- Uso da CPU
- Consumo de memória
- Atividade do disco
- Tráfego de rede
- Processos em execução

Gera relatórios HTML estilizados com Bootstrap e inclui alertas em tempo real para limites de recursos.

## 🧠 Estrutura do Código

### 📦 Importações
- Monitoramento: `psutil`, `platform`, `os`, `datetime`
- Componentes GUI: `tkinter`, `matplotlib`
- Processamento de dados: `collections`, `argparse`, `csv`, `json`
- Recursos avançados: `logging`, `tracemalloc`, `ctypes`

### ⚙️ Configuração
```python
CONFIG_FILE = "config.json"
DEFAULT_CONFIG = {
    "monitor_interval": 2,
    "max_duration": 600,
    # ... outros padrões
}
Criação automática do arquivo de configuração

Tratamento de erros no carregamento

🚨 Gerenciador de Alertas
Histórico com collections.deque

Disparo inteligente baseado em médias históricas

Prevenção de alertas duplicados

🔍 Classe SystemMonitor
Principais Métodos:

get_system_info(): Snapshot completo do hardware/SO

get_processes_info(): Agregação de métricas de processos

check_memory_leak(): Análise de alocação de memória

generate_report(): Geração de relatórios HTML/CSV

🖥️ Implementação GUI
Recursos:

Interface com temas (Claro/Escuro/Azul)

Dashboard de métricas em tempo real

Visualização em árvore de processos

Gráficos interativos

Gerenciamento de configurações

🛠️ Funcionalidades
🖱️ Modo GUI
bash
Copy
python monitor.py --gui
Aba de configuração para ajustes

Monitoramento em tempo real

Testes de estresse integrados

Personalização de temas

⌨️ Modo CLI
bash
Copy
python monitor.py --interval 5 --duration 300 --output relatorio.html
Monitoramento não interativo

Amostragem programada de recursos

Geração automática de relatórios

🌟 Recursos Principais
Monitoramento multi-thread

Suporte multiplataforma (Windows/macOS/Linux)

Relatórios HTML com Bootstrap

Visualização de dados com Matplotlib

Detecção de vazamento de memória

Limites de alerta configuráveis

Acompanhamento de processos específicos

Interface GUI temática

Tratamento abrangente de exceções

📈 Exemplo de Relatório
Inclui:

Tabela resumo do sistema

Linha do tempo de uso de recursos

Gráficos de principais processos

Histórico de alertas

Detalhes de hardware

## 🎯 Objetivo Principal
Monitorar em tempo real o desempenho do sistema (CPU, memória, disco, rede) e gerar **relatórios HTML detalhados** automaticamente após o término do monitoramento.

## 🌟 Recursos Principais

### 📊 Monitoramento em Tempo Real
- Coleta dados de CPU, memória, disco e rede em intervalos configuráveis
- Usa API nativa do Windows (`win32pdh`) + `psutil` como fallback
- Monitora processos específicos selecionados pelo usuário

### 🔔 Sistema de Alertas Inteligente
- Detecta uso excessivo de CPU e memória
- Identifica vazamentos de memória em processos
- Monitora uso de memória virtual (swap)
- Histórico completo de alertas

### 📑 Geração de Relatórios Profissionais
- Relatórios HTML completos com:
  - 📈 Gráficos interativos de uso de recursos
  - 📊 Tabelas detalhadas de processos
  - ⚠️ Histórico de alertas
  - ℹ️ Informações do sistema
- Exportação para CSV e imagens de gráficos

## � Arquitetura do Sistema
```mermaid
graph TD
    A[SystemMonitor] -->|Coleta dados| B[CPU/Memória/Disco/Rede]
    A --> C[AlertManager]
    D[SystemMonitorGUI] -->|Interface| A
    A -->|Gera| E[Relatórios HTML]
💡 Recursos Avançados
🕵️‍♂️ Detecção de vazamentos de memória

🎨 Suporte a temas de interface (claro/escuro/azul)

⚙️ Configuração persistente via JSON

💻 Multiplataforma (Windows com fallback cross-platform)

⚙️ Como Funciona
Coleta de Dados
Thread dedicada coleta métricas em intervalos configuráveis (padrão: 0.5s)

Processamento

Cálculo de médias/máximos/mínimos

Detecção de padrões de vazamento

Análise de variações de recursos

Geração de Relatórios

Gráficos com matplotlib

Tabelas organizadas

Salvamento automático

🖥️ Interface Gráfica
Gráficos dinâmicos em tempo real

Controle completo do monitoramento

Visualização de alertas

🔄 Fluxo de Operação
mermaid
Copy
sequenceDiagram
    Usuário->>+GUI: Configura parâmetros
    GUI->>+Monitor: Inicia thread
    Monitor->>+Sistema: Coleta dados
    Sistema-->>-Monitor: Métricas
    Monitor->>+AlertManager: Verifica alertas
    AlertManager-->>-GUI: Notifica usuário
    Monitor->>+ReportGenerator: Gera HTML
    ReportGenerator-->>-Usuário: Abre no navegador
🆕 Inovações da Versão 5.06
✅ Relatórios HTML profissionais

✅ Monitoramento detalhado de memória por processo

✅ Sistema de alertas mais inteligente

✅ Interface gráfica com temas

✅ Melhor tratamento de erros

🛠️ Exemplo de Uso
bash
Copy
# Modo GUI (padrão)
python monitor.py

# Modo CLI com opções avançadas
python monitor.py --interval 1 --duration 120 --alert-cpu 90 --alert-mem 85
👨‍💻 Público-Alvo
Este sistema é ideal para:

Administradores de sistemas

Desenvolvedores de software

Analistas de performance

Qualquer profissional que precise monitorar recursos do sistema
