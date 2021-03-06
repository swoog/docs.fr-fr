---
title: Ajout d'états en ligne et hors connexion
ms.date: 03/30/2017
ms.assetid: 05e5f51d-81b6-4c17-b364-9dda447a5fce
ms.openlocfilehash: 15a963d4de0dcf1d7f0162b0a3266e17d4073ecd
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61857738"
---
# <a name="adding-online-and-offline-status"></a>Ajout d'états en ligne et hors connexion
Dans de nombreux cas, il est important qu'une application surveille les informations relatives à l'état d'une connexion de canal homologue. Vous pouvez obtenir ces informations en appelant la méthode `GetProperty` depuis une implémentation de l'interface <xref:System.ServiceModel.IOnlineStatus>. Un objet implémenté sur cette interface peut en effet surveiller l'état de la connexion ou s'inscrire à des gestionnaires d'événements, tels que `OnOnline` et `OnOffline`. Cet objet réagira immédiatement à toutes modifications de l'état en ligne.  
  
 Dans l'infrastructure de canal homologue, un client est considéré comme étant en ligne s'il est connecté à au moins un autre homologue et comme étant hors connexion dans le cas contraire. Ceci peut s'avérer particulièrement utile à la fois pour déboguer les applications en cours de développement ou pour communiquer des informations détaillées à l'utilisateur final.  
  
> [!NOTE]
>  Un gestionnaire d'événements en ligne doit en premier lieu garantir l'ouverture du nœud avant l'envoi de tout message.  
  
## <a name="see-also"></a>Voir aussi

- [Création d’une application de canal homologue](../../../../docs/framework/wcf/feature-details/building-a-peer-channel-application.md)
