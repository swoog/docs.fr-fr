---
title: Guide pratique pour configurer un domaine d’application
ms.custom: ''
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: ''
ms.suite: ''
ms.technology:
- dotnet-bcl
ms.tgt_pltfrm: ''
ms.topic: article
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- application domains, configuring
- ApplicationBase property
ms.assetid: 07ea8438-7a34-49f0-a7e8-3d6ff7e4a482
caps.latest.revision: 9
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
ms.openlocfilehash: d8db75edec8e80e0e137593a424f12575cfc747b
ms.sourcegitcommit: 9a4fe1a1c37b26532654b4bbe22d702237950009
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/16/2018
---
# <a name="how-to-configure-an-application-domain"></a>Guide pratique pour configurer un domaine d’application
Vous pouvez fournir au Common Language Runtime des informations de configuration pour un nouveau domaine d’application à l’aide de la classe <xref:System.AppDomainSetup>. Quand vous créez vos propres domaines d’application, la propriété la plus importante est <xref:System.AppDomainSetup.ApplicationBase%2A>. Les autres propriétés **AppDomainSetup** sont utilisées principalement par les hôtes du runtime pour configurer un domaine d’application particulier.  
  
 La propriété **ApplicationBase** définit le répertoire racine de l’application. Quand le runtime a besoin de satisfaire une demande de type, il interroge l’assembly contenant le type dans le répertoire spécifié par la propriété **ApplicationBase**.  
  
> [!NOTE]
>  Un nouveau domaine d’application hérite uniquement de la propriété **ApplicationBase** du créateur.  
  
 L’exemple suivant crée une instance de la classe **AppDomainSetup**, utilise cette classe pour créer un domaine d’application, écrit les informations dans la console, puis décharge le domaine d’application.  
  
## <a name="example"></a>Exemple  
 [!code-cpp[ADApplicationBase#2](../../../samples/snippets/cpp/VS_Snippets_CLR/ADApplicationBase/CPP/source2.cpp#2)]
 [!code-csharp[ADApplicationBase#2](../../../samples/snippets/csharp/VS_Snippets_CLR/ADApplicationBase/CS/source2.cs#2)]
 [!code-vb[ADApplicationBase#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR/ADApplicationBase/VB/source2.vb#2)]  
  
## <a name="see-also"></a>Voir aussi  
 [Programmation avec des domaines d’application](application-domains.md#programming-with-application-domains)  
 [Utilisation des domaines d’application](../../../docs/framework/app-domains/use.md)
