---
title: 'Résolution des problèmes : Succès de l’Application de Service&#39;t installation'
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
manager: douge
ms.openlocfilehash: 1f3e5674f9a52627efdc24d6c70c0ab16dcdbbbd
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="troubleshooting-service-application-won39t-install"></a>Résolution des problèmes : Succès de l’Application de Service&#39;t installation
Si votre application de service ne s’installe pas correctement, vérifiez que le <xref:System.ServiceProcess.ServiceBase.ServiceName%2A> propriété pour la classe de service est définie sur la même valeur, comme indiqué dans le programme d’installation de ce service. La valeur doit être le même dans les deux instances dans l’ordre de votre service installer correctement.  
  
> [!NOTE]
>  Vous pouvez également consulter les journaux d’installation pour obtenir des commentaires sur le processus d’installation.  
  
 Vous devez également vérifier pour déterminer si vous avez un autre service portant le même nom que celui déjà installé. Les noms de service doivent être uniques pour l’installation réussisse.  
  
## <a name="see-also"></a>Voir aussi  
 [Introduction aux applications de service Windows](../../../docs/framework/windows-services/introduction-to-windows-service-applications.md)
