---
title: 'Procédure : Tester le Proxy de découverte'
ms.date: 03/30/2017
ms.assetid: d96e3fa2-3c42-4e5d-8244-2694081bdc32
ms.openlocfilehash: 3c159481813266386706b34d172bbf9614a8253d
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54590511"
---
# <a name="how-to-test-the-discovery-proxy"></a>Procédure : Tester le Proxy de découverte
Cette rubrique est la quatrième d'une série quatre qui expliquent comment implémenter un proxy de découverte. Dans la rubrique précédente, [Comment : Implémenter une Application cliente qui utilise le Proxy de découverte pour rechercher un Service](../../../../docs/framework/wcf/feature-details/client-app-discovery-proxy-to-find-a-service.md), vous avez implémenté une application de client WCF qui utilise le proxy de découverte pour rechercher un service, puis appelle le service. Cette rubrique explique comment vérifier si le proxy de découverte, le service et l'application cliente fonctionnent comme prévu.  
  
### <a name="run-the-discovery-proxy"></a>Exécuter le proxy de découverte  
  
1.  Ouvrez une invite de commandes en tant qu'administrateur.  
  
2.  Vous pouvez voir une boîte de dialogue indiquant que : Pare-feu de Windows a bloqué certaines fonctionnalités de ce programme. Si vous voyez ce message, cliquez sur le **Unblock** bouton.  
  
3.  Dans l'invite de commandes, exécutez le proxy de découverte, DiscoveryProxy.exe.  
  
4.  L'application doit afficher le texte suivant : `Proxy started. Hit Enter to exit`.  
  
### <a name="run-the-discoverable-service"></a>Exécuter le service détectable  
  
1.  Ouvrez une invite de commandes en tant qu'administrateur.  
  
2.  Dans l'invite de commandes, exécutez le service détectable service.exe.  
  
3.  Le DiscoveryProxy.exe doit afficher le texte suivant : `******* Adding the following service: ** [Service Contract Name] ** [Service Endpoint Addr] 3.******* Done *******` .  
  
### <a name="run-the-client-application"></a>Exécuter l'application cliente  
  
1.  Ouvrez une invite de commandes.  
  
2.  Dans l'invite de commandes, exécutez l'application client.exe.  
  
3.  Après quelques secondes, l’application cliente affiche le texte suivant : Connexion à [-point de terminaison Service].  
  
4.  Le service.exe doit ensuite afficher le texte suivant : Salutation reçu, je vais répondre.  
  
5.  Le client.exe doit ensuite afficher le texte suivant : Bonjour Client !  
  
### <a name="shut-down-the-applications"></a>Arrêter les applications  
  
1.  Arrêtez l'application cliente.  
  
2.  Arrêtez le service. Le proxy de découverte affiche le texte suivant : `******* Removing the following service: ** [Service Contract Name] ** [Service Endpoint Addr] 2.3.******* Done *******`.  
  
3.  Arrêtez le proxy de découverte.  
  
## <a name="see-also"></a>Voir aussi
- [Vue d’ensemble de la découverte WCF](../../../../docs/framework/wcf/feature-details/wcf-discovery-overview.md)
- [Guide pratique pour Implémenter un Proxy de découverte](../../../../docs/framework/wcf/feature-details/how-to-implement-a-discovery-proxy.md)
- [Guide pratique pour Implémenter un Service détectable qui s’enregistre avec le Proxy de découverte](../../../../docs/framework/wcf/feature-details/discoverable-service-that-registers-with-the-discovery-proxy.md)
- [Guide pratique pour Implémenter une Application cliente qui utilise le Proxy de découverte pour rechercher un Service](../../../../docs/framework/wcf/feature-details/client-app-discovery-proxy-to-find-a-service.md)
