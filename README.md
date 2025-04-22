O atual projeto é um desenvolvimento interno da equipe de apoio à Plataforma Liferay DXP na empresa MTI.
A operacionalização da atual imagem requer pre-requisitos, elencados a seguir:

1) Descer o projeto para uma pasta de trabalho.
2) Abrir o projeto dentro de um ambiente VSC. Neste ponto, tambem é possivel abrir o projeto no vsc e fazer pull do repositorio github/gitlab.
3) Criar pasta com nome 'chave', dentro da pasta liferay.
4) Criar pasta com nome 'deploy', dentro da pasta liferay.
5) Fazer download de uma chave de desenvolvimento do site help.liferay.com e copiar a mesma dentro da pasta chave e, também, na pasta deploy. Quando executa o docker-compose a da pasta deploy será consumida e apagada.
6) Abrir um terminal apontando na pasta raiz do projeto.
7) Executar no prompt 'docker-compose up --build -d'
8) Tudo indica que depois de alguns minutos pode acessar seu ambiente em localhost:8080
9) Em caso de precisar logs, pode ser realizado docker-compose up --build -d > compose_liferay.log
10) Se necessário podem ser observados os logs especificos de cada serviço por meio de:
      docker logs liferay_dxp > liferay.log
      docker logs liferay_postgres > postgres.log
11) Para parar a instância se aconselha fazer por meio de docker-compose down

Qualquer contribuição para melhora é bem-vinda.
