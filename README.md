# LAB - Entendendo sobre Segurança e Identidade na Azure (AZ900 | DIO)

Este guia foi elaborado como parte do laboratório "Entendendo sobre Segurança e Identidade na Azure" da trilha de formação AZ-900. Aqui, um estudante de DevOps iniciante documenta, de forma simples e objetiva, os principais recursos de identidade e segurança do Microsoft Azure, explorando o Microsoft Entra ID (antigo Azure Active Directory) e o Microsoft Defender for Cloud.

---

## 🔐 Microsoft Entra ID (Azure Active Directory)

### 👍 O que é?
O Microsoft Entra ID é o serviço de identidade da Microsoft baseado na nuvem. Ele permite que você gerencie identidades e acessos a aplicativos e recursos da Azure e outros serviços Microsoft (como Microsoft 365).

### ✨ Funcionalidades Principais:
- **Autenticação de usuários e dispositivos**
- **Controle de acesso com base em funções (RBAC)**
- **Single Sign-On (SSO)**
- **Integração com identidades locais (Active Directory)**
- **Multi-Factor Authentication (MFA)**

### ⚖️ Diferença entre planos Gratuito e Pago:
| Funcionalidade                       | Gratuito | P1 | P2 |
|--------------------------------------|----------|----|----|
| Autenticação SSO básica              | ✅       |✅ | ✅|
| MFA (básico)                         | ✅       |✅ | ✅|
| Conditional Access                   | ❌       |✅ | ✅|
| Identity Protection                  | ❌       |❌ | ✅|
| Governance de Identidade             | ❌       |✅ | ✅|

### 💸 Exemplos Reais de Uso:
- Criação de um grupo "Desenvolvedores" com acesso apenas às VMs de dev
- Usuários de RH com acesso exclusivo às planilhas do SharePoint
- MFA obrigatório para acesso de administradores

### 👥 Permissões, Logins e Grupos
- **Usuários**: podem ser criados manualmente ou sincronizados com AD local.
- **Grupos**: podem ser usados para aplicar permissões em massa.
- **Funções (Roles)**: definem o que cada usuário pode ou não fazer na Azure.

### 🌐 Sincronização com AD Local
Com o Azure AD Connect é possível integrar sua estrutura local com o Entra ID, mantendo logins unificados e seguros.

---

## ⚠️ Microsoft Defender for Cloud

### 📃 O que é?
É uma plataforma de gerenciamento de postura de segurança (CSPM) e proteção contra ameaças para workloads na nuvem e ambientes híbridos.

### ⚖️ Planos:
| Recurso                              | Gratuito | Plano Padrão |
|--------------------------------------|----------|--------------|
| Avaliação de segurança de recursos   | ✅       | ✅          |
| Recomendações de melhorias           | ✅       | ✅          |
| Proteção contra ameaças em tempo real| ❌       | ✅          |
| Proteção para SQL, VMs, Storage etc. | ❌       | ✅          |

### 🌐 Recursos e Utilidades:
- **Secure Score**: Métrica que mostra o quão protegidos estão seus recursos
- **Alertas de ameaça**: Notificações em tempo real
- **Políticas de segurança**: Definem padrões obrigatórios para seus recursos

### 💡 Exemplos de Uso:
- Alertar quando um Storage Blob for acessado anonimamente
- Detectar uma VM com portas RDP abertas para internet
- Aplicar criptografia obrigatória a todos os discos gerenciados

---

## 📄 Conclusão
O Microsoft Entra ID e o Defender for Cloud são fundamentais para garantir segurança, controle de acesso e conformidade na nuvem. Mesmo com os planos gratuitos, já é possível implementar uma postura de segurança eficaz para pequenos projetos ou estudos.

---

## 📅 Referências:
- [Documentação Microsoft Entra ID](https://learn.microsoft.com/pt-br/entra/)
- [Microsoft Defender for Cloud](https://learn.microsoft.com/pt-br/azure/defender-for-cloud/)
- [DIO - Curso AZ-900](https://www.dio.me/)

---

Desenvolvido por [**Pedro Henrique Gomes dos Santos**](https://www.linkedin.com/in/pedro-henrique-gomes-dos-santos/)
