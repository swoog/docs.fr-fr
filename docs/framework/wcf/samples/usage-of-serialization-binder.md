---
title: Usage of Serialization Binder
ms.date: 03/30/2017
ms.assetid: ab46c087-200c-45bf-9c95-5a6cda6e8b98
ms.openlocfilehash: 677decebcf444fed95311bd02acf8a96e0a4eca9
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65591777"
---
# <a name="usage-of-serialization-binder"></a>Usage of Serialization Binder
Cet exemple montre comment utiliser le <xref:System.Runtime.Serialization.SerializationBinder> pour modifier la version d'un type générique lorsqu'il est sérialisé.  
  
## <a name="demonstrates"></a>Démonstrations  
 <xref:System.Runtime.Serialization.SerializationBinder>, <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter>  
  
## <a name="discussion"></a>Discussion  
 Cet exemple montre comment deux entités que sont cible différentes versions de peut .NET Framework communiquer à l’aide du formateur binary et le binder de sérialisation.  
  
 Le développement de cet exemple a été réalisé à l'aide de .NET Remoting. L'exemple se compose d'un serveur ciblant [!INCLUDE[netfx40_long](../../../../includes/netfx40-long-md.md)], qui implémente un contrat avec les types génériques, et deux clients différents, l'un ciblant [!INCLUDE[dnprdnlong](../../../../includes/dnprdnlong-md.md)] et l'autre ciblant [!INCLUDE[netfx40_short](../../../../includes/netfx40-short-md.md)].  
  
 Le serveur attache un <xref:System.Runtime.Serialization.SerializationBinder> au formateur binary pour être en mesure de modifier la version des types en conséquence lors de la sérialisation, si les deux clients peuvent désérialiser correctement ces types.  
  
#### <a name="to-set-up-build-and-run-the-sample"></a>Pour configurer, générer et exécuter l'exemple  
  
1. Pour exécuter le client, cliquez sur la solution, SBGenericsVTS (6 projets), puis sélectionnez **propriétés**.  
  
2. Dans **propriétés communes**, sélectionnez **projet de démarrage**, puis sélectionnez **plusieurs projets de démarrage**.  
  
3. Sélectionnez **Server** tout d’abord, puis **Client20** , puis **Client40**. Sélectionnez le **Démarrer** action à ces trois projets et laisser le reste défini sur **aucun**.  
  
4. Cliquez sur **OK** puis appuyez sur F5 pour exécuter l’exemple.
