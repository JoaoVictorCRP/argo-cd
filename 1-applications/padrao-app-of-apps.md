# Padrão App of Apps

- O padrão App of Apps é uma abordagem arquitetural utilizada no ArgoCD para gerenciar múltiplas aplicações Kubernetes de forma organizada e escalável. 
  - Nesse padrão, uma aplicação "pai" (App of Apps) é criada para gerenciar várias aplicações "filhas", permitindo que você agrupe e controle o ciclo de vida de várias aplicações relacionadas a partir de um único ponto.

- A aplicação "pai" sobe as definições das aplicações "filhas" a partir de um repositório Git, onde cada aplicação filha é definida como um recurso separado. 
  - Isso facilita a gestão de ambientes complexos, onde múltiplas aplicações precisam ser implantadas e mantidas em sincronia.