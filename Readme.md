# Git Flow Commands
## Instalación
[Install Flow](https://github.com/petervanderdoes/gitflow-avh/wiki/Installation)
## Git autocomplete Mac terminal
[Install Bash git completion](https://github.com/bobthecow/git-flow-completion/wiki/Install-Bash-git-completion)
## Inicialización

`git flow init`

Escribir nombres de ramas, prefijos de tags…

Sin flow

`git init`

`git commit -allow-empty -m “start repo"`

`git checkout -b develop master`

## Conectar con un repositorio

`git remote add origin _url_`

## Comenzar una Feature

`git flow feature start _name_`

Sin flow

`git checkout -b feature/_name_ develop`

## Publicar una Feature

`git flow feature publish _name_`

Sin flow

`git checkout feature/_name_`

`git push origin feature/_name_`

## Obtener una Feauture

`git flow feature pull origin _name_`

Sin flow

`git checkout feature/_name_`

`git pull —rebase origin feature/_name_`

## Trackear cambios de una Feature

`git flow feature track _name_`

## Finalizar una Feature

`git flow feature finish _name_`

* Mergea a develop
* Borra la rama
* cambia la rama a develop

`git push origin develop`

## Crear una publicación

`git flow release start _name_`

Sin flow

`git checkout -b release/1.2.0 develop`

## Publicar una release

`git flow release publish _name_`

Sin flow

`git checkout release/_name_`

`git push origin release/_name_`

## Finalizar una publicación

`git flow release finish _name_`

Sin flow
`git checkout master`

`git merge —no-ff release/_name_`

`git tag -a _name`

`git checkout develop`

`git merge —no-ff release/_name`

`git branch -d release/_name_`

* Fusiona la rama en master
* Etiqueta con su nombre
* Fusiona con develop
* borra la publicación

## Crear un hotfix

git flow hot fix start _name_ [commit]

Sin flow

git checkout -b hotfix/_name_ [commit]

## Finalizar un hotfix

`git flow hotfix finish _name_`

Si flow

`git checkout master`

`git merge —no-ff hotfix/_name_`

`git tag -a _name`

`git checkout develop`

`git merge —no-ff hotfix/_name_`

`git branch -d hotfix/_name_`
