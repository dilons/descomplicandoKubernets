# DAY-3 - Deployments e Rollouts

https://github.com/badtuxx/CertifiedContainersExpert/blob/main/DescomplicandoKubernetes/day-3/README.md

k describe deployments - descreve o deployment trazendo informaçÕes

estratégias de deploy

RollingUpdate

A estratégia RollingUpdate é a estratégia de atualização padrão do Kubernetes, ela é utilizada para atualizar os Pods de um Deployment de forma gradual, ou seja, ela atualiza um Pod por vez, ou um grupo de Pods por vez.

Nós podemos definir como será a atualização dos Pods, por exemplo, podemos definir a quantidade máxima de Pods que podem ficar indisponíveis durante a atualização, ou podemos definir a quantidade máxima de Pods que podem ser criados durante a atualização.

Vamos também aumentar a quantidade de réplicas do Deployment para 10, para que possamos ter um pouco mais de Pods para atualizar.

E para que possamos testar a estratégia RollingUpdate, vamos alterar a versão da imagem do Nginx para 1.15.0.

Recreate

A estratégia Recreate é uma estratégia de atualização que irá remover todos os Pods do Deployment e criar novos Pods com a nova versão da imagem. A parte boa é que o deploy acontecerá rapidamente, porém o ponto negativo é que o serviço ficará indisponível durante o processo de atualização.

