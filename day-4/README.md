# ReplicaSets, Daemonsets e Probes

https://github.com/badtuxx/CertifiedContainersExpert/tree/main/DescomplicandoKubernetes/day-4#apagando-o-replicaset

kubectl get replicaset \ k get rs
kubectl scale deployment nginx-deployment --replicas 5 \ k scale deployment nginx-deployment --replicas 5

quando é criado o replica set, não é feito o rollout dos pods quando é mudado o manifesto, por exemplo, ao trocar a versão do nginx, e der o apply no manifesto, o pod só será atualizado, quando o pod for deletado.

------ 

O DaemonSet é um objeto que garante que todos os nós do cluster executem uma réplica de um Pod, ou seja, ele garante que todos os nós do cluster executem uma cópia de um Pod.

daemonsets e replicasets não são criados via CLI, apenas por manifestos

------

resumo probes

dependendo da configuração, servem para garantir que caso ocorro problema com o POD, o k8s, toma uma ação, seja reiniciar o pod ou remover o pod do cluster

liveness -> saber se o pod está vivo 
startup -> executar um teste pra saber se ele foi startadado
readness -> valida se o pod está OK para receber requisições externas
