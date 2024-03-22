Crie 3 deploymentes diferentes utilizando, limites de recurso, estratégias de deploy e probes.

trafeik.yaml -> utiliza a estratégia de recreate, recriando todos os pods quando necessário;
radarr.yaml -> utilza a estratégia de rollingUpdate, atualizando 1 pod por vez, sendo que pode ter no máximo 2 pods indisponíveis;
httpd.yaml ->  utilza a estratégia de rollingUpdate, atualizando 1 pod por vez, sendo que pode ter no máximo 2 pods indisponíveis;