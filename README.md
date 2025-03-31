# System Monitoring Tool

<img width="222" alt="system_monitor_hyper_logo" src="https://github.com/user-attachments/assets/3a2eb494-9951-4c0e-80f2-a34fe1d5c2ff" />


Uma ferramenta avançada de monitoramento de sistema que fornece informações detalhadas sobre o uso de recursos do computador, com interface gráfica (GUI) e linha de comando (CLI).

## 📌 Visão Geral

Este script monitora em tempo real:
- Uso de CPU (por núcleo e agregado)
- Memória RAM e Swap
- Utilização de disco
- Atividade de rede
- Processos em execução

Gera relatórios HTML estilizados com Bootstrap e gráficos interativos.

## 🛠️ Tecnologias Utilizadas

- Python 3.8+
- Bibliotecas principais:
  - `psutil` - Coleta de métricas do sistema
  - `tkinter` - Interface gráfica
  - `matplotlib` - Visualização de dados
  - `Bootstrap` (HTML) - Relatórios formatados

## 🏗️ Estrutura do Código

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
