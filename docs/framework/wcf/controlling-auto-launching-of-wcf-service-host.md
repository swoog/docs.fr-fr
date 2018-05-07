---
title: Contrôle de l'auto-lancement de l'hôte de service WCF
ms.date: 03/30/2017
f1_keywords:
- WcfOptions
ms.assetid: 6abe5d34-519b-4cef-8f02-3c0a7f125585
ms.openlocfilehash: fe936ee3ff42b586c733de597de808b86f3e2575
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="controlling-auto-launching-of-wcf-service-host"></a>Contrôle de l'auto-lancement de l'hôte de service WCF
Vous pouvez contrôler la fonction d’auto-lancement de l’hôte de Service Windows Communication Foundation (WCF) (WcfSvcHost.exe) pour un [!INCLUDE[indigo2](../../../includes/indigo2-md.md)] projet bibliothèque du Service, lorsque vous déboguez un autre projet dans la même solution Visual Studio contenant plusieurs projets .  
  
 Pour ce faire, cliquez sur le [!INCLUDE[indigo2](../../../includes/indigo2-md.md)] projet de Service dans **l’Explorateur de solutions**, choisissez **propriétés**, puis cliquez sur **Options WCF** onglet. Le **démarrer WCF Service hôte lors du débogage d’un autre projet dans la même solution** case à cocher est activée par défaut. Vous pouvez la désactiver afin que l'hôte du service [!INCLUDE[indigo2](../../../includes/indigo2-md.md)] de ce projet spécifique ne démarre pas lorsqu'un autre projet est débogué dans la même solution.  
  
 Ce comportement n'affecte pas le débogage F5 ni les fonctionnalités d'ajout d'une référence de service pour ce projet.  
  
 Cette option est disponible dans le cadre des projets suivants :  
  
-   [!INCLUDE[indigo2](../../../includes/indigo2-md.md)] Projet de la bibliothèque du service  
  
-   Projet de la bibliothèque du service du workflow séquentiel  
  
-   Projet de la bibliothèque du service de workflow d'ordinateur d'état  
  
-   Projet de la bibliothèque du service de syndication  
  
## <a name="see-also"></a>Voir aussi  
 [WCF Service Host (WcfSvcHost.exe)](../../../docs/framework/wcf/wcf-service-host-wcfsvchost-exe.md)
