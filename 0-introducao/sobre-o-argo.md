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

## Componentes do Argo
- **Projects**: Permitem agrupar aplicativos relacionados e definir políticas de acesso e sincronização para esses grupos.

- **Applications**: Representam os aplicativos individuais que são gerenciados pelo ArgoCD. Cada aplicação está associada a um repositório Git e a um cluster Kubernetes.

- **Repositories**: São os repositórios Git que contêm as definições de configuração dos aplicativos.

- **Sync Windows**: Permitem definir janelas de tempo específicas durante as quais as sincronizações automáticas podem ocorrer.

## Exemplo de Aplicação com ArgoCD
- Um exemplo de aplicação gerenciada pelo argo pode ser vista no arquivo `guestbook-sample-app.yaml`, que define uma aplicação chamada "guestbook" que utiliza Helm para gerenciar seus manifests. 
  - A aplicação está configurada para sincronizar automaticamente com o repositório Git especificado, garantindo que o estado do aplicativo no cluster Kubernetes esteja sempre alinhado com o estado desejado definido no Git.