---
title: Dépannage du didacticiel de mise en route
ms.date: 03/30/2017
ms.assetid: 69a21511-0871-4c41-9a53-93110e84d7fd
ms.openlocfilehash: 5b8cd04ef4d98e522e255e1b7529e848351b2e0c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54695658"
---
# <a name="troubleshooting-the-getting-started-tutorial"></a>Dépannage du didacticiel de mise en route
Cette rubrique décrit les problèmes les plus courants rencontrés pendant l'exécution du didacticiel de prise en main et comment les résoudre.  
  
**Je n’arrive pas à trouver les fichiers de projet sur mon disque dur.**

 Visual Studio enregistre les fichiers projet dans c:\users\\<user name>\Documents\\< version de Visual Studio\>\Projects.  
  
**Tente d’exécuter l’application de service : HTTP n’a pas pu inscrire URL `http://+:8000/ServiceModelSamples/Service/`.** 
 **Votre processus ne dispose pas de droits d’accès à cet espace de noms.** 

 Le processus qui héberge un service WCF doit être exécuté avec des privilèges d’administrateur. Si vous exécutez le service à partir de Visual Studio, vous devez exécuter Visual Studio en tant qu’administrateur. Pour cela, cliquez sur **Démarrer**, avec le bouton droit **Visual Studio \< *version* >**  et sélectionnez **Run As Administrator**. Si vous exécutez le service à partir d’une invite de ligne de commande dans une fenêtre de console, vous devez démarrer la fenêtre de console en tant qu’administrateur de la même façon. Cliquez sur **Démarrer**, avec le bouton droit **invite de commandes** et sélectionnez **exécuter en tant qu’administrateur**.  
  
**Essayez d’utiliser l’outil Svcutil.exe : 'svcutil' n’est pas reconnu comme une commande interne ou externe, un programme exécutable ou un fichier de commandes.**

 Svcutil.exe doit figurer dans le chemin d’accès système. La solution la plus simple consiste à utiliser l'invite de commandes. Cliquez sur **Démarrer**, sélectionnez **tous les programmes**, **Visual Studio \< *version*>**,  **Visual Studio Tools**, et **invite de commandes développeur pour Visual Studio**. Cette invite de commande définit le chemin d’accès système pour les emplacements corrects pour tous les outils fournis dans le cadre de Visual Studio.  

**Impossible de trouver le fichier App.config généré par Svcutil.exe.**

 Le **ajouter un élément existant** boîte de dialogue affiche uniquement les fichiers portant les extensions suivantes par défaut : .cs, .resx, .settings, .xsd, .wsdl. Vous pouvez spécifier que vous souhaitez voir tous les types de fichiers en sélectionnant **tous les fichiers (\*.\*)**  dans la zone de liste déroulante dans le coin inférieur droit de la **ajouter un élément existant** boîte de dialogue.  


**Compilation de l’application cliente : 'CalculatorClient' ne contient-elle pas de définition pour '\<nom de la méthode >' et aucune méthode d’extension '\<nom de la méthode >' acceptant un premier argument de type 'CalculatorClient' est introuvable (vous manque-t-il une à l’aide la directive ou un référence d’assembly ?)**  

Seules les méthodes marquées avec `ServiceOperationAttribute` sont exposées au monde extérieur. Si vous avez omis le `ServiceOperationAttribute` attribut à partir d’une des méthodes dans le `ICalculator` interface, vous obtenez ce message d’erreur lors de la compilation d’une application cliente qui effectue un appel à l’opération de l’attribut manquant.  

**Compilation de l’application cliente : Le nom du type ou espace de noms 'CalculatorClient' est introuvable (vous manque-t-il une à l’aide de la directive ou une référence d’assembly ?)**

 Vous obtenez cette erreur si vous n'ajoutez pas le fichier Proxy.cs ou Proxy.vb à votre projet client.  

**Le client en cours d’exécution : Exception non prise en charge : System.ServiceModel.EndpointNotFoundException: Ne peut pas se connecter à `http://localhost:8000/ServiceModelSamples/Service/CalculatorService`. Code d’erreur TCP 10061 : Aucune connexion a pu être établie car l’ordinateur cible l’a activement refusée.**

Cette erreur se produit si vous exécutez l'application cliente sans exécuter le service.  
  
**Exception non gérée : System.ServiceModel.Security.SecurityNegotiationException: Négociation de sécurité SOAP avec `http://localhost:8000/ServiceModelSamples/Service/CalculatorService` pour cible `http://localhost:8000/ServiceModelSamples/Service/CalculatorService` a échoué**  

Cette erreur se produit sur un ordinateur appartenant à un domaine qui ne bénéficie d'aucune connectivité réseau. Soit vous connectez votre ordinateur au réseau, soit vous désactivez la sécurité à la fois pour le client et le service. Pour le service, modifiez le code qui crée WSHttpBinding par ce qui suit.  
  
```csharp
// Step 3 of the hosting procedure: Add a service endpoint  
selfhost.AddServiceEndpoint(typeof(ICalculator), new WSHttpBinding(SecurityMode.None), "CalculatorService");  
```

Pour le client, modifiez le  **\<sécurité >** élément sous le  **\<liaison >** élément à ce qui suit :  
  
```xml
<security mode="Node" />  
```  

## <a name="see-also"></a>Voir aussi
- [Didacticiel Bien démarrer](../../../docs/framework/wcf/getting-started-tutorial.md)
- [Démarrage rapide de la résolution des problèmes WCF](../../../docs/framework/wcf/wcf-troubleshooting-quickstart.md)
- [Résolution des problèmes d’installation](../../../docs/framework/wcf/troubleshooting-setup-issues.md)
