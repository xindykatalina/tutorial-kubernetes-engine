# tutorial-kubernetes-engine
Tutorial para el despliegue en la plataforma GCP  kubernetes engine

1. Lo primero que hay que instalar en su maquina es el Google Cloud SDK

  -Se encuentra en esta url https://cloud.google.com/sdk/docs/quickstarts
	
  -Seleccionamos Quickstart for Debian and Ubuntu
  
  -En la linea de comandos ejecutamos lo siguiente
  
   //Create environment variable for correct distribution
   
      export CLOUD_SDK_REPO="cloud-sdk-$(lsb_release -c -s)"

   //Add the Cloud SDK distribution URI as a package source
   
      echo "deb http://packages.cloud.google.com/apt $CLOUD_SDK_REPO main" | sudo tee -a /etc/apt/sources.list.d/google-cloud-sdk.list

   //Import the Google Cloud Platform public key
   
      curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -

   //Update the package list and install the Cloud SDK
   
      sudo apt-get update && sudo apt-get install google-cloud-sdk

2. Inicializa el SDK
	
   - gcloud init
   - Acepte la opción para iniciar sesión con su cuenta de usuario de Google: ingresando Y
   - En su navegador, inicie sesión en su cuenta de usuario de Google cuando se le solicite y haga clic en Permitir para otorgar permiso para acceder a los recursos de Google Cloud Platform.
   - En el símbolo del sistema, seleccione un proyecto de Cloud Platform de la lista de aquellos en los que tiene permisos de Propietario , Editor o Visor
   - Si tiene la API de Google Compute Engine habilitada, le gcloud init permite elegir una zona predeterminada de Compute Engine
   - Nuevamente ejecutamos gcloud init confirma que ha completado los pasos de configuración con éxito
