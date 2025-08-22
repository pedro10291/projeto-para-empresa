# 📦 App Corporativo de Produção

Este projeto tem como objetivo criar um aplicativo simples, intuitivo e funcional para gerenciar o fluxo de produção de "O's" dentro da empresa, com controle por setor e suporte a funcionamento offline.

---

## 📑 Sumário

- [Fluxo de Trabalho](#fluxo-de-trabalho)
- [Estrutura de Dados](#estrutura-de-dados)
- [Perfis de Usuário](#perfis-de-usuário)
- [Tecnologias Recomendadas](#tecnologias-recomendadas)
- [Tempo Estimado de Desenvolvimento](#tempo-estimado-de-desenvolvimento)
- [Vantagens para a Empresa](#vantagens-para-a-empresa)
- [Funcionalidade Offline](#funcionalidade-offline)
- [Desafios Atuais na Empresa](#desafios-atuais-na-empresa)
- [Funcionalidades Sugeridas para Resolver os Desafios](#funcionalidades-sugeridas-para-resolver-os-desafios)
- [Como Criar o App Sem Ser Programador](#como-criar-o-app-sem-ser-programador)

---

## 🔄 Fluxo de Trabalho

### 1. Planejamento
- Cadastro da "O's" pelo líder de planejamento.
- Definição de máquina, prazo, tipo de produção.

### 2. Estoque
- Verificação de papel necessário.
- Atualização de status: disponível, em falta, aguardando reposição.

### 3. Produção
- Início da produção pelo operador.
- Atualização de status: em andamento, finalizado.

### 4. Expedição
- Recebimento da "O's" finalizada.
- Atualização de status: expedido, aguardando transporte, armazenado.

---

## 🧩 Estrutura de Dados

Campos principais:
- `quantidade_papel`
- `formato_papel`
- `status_estoque`
- `responsavel_estoque_id`
- `status_producao`
- `data_inicio_producao`
- `data_fim_producao`
- `responsavel_producao_id`
- `status_expedicao`
- `responsavel_expedicao_id`

---

## 🔐 Perfis de Usuário

- **Planejador**: cadastra "O's", define requisitos.
- **Estoque**: atualiza papel e formato.
- **Produção**: inicia e finaliza "O's".
- **Expedição**: prepara envio.
- **Supervisor/Admin**: acompanha todo o fluxo.

---

## 🧪 Tecnologias Recomendadas

### Frontend
- React.js ou Vue.js
- Tailwind CSS ou Material UI

### Backend
- Node.js + Express ou Python + FastAPI
- PostgreSQL
- WebSockets ou MQTT

### Autenticação
- JWT (JSON Web Token)

### Infraestrutura
- Docker + Docker Compose
- AWS, Azure ou VPS
- GitHub Actions ou Jenkins

---

## ⏳ Tempo Estimado de Desenvolvimento

| Fase                     | Duração Estimada |
|--------------------------|------------------|
| Planejamento e protótipo | 3 a 5 dias       |
| Backend e banco de dados | 5 a 10 dias      |
| Interface e integração   | 5 a 7 dias       |
| Comunicação com máquinas | 5 a 7 dias       |
| Testes e ajustes         | 3 a 5 dias       |
| Implantação e treinamento| 2 a 3 dias       |
| **Total estimado**       | **3 a 5 semanas**|

---

## ✅ Vantagens para a Empresa

- Centralização das informações de produção
- Redução de erros e retrabalho
- Visibilidade em tempo real
- Integração entre setores
- Histórico completo
- Agilidade na tomada de decisões
- Redução do uso de papel
- Maior controle sobre insumos e prazos
- Reduz espera de tempo de máquina
- Quantidade correta de papel, assim reduzira risco de umidade.

---

## 📶 Funcionalidade Offline

### Estratégia
- Criar como Progressive Web App (PWA)
- Armazenar dados localmente com IndexedDB
- Usar Service Workers para cache
- Sincronizar com servidor quando a conexão voltar

### Benefícios
- Funcionamento garantido em áreas sem Wi-Fi
- Maior confiabilidade e produtividade
- Redução de falhas por perda de conexão

---

## 🚧 Desafios Atuais na Empresa

Apesar da estrutura existente, alguns gargalos operacionais impactam a eficiência do fluxo de produção:

### 🔻 Materiais Insuficientes
- Falta recorrente de insumos como papel e saquinhos para pastas.
- Planejador precisa buscar fisicamente os materiais, o que consome tempo.
- Erros frequentes na entrega de materiais solicitados (ex.: papel vem, mas saquinhos não).

### 🧍‍♂️ Mão de Obra 100% Manual
- Ausência de automação no processo de solicitação e entrega de insumos.
- Dependência de deslocamento físico entre setores para confirmar disponibilidade.

### 📅 Expedição Manual
- Liberação de materiais é registrada manualmente no Google Agenda.
- Falta de integração entre produção e expedição gera atrasos e retrabalho.

---

## 🛠️ Funcionalidades Sugeridas para Resolver os Desafios

### 📦 Gestão de Insumos
- Sistema de checklist por "O's" com itens obrigatórios (papel, saquinhos, etc.)
- Notificações automáticas para o setor de estoque ao cadastrar uma nova "O's"
- Alerta de pendência caso algum item não seja entregue

### 🤖 Redução da Mão de Obra Manual
- Interface para solicitação digital de materiais
- Atualização de status em tempo real entre setores
- Histórico de solicitações e entregas para rastreabilidade

### 📆 Expedição Integrada
- Painel de expedição com status de cada "O's"
- Botão de "liberar para transporte" que atualiza automaticamente o sistema
- Integração com calendário interno (Google Calendar ou similar) para agendamento automático

---
