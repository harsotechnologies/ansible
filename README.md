# ansible
-   for windows conectivity
    asegurarse que winrm esta activo:
        Ejecutar en powershell para activar winrm:
        
            iex(iwr https://raw.githubusercontent.com/ansible/ansible/devel/examples/scripts/ConfigureRemotingForAnsible.ps1).Content
            
        En caso de que haya error de SSL/TLS ejecutar:
        
            [Net.ServicePointManager]::SecurityProtocol = "tls12, tls11, tls"
            
        comandos para verificacion de listeners:
        
            winrm enumerate winrm/config/Listener
            winrm get winrm/config/Service

Para agregar repositorio GITHUB en AWX se usa el formato:

ssh://git@ssh.github.com:443/yourname/reponame.git

Es necesario crear una llave SSH y cargar la llave publica en la cuenta de github.
Dentro de AWX se tiene que guardar la llave privada dentro de una credencial tipo Source Control sin user ni password.
