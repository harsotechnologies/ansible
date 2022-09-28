# ansible
-   for windows conectivity
    asegurarse que winrm esta activo:
        Ejecutar en powershell para activar winrm:
            iex(iwr https://raw.githubusercontent.com/ansible/ansible/devel/examples/scripts/ConfigureRemotingForAnsible.ps1).Content
        En caso de que haya error de SSL/TLS ejecutar:
            [Net.ServicePointManager]::SecurityProtocol = "tls12, tls11, tls"
        comandos para verificacion de listeners:
            winrm enumerate winrm/config/Listener
        
    