---
title: 'Résolution des problèmes : impossibilité d’installer une application de service'
ms.date: 03/30/2017
helpviewer_keywords:
- troubleshooting service applications
- services, troubleshooting
- services, debugging
- Windows NT services, troubleshooting
- troubleshooting NT services
- Windows Service applications, troubleshooting
ms.assetid: 45c48e2e-b97d-44bc-8896-14f328e0ce33
author: ghogen
ms.openlocfilehash: 998c7a3f5ca405b3bd66b877d027126f6c76cc15
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54494416"
---
# <a name="troubleshooting-service-application-won39t-install"></a>Résolution des problèmes : impossibilité d’installer une application de service
Si votre application de service ne s’installe pas correctement, vérifiez que la propriété <xref:System.ServiceProcess.ServiceBase.ServiceName%2A> de la classe de service est définie avec la même valeur que celle indiquée dans le programme d’installation de ce service. Pour que votre service s’installe correctement, la valeur doit être la même dans les deux instances.  
  
> [!NOTE]
>  Vous pouvez également passer en revue les journaux d’installation pour récupérer des commentaires sur le processus d’installation.  
  
 Déterminez également si un autre service portant le même nom est déjà installé. Pour que l’installation réussisse, les noms de service doivent être uniques.  
  
## <a name="see-also"></a>Voir aussi
- [Introduction aux applications de service Windows](../../../docs/framework/windows-services/introduction-to-windows-service-applications.md)
