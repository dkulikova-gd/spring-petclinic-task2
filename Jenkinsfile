properties([
  parameters([
    string(name: 'dockerTagName', defaultValue: 'latest', description: 'Docker Tag', )
   ])
])
sh "docker push dkulikova/spring-petclinic:${dockerTagName}"
