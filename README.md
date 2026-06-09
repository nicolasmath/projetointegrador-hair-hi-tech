![GitHub License](https://img.shields.io/github/license/nicolasmath/lab-redes-01)

# Projeto Integrador - Implantação de Infraestrutura de TI
**Empresa:** Hair Hi-Tech  
**Slogan:** Soluções tecnológicas e suporte em TI.

![Logo Hair Hi-Tech](Logotipo.png)

Alunos: Nicolas, Anna, Rafael, Sara, Gabriel M., Levy.

---

## 📝 Sobre a Empresa

### Missão
Nossa missão é alinhar processos, blindar servidores e garantir o fluxo contínuo de dados, entregando um suporte em TI tão fluido, inteligente e sob medida que se torna invisível no dia a dia dos nossos parceiros.

### Visão
Ser a principal referência em terceirização e infraestrutura de TI para empresas prestadoras de serviços até 2030, alcançando a marca de 100% de disponibilidade dos ambientes gerenciados e expandindo nossa operação com soluções automatizadas e alta retenção de clientes.

### Organograma Simplificado
* **Diretoria:** CEO e CTO
* **Administrativo / Financeiro:** RH e Faturamento
* **Recepção:** Atendimento Inicial
* **Suporte Técnico / Operações:** Analistas de Infraestrutura e Helpdesk

**Quantidade de Funcionários:** 15 colaboradores.

### Planta Baixa do Escritório
![Planta Baixa Hair Hi-Tech](PlantaescritórioTI.png)

---

## 👥 Integrantes do Grupo e Funções (Kanban)

* **[Nicolas e Anna]** - Scrum Master & Sysadmin Windows (Active Directory, DNS, DHCP e GPOs).
* **[Gabriel Monteiro e Sara]** - Sysadmin Linux & DevOps (Servidor Web Apache/Nginx, Banco de Dados e GLPI).
* **[Rafael e Levy]** - Engenheiro de Redes (Topologias e Configurações no Cisco Packet Tracer).

---

## 🛠️ Projeto de Rede (Cisco Packet Tracer)

A rede está estruturada na subrede **192.168.20.0/24** para organizar os ativos de forma estática e as estações de trabalho via DHCP.

### Plano de Endereçamento IP

| Equipamento / Serviço | Endereço IP | Interface | Função no Projeto |
| :--- | :--- | :--- | :--- |
| **Gateway / Firewall** | `192.168.20.1` | Gig0/0/1 | Roteamento de borda e segurança |
| **Windows Server (AD/DNS)** | `192.168.20.10` | FE0 | Controlador de Domínio e escopo DHCP |
| **Linux Server (GLPI)** | `192.168.20.20` | FE0 | Sistema de chamados técnicos |
| **Linux Server (Web/Wiki)** | `192.168.20.30` | FE0 | Aplicação Web Corporativa |
| **Impressora de Rede** | `192.168.20.50` | FE0 | Impressora compartilhada do escritório |
| **Access Point (Wi-Fi)** | `192.168.20.60` | Port 0 | Distribuição de sinal sem fio (SSID: HairHiTech_Corp) |
| **Estações de Trabalho** | DHCP | FE0 / Dynamic | IPs distribuídos do `.100` ao `.200` |

---

### Topologia Lógica do Cenário
![Topologia da Rede](cenário.png)

---

## 📂 Estrutura de Pastas do Repositório

* `/packet-tracer`: Arquivos `.pkt` das topologias física e lógica.
* `/documentacao`: Planta baixa do escritório, relatórios e atas de reuniões.
* `/scripts`: Scripts de automação ou arquivos de configuração dos servidores (Windows/Linux).

---

## 🚀 Como Executar o Laboratório

1. Baixe o arquivo da topologia na pasta `/packet-tracer`.
2. Abra no **Cisco Packet Tracer** (versão 8.X recomendada).
3. Para testar os servidores web, abra o navegador de qualquer PC cliente e acesse o IP `192.168.20.30`.
