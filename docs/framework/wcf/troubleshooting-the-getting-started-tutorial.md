---
title: Résoudre les problèmes de la méthode Get en main des didacticiels de Windows Communication Foundation
ms.date: 01/25/2019
ms.assetid: 69a21511-0871-4c41-9a53-93110e84d7fd
ms.openlocfilehash: 8089e0fee262d07be591069982b1aacfbeae2521
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61791467"
---
# <a name="troubleshoot-the-get-started-with-windows-communication-foundation-tutorials"></a>Résoudre les problèmes de la méthode Get en main des didacticiels de Windows Communication Foundation

Cet article fournit des solutions pour les problèmes courants et les erreurs que vous pouvez rencontrer lorsque vous suivez les étapes décrites dans le [didacticiel : Prise en main les applications Windows Communication Foundation](getting-started-tutorial.md). 
  
## <a name="common-problems"></a>Problèmes courants

**Impossible de trouver les fichiers de projet sur mon disque dur.**

 Visual Studio enregistre les fichiers de projet dans *C:\Users\\&lt;nom d’utilisateur&gt;\source\repos*.  

**Impossible de trouver le *App.config* fichier généré par *Svcutil.exe*.**

 Dans Visual Studio, le **ajouter un élément existant** fenêtre affiche uniquement les fichiers portant les extensions suivantes par défaut : 
- *.cs* 
- *.resx* 
- *.settings*
- *.xsd* 
- *.wsdl*

Pour afficher tous les types de fichier, sélectionnez **tous les fichiers (\*.\*)**  dans la liste déroulante dans le coin inférieur droit de la **ajouter un élément existant** fenêtre.  
  
## <a name="common-errors"></a>Erreurs courantes

### <a name="compile-the-service-application"></a>Compilez l’application de service 

**Erreur BC30420 'Sub Main' est introuvable dans 'GettingStartedHost.Module1'.**

Le point d’entrée est incorrect pour l’application Visual Basic. Apportez la modification suivante :

   1. Dans le **l’Explorateur de solutions** fenêtre, sélectionnez le **GettingStartedHost** dossier, puis sélectionnez **propriétés** dans le menu contextuel.
    A. Dans le **GettingStartedHost** fenêtre, pour **objet de démarrage**, sélectionnez **Service.Program** (ou le point d’entrée pour votre application) dans la liste. 
    B. Dans le menu principal, sélectionnez **fichier** > **Enregistrer tout**.

### <a name="run-the-service-application"></a>Exécutez l’application de service 

**HTTP n’a pas pu inscrire URL « http :\// + : 8000/GettingStarted/CalculatorService ». Le processus n'a pas de droits d'accès à cet espace de noms.** 

 Pour permettre l’accès, démarrez le processus qui héberge le service Windows Communication Foundation (WCF) avec des privilèges d’administrateur :
- Pour Visual Studio : Sélectionnez le programme Visual Studio dans le **Démarrer** menu, puis sélectionnez **plus** > **exécuter en tant qu’administrateur** dans le menu contextuel.
- Pour une fenêtre de console : Sélectionnez **invite de commandes** dans le **Démarrer** menu, puis sélectionnez **plus** > **exécuter en tant qu’administrateur** à partir du raccourci menu.
- Pour Explorer de Windows : Sélectionnez le fichier exécutable, puis **exécuter en tant qu’administrateur** dans le menu contextuel.

### <a name="compile-the-client-application"></a>Compilez l’application cliente

**'CalculatorClient', ne contient pas de définition pour '\<nom de la méthode >' et aucune méthode d’extension '\<nom de la méthode >' acceptant un premier argument de type 'CalculatorClient' est introuvable (vous manque-t-il une à l’aide la directive ou un référence d’assembly ?)**  

Uniquement les méthodes que vous marquez avec le `ServiceOperationAttribute` attribut sont exposés publiquement. Si vous omettez le `ServiceOperationAttribute` attribut à partir d’une méthode dans le `ICalculator` interface, vous recevez ce message d’erreur pendant la compilation.  

**Le nom du type ou espace de noms 'CalculatorClient' est introuvable (vous manque-t-il une à l’aide de la directive ou une référence d’assembly ?)**

 Vous recevez cette erreur si vous n’ajoutez pas le *generatedProxy.cs* (ou *generatedProxy.vb*) le fichier à votre projet client lorsque vous avez généré avec la *Svcutil.exe* outil .  

### <a name="run-the-client-application"></a>Exécutez l’application cliente

**Exception non gérée : System.ServiceModel.EndpointNotFoundException: Ne peut pas se connecter à « http :\//localhost:8000/GettingStarted/CalculatorService ». Code d’erreur TCP 10061 : Aucune connexion a pu être établie car l’ordinateur cible l’a activement refusée.**

Cette erreur se produit si vous exécutez l’application cliente sans premier démarrage du service. Tout d’abord, exécutez l’application hôte pour démarrer le service, puis exécutez l’application cliente.

### <a name="use-the-svcutilexe-tool"></a>Utilisez l’outil Svcutil.exe
   
**'Svcutil' n’est pas reconnu comme une commande interne ou externe, un programme exécutable ou un fichier de commandes.**

 *SvcUtil.exe* doit se trouver dans le chemin d’accès système. La solution la plus simple consiste à utiliser l’invite de commandes de Visual Studio. À partir de la **Démarrer** menu, sélectionnez le **Visual Studio \<version >** répertoire, puis sélectionnez **invite de commandes développeur pour VS \<version >**. Cette invite de commande définit le chemin d’accès système pour les emplacements corrects pour tous les outils fournis dans le cadre de Visual Studio.  
  
### <a name="run-the-service-and-client-applications"></a>Exécuter les applications clientes et de service

**System.ServiceModel.Security.SecurityNegotiationException: Négociation de sécurité SOAP avec « http :\//localhost:8000/GettingStarted/CalculatorService » pour la cible ' http :\//localhost:8000/GettingStarted/CalculatorService ' a échoué**  

Cette erreur se produit sur un ordinateur joint au domaine n’ayant pas de connectivité réseau. Connecter votre ordinateur au réseau ou de désactiver la sécurité pour le service et le client. 

Pour désactiver la sécurité :

- Pour le service, remplacez le code qui crée le `WSHttpBinding` par le code suivant :  
  
    ```csharp
    // Step 3: Add a service endpoint.
    selfhost.AddServiceEndpoint(typeof(ICalculator), new WSHttpBinding(SecurityMode.None), "CalculatorService");  
    ```

- Pour le client, dans le fichier de configuration, mise à jour le  **\<sécurité >** élément sous le  **\<liaison >** élément comme suit :  
  
    ```xml
    <binding name="WSHttpBinding_ICalculator" security mode="None" />
    ```  

## <a name="see-also"></a>Voir aussi  
 [Prise en main les applications WCF](getting-started-tutorial.md)  
 [Démarrage rapide de la résolution des problèmes de WCF](wcf-troubleshooting-quickstart.md)  
 [Dépannage des problèmes d’installation](troubleshooting-setup-issues.md)
