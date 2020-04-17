# Trilha DevOps da 4Linux

[![Build Status](https://travis-ci.org/kvnfreire/DevOpsLab-HelloWorld.svg?branch=master)](https://travis-ci.org/kvnfreire/DevOpsLab-HelloWorld)

## Aplicação criada para exemplificar o Ciclo de uma PipeLine DevOps


Para maiores informações acesse o [Site da 4Linux](https://www.4linux.com.br/cursos/devops)

## TROUBLESHOOT

For some reason heroku auth:token was returning a wrong token for me, even after making sure that I was logged in to heroku on the command line.

After trying all the solutions posted, what worked for me was:

Go to Heroku Account
Manually copy the API Key and then paste it into command line:

For the ones hosted at travis-ci.org:
travis encrypt pasteAPIKeyHere --add deploy.api_key --org
travis encrypt $(heroku auth:token) --add deploy.api_key --org
