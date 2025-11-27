# Sobre o ArgoCD

- O ArgoCD é uma ferramenta de entrega contínua (CD) declarativa para Kubernetes. Ele permite que você implemente e gerencie aplicativos Kubernetes usando o **Git como fonte única de verdade**. Com o ArgoCD, você pode sincronizar automaticamente o estado desejado dos aplicativos definidos em repositórios Git com o estado real no cluster Kubernetes, facilitando a automação e a gestão de configurações em ambientes de produção.

- Principais características do ArgoCD:
  - **GitOps**: Utiliza o Git como fonte de verdade para a configuração e o estado dos aplicativos.
  - **Sincronização automática**: Monitora os repositórios Git e sincroniza automaticamente as alterações com o cluster Kubernetes.
  - **Interface de usuário intuitiva**: Fornece uma interface web para visualizar e gerenciar aplicativos, bem como para monitorar o estado de sincronização.
  - **Suporte a múltiplos formatos de configuração**: Compatível com YAML, Helm, Kustomize, Jsonnet, entre outros.
  - **Controle de acesso baseado em funções (RBAC)**: Permite definir permissões granulares para usuários e equipes.

- **O Argo usa o próprio etcd como base de dados para armazenar o estado dos aplicativos e suas configurações**. 
  - Isso permite que o ArgoCD mantenha um registro consistente do estado desejado dos aplicativos e facilite a sincronização com o cluster Kubernetes.