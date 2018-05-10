---
title: Utilisation des outils de développement WCF
ms.date: 03/30/2017
ms.assetid: 054adb87-c244-4d5a-83d1-0b2b44bd454b
ms.openlocfilehash: 41d2ee2881b79ffb086a931ec6d271d409ac66db
ms.sourcegitcommit: 15109844229ade1c6449f48f3834db1b26907824
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2018
---
# <a name="using-the-wcf-development-tools"></a>Utilisation des outils de développement WCF
Cette section décrit les outils de développement Visual Studio qui peuvent vous aider à développer votre WCFservice.  
  
 Vous pouvez utiliser les modèles Visual Studio comme base pour générer rapidement votre propre service, puis utiliser l’hôte de Service WCF et le Client Test WCF pour déboguer et tester votre service. Ces outils offrent un cycle de débogage et de test rapide et transparent tout en supprimant l’obligation de se limiter à un modèle d’hébergement à un stade précoce.  
  
## <a name="the-wcf-developer-tools"></a>Outils WCF Developer  
 [Modèles Visual Studio WCF](../../../docs/framework/wcf/wcf-vs-templates.md)  
  
 Vous pouvez utiliser les modèles de projet et d’élément prédéfinis de Visual Studio dans Visual Studio pour générer rapidement des services WCF et les applications s’y rapportant.  
  
 [WCF Service Host (WcfSvcHost.exe)](../../../docs/framework/wcf/wcf-service-host-wcfsvchost-exe.md)  
  
 L’hôte de Service WCF (WcfSvcHost.exe) vous permet de lancer le débogueur Visual Studio (F5) pour héberger et tester un service que vous avez implémenté automatiquement. Vous pouvez ensuite tester le service à l’aide du Client de Test WCF (wcfTestClient.exe) ou votre propre client pour rechercher et corriger les erreurs potentielles.  
  
 [Client test WCF (WcfTestClient.exe)](../../../docs/framework/wcf/wcf-test-client-wcftestclient-exe.md)  
  
 Client Test WCF (WcfTestClient.exe) est un outil GUI qui permet d’entrer des paramètres de types arbitraires, d’envoyer ces entrées au service et afficher que la réponse que le service renvoie. Il offre de service transparentes lorsqu’il est associé avec l’hôte de Service WCF de test.  
  
 [Génération de classes de type de données à partir de XML](../../../docs/framework/wcf/generating-data-type-classes-from-xml.md)  
  
 Les données XML stockées dans le presse-papiers peuvent être collées dans une page de codes. Les classes définies dans les données sont converties en types de codes.  
  
## <a name="using-the-tools-without-administrator-privilege"></a>Utilisation des outils sans privilège d'administrateur  
 Pour permettre aux utilisateurs sans privilège d’administrateur développer des services WCF, une liste ACL (Access Control List) est créée pour l’espace de noms «http://+:8731/Design_Time_Addresses» lors de l’installation de Visual Studio. La liste ACL a la valeur (UI), qui inclut tous les utilisateurs interactifs ayant ouvert une session sur l'ordinateur. Les administrateurs peuvent ajouter ou supprimer des utilisateurs de cette liste ACL ou ouvrir des ports supplémentaires. Cette liste ACL permet aux modèles WCF ou WF d'envoyer et de recevoir des données dans leur configuration par défaut. Il permet également aux utilisateurs d’utiliser l’hôte de Service WCF (wcfSvcHost.exe) sans leur accorder des privilèges d’administrateur.  
  
 Vous pouvez modifier l'accès à l'aide de l'outil Netsh.exe dans [!INCLUDE[wv](../../../includes/wv-md.md)] par le biais du compte d'administrateur supérieur. L'utilisation de Netsh.exe est illustrée dans l'exemple suivant.  
  
```  
netsh http add urlacl url=http://+:8001/MyService user=<domain>\<user>  
```  
  
 Pour plus d’informations sur Netsh.exe, consultez [comment utiliser l’outil Netsh.exe et les commutateurs de ligne de commande](http://go.microsoft.com/fwlink/?LinkId=97877).  
  
## <a name="see-also"></a>Voir aussi  
 [Modèles Visual Studio WCF](../../../docs/framework/wcf/wcf-vs-templates.md)  
 [WCF Service Host (WcfSvcHost.exe)](../../../docs/framework/wcf/wcf-service-host-wcfsvchost-exe.md)  
 [Client test WCF (WcfTestClient.exe)](../../../docs/framework/wcf/wcf-test-client-wcftestclient-exe.md)
