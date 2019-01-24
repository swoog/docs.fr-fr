---
title: Contrôle de l'auto-lancement de l'hôte de service WCF
ms.date: 03/30/2017
f1_keywords:
- WcfOptions
ms.assetid: 6abe5d34-519b-4cef-8f02-3c0a7f125585
ms.openlocfilehash: f7f58a684449819fe945ad1ba5bff12f425c8294
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54712390"
---
# <a name="controlling-auto-launching-of-wcf-service-host"></a>Contrôle de l'auto-lancement de l'hôte de service WCF
Lorsque vous déboguez un autre projet dans la même solution Visual Studio contenant plusieurs projets, vous pouvez contrôler la fonction d’auto-lancement de l’hôte de Service Windows Communication Foundation (WCF) (WcfSvcHost.exe) pour un projet de bibliothèque de Service WCF.  
  
 Pour ce faire, cliquez sur le projet de Service WCF dans **l’Explorateur de solutions**, choisissez **propriétés**, puis cliquez sur **Options WCF** onglet. Le **démarrer WCF Service hôte lors du débogage d’un autre projet dans la même solution** case à cocher est activée par défaut. Vous pouvez désactiver la case pour que l’hôte de Service WCF pour ce projet spécifique n’est pas lancée lorsqu’un autre projet est débogué dans la même solution.  
  
 Ce comportement n'affecte pas le débogage F5 ni les fonctionnalités d'ajout d'une référence de service pour ce projet.  
  
 Cette option est disponible dans le cadre des projets suivants :  
  
-   Projet de bibliothèque de Service WCF.  
  
-   Projet de la bibliothèque du service du workflow séquentiel  
  
-   Projet de la bibliothèque du service de workflow d'ordinateur d'état  
  
-   Projet de la bibliothèque du service de syndication  
  
## <a name="see-also"></a>Voir aussi
- [WCF Service Host (WcfSvcHost.exe)](../../../docs/framework/wcf/wcf-service-host-wcfsvchost-exe.md)
