---
title: WS Transport Security
ms.date: 03/30/2017
ms.assetid: 33a20358-5e1b-458a-a6a9-15753bc7b99b
ms.openlocfilehash: 3bc9cf3700e79b62c54c335f838c7fa660d9e780
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/27/2018
ms.locfileid: "50180911"
---
# <a name="ws-transport-security"></a><span data-ttu-id="ef26d-102">WS Transport Security</span><span class="sxs-lookup"><span data-stu-id="ef26d-102">WS Transport Security</span></span>
<span data-ttu-id="ef26d-103">Cet exemple illustre l’utilisation de la sécurité de transport SSL avec la liaison <xref:System.ServiceModel.WSHttpBinding>.</span><span class="sxs-lookup"><span data-stu-id="ef26d-103">This sample demonstrates the use of SSL transport security with the <xref:System.ServiceModel.WSHttpBinding> binding.</span></span> <span data-ttu-id="ef26d-104">Par défaut, la liaison `wsHttpBinding` assure la communication HTTP.</span><span class="sxs-lookup"><span data-stu-id="ef26d-104">By default, the `wsHttpBinding` binding provides HTTP communication.</span></span> <span data-ttu-id="ef26d-105">En cas de configuration pour la sécurité du transport, la liaison prend en charge la communication HTTPS.</span><span class="sxs-lookup"><span data-stu-id="ef26d-105">When configured for transport security, the binding supports HTTPS communication.</span></span> <span data-ttu-id="ef26d-106">Cet exemple est basé sur le [mise en route](../../../../docs/framework/wcf/samples/getting-started-sample.md) qui implémente un service de calculatrice.</span><span class="sxs-lookup"><span data-stu-id="ef26d-106">This sample is based on the [Getting Started](../../../../docs/framework/wcf/samples/getting-started-sample.md) that implements a calculator service.</span></span> <span data-ttu-id="ef26d-107">La liaison `wsHttpBinding` est spécifiée et configurée dans les fichiers de configuration de l'application pour le client et le service.</span><span class="sxs-lookup"><span data-stu-id="ef26d-107">The `wsHttpBinding` is specified and configured in the application configuration files for the client and service.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="ef26d-108">La procédure d'installation ainsi que les instructions de génération correspondant à cet exemple figurent en fin de rubrique.</span><span class="sxs-lookup"><span data-stu-id="ef26d-108">The set-up procedure and build instructions for this sample are located at the end of this topic.</span></span>  
  
> [!IMPORTANT]
>  <span data-ttu-id="ef26d-109">Les exemples peuvent déjà être installés sur votre ordinateur.</span><span class="sxs-lookup"><span data-stu-id="ef26d-109">The samples may already be installed on your machine.</span></span> <span data-ttu-id="ef26d-110">Recherchez le répertoire (par défaut) suivant avant de continuer.</span><span class="sxs-lookup"><span data-stu-id="ef26d-110">Check for the following (default) directory before continuing.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  <span data-ttu-id="ef26d-111">Si ce répertoire n’existe pas, accédez à [Windows Communication Foundation (WCF) et des exemples de Windows Workflow Foundation (WF) pour .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) pour télécharger tous les Windows Communication Foundation (WCF) et [!INCLUDE[wf1](../../../../includes/wf1-md.md)] exemples.</span><span class="sxs-lookup"><span data-stu-id="ef26d-111">If this directory does not exist, go to [Windows Communication Foundation (WCF) and Windows Workflow Foundation (WF) Samples for .NET Framework 4](https://go.microsoft.com/fwlink/?LinkId=150780) to download all Windows Communication Foundation (WCF) and [!INCLUDE[wf1](../../../../includes/wf1-md.md)] samples.</span></span> <span data-ttu-id="ef26d-112">Cet exemple se trouve dans le répertoire suivant.</span><span class="sxs-lookup"><span data-stu-id="ef26d-112">This sample is located in the following directory.</span></span>  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Binding\WS\wsTransportSecurity`  
  
 <span data-ttu-id="ef26d-113">Le code de programme dans l’exemple est identique à celle de la [mise en route](../../../../docs/framework/wcf/samples/getting-started-sample.md) service.</span><span class="sxs-lookup"><span data-stu-id="ef26d-113">The program code in the sample is identical to that of the [Getting Started](../../../../docs/framework/wcf/samples/getting-started-sample.md) service.</span></span> <span data-ttu-id="ef26d-114">Vous devez créer un certificat et l’assigner en utilisant l’Assistant Certificat de serveur web avant de générer et exécuter l’exemple.</span><span class="sxs-lookup"><span data-stu-id="ef26d-114">You must create a certificate and assign it by using the Web Server Certificate Wizard before building and running the sample.</span></span> <span data-ttu-id="ef26d-115">La définition du point de terminaison et la définition de la liaison dans les paramètres du fichier de configuration activent le mode de sécurité `Transport`, comme le montre l'exemple de configuration suivant pour le client.</span><span class="sxs-lookup"><span data-stu-id="ef26d-115">The endpoint definition and binding definition in the configuration file settings enable `Transport` security mode, as shown in the following sample configuration for the client.</span></span>  
  
```xml  
<system.serviceModel>  
  
    <client>  
      <!-- this endpoint has an https: address -->  
      <endpoint address="https://localhost/servicemodelsamples/service.svc" binding="wsHttpBinding" bindingConfiguration="Binding1" contract="Microsoft.Samples.TransportSecurity.ICalculator"/>  
    </client>  
  
    <bindings>  
      <wsHttpBinding>  
        <!-- configure wsHttpbinding with Transport security mode  
                   and clientCredentialType as None -->  
        <binding name="Binding1">  
          <security mode="Transport">  
            <transport clientCredentialType="None"/>  
          </security>  
        </binding>  
      </wsHttpBinding>  
    </bindings>  
  
  </system.serviceModel>  
```  
  
 <span data-ttu-id="ef26d-116">L'adresse spécifiée utilise le modèle https://.</span><span class="sxs-lookup"><span data-stu-id="ef26d-116">The address specified uses the https:// scheme.</span></span> <span data-ttu-id="ef26d-117">La configuration de la liaison définit le mode de sécurité au mode `Transport`.</span><span class="sxs-lookup"><span data-stu-id="ef26d-117">The binding configuration sets the security mode to `Transport`.</span></span> <span data-ttu-id="ef26d-118">Le même mode de sécurité doit être spécifié dans le fichier Web.config du service.</span><span class="sxs-lookup"><span data-stu-id="ef26d-118">The same security mode must be specified in the service's Web.config file.</span></span>  
  
 <span data-ttu-id="ef26d-119">Étant donné que le certificat utilisé dans cet exemple est un certificat de test créé avec Makecert.exe, une alerte de sécurité apparaît lorsque vous essayez d’accéder à une adresse https : adresse, par exemple https://localhost/servicemodelsamples/service.svc, à partir de votre navigateur.</span><span class="sxs-lookup"><span data-stu-id="ef26d-119">Because the certificate used in this sample is a test certificate created with Makecert.exe, a security alert appears when you try to access an https: address, such as https://localhost/servicemodelsamples/service.svc, from your browser.</span></span> <span data-ttu-id="ef26d-120">Pour autoriser le client Windows Communication Foundation (WCF) travailler avec un certificat de test en place, du code supplémentaire a été ajouté au client pour supprimer l’alerte de sécurité.</span><span class="sxs-lookup"><span data-stu-id="ef26d-120">To allow the Windows Communication Foundation (WCF) client to work with a test certificate in place, some additional code has been added to the client to suppress the security alert.</span></span> <span data-ttu-id="ef26d-121">Ce code, et la classe qui l'accompagne, n'est pas requis lors de l'utilisation de certificats de production.</span><span class="sxs-lookup"><span data-stu-id="ef26d-121">This code, and the accompanying class, is not required when using production certificates.</span></span>  

```csharp
// This code is required only for test certificates like those created by Makecert.exe.  
PermissiveCertificatePolicy.Enact("CN=ServiceModelSamples-HTTPS-Server");  
```

 <span data-ttu-id="ef26d-122">Lorsque vous exécutez l'exemple, les demandes et réponses d'opération s'affichent dans la fenêtre de console du client.</span><span class="sxs-lookup"><span data-stu-id="ef26d-122">When you run the sample, the operation requests and responses are displayed in the client console window.</span></span> <span data-ttu-id="ef26d-123">Appuyez sur Entrée dans la fenêtre du client pour l'arrêter.</span><span class="sxs-lookup"><span data-stu-id="ef26d-123">Press ENTER in the client window to shut down the client.</span></span>  
  
```  
Add(100,15.99) = 115.99  
Subtract(145,76.54) = 68.46  
Multiply(9,81.25) = 731.25  
Divide(22,7) = 3.14285714285714  
  
Press <ENTER> to terminate client.  
```  
  
### <a name="to-set-up-build-and-run-the-sample"></a><span data-ttu-id="ef26d-124">Pour configurer, générer et exécuter l'exemple</span><span class="sxs-lookup"><span data-stu-id="ef26d-124">To set up, build, and run the sample</span></span>  
  
1.  <span data-ttu-id="ef26d-125">Installez [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] 4.0 à l'aide de la commande suivante.</span><span class="sxs-lookup"><span data-stu-id="ef26d-125">Install [!INCLUDE[vstecasp](../../../../includes/vstecasp-md.md)] 4.0 using the following command.</span></span>  
  
    ```  
    %windir%\Microsoft.NET\Framework\v4.0.XXXXX\aspnet_regiis.exe /i /enable  
    ```  
  
2.  <span data-ttu-id="ef26d-126">Vérifiez que vous avez effectué la [procédure d’installation unique pour les exemples Windows Communication Foundation](../../../../docs/framework/wcf/samples/one-time-setup-procedure-for-the-wcf-samples.md).</span><span class="sxs-lookup"><span data-stu-id="ef26d-126">Ensure that you have performed the [One-Time Setup Procedure for the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/one-time-setup-procedure-for-the-wcf-samples.md).</span></span>  
  
3.  <span data-ttu-id="ef26d-127">Vérifiez que vous avez effectué la [Instructions d’Installation du certificat serveur Internet Information Services (IIS)](../../../../docs/framework/wcf/samples/iis-server-certificate-installation-instructions.md).</span><span class="sxs-lookup"><span data-stu-id="ef26d-127">Ensure that you have performed the [Internet Information Services (IIS) Server Certificate Installation Instructions](../../../../docs/framework/wcf/samples/iis-server-certificate-installation-instructions.md).</span></span>  
  
4.  <span data-ttu-id="ef26d-128">Pour générer l’édition C# ou Visual Basic .NET de la solution, conformez-vous aux instructions figurant dans [Building the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/building-the-samples.md).</span><span class="sxs-lookup"><span data-stu-id="ef26d-128">To build the C# or Visual Basic .NET edition of the solution, follow the instructions in [Building the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/building-the-samples.md).</span></span>  
  
5.  <span data-ttu-id="ef26d-129">Pour exécuter l’exemple dans une configuration unique ou plusieurs ordinateurs, suivez les instructions de [en cours d’exécution les exemples Windows Communication Foundation](../../../../docs/framework/wcf/samples/running-the-samples.md).</span><span class="sxs-lookup"><span data-stu-id="ef26d-129">To run the sample in a single- or cross-machine configuration, follow the instructions in [Running the Windows Communication Foundation Samples](../../../../docs/framework/wcf/samples/running-the-samples.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ef26d-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ef26d-130">See Also</span></span>
