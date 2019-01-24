---
title: 'Procédure : Utiliser Svcutil.exe pour valider le Code de Service compilé'
ms.date: 03/30/2017
ms.assetid: d0d820fb-41c2-45b8-8f22-0fa5aeebbbaa
ms.openlocfilehash: a06cf57fce883753af4686b294396d6d6da73a13
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54531926"
---
# <a name="how-to-use-svcutilexe-to-validate-compiled-service-code"></a>Procédure : Utiliser Svcutil.exe pour valider le Code de Service compilé
Vous pouvez utiliser la [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) pour détecter les erreurs dans les configurations et les implémentations de service sans héberger le service.  
  
### <a name="to-validate-a-service"></a>Pour valider un service  
  
1.  Compilez votre service dans un fichier exécutable et un ou plusieurs assemblys dépendants.  
  
2.  Ouvrez une invite de commandes du Kit de développement SDK.  
  
3.  À l'invite de commandes, lancez l'outil Svcutil.exe à l'aide du format suivant. Pour plus d’informations sur les différents paramètres, consultez la section de validation de Service de la [ServiceModel Metadata Utility Tool (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md) rubrique.  
  
    ```  
    svcutil.exe /validate /serviceName:<serviceConfigName>  <assemblyPath>*  
    ```  
  
     Vous devez utiliser l'option `/serviceName` pour indiquer le nom de configuration du service que vous souhaitez valider.  
  
     L'argument `assemblyPath` spécifie le chemin d'accès au fichier exécutable du service et un ou plusieurs assemblys qui contiennent les types de services à valider. L'assembly exécutable doit avoir un fichier de configuration associé pour fournir la configuration du service. Vous pouvez utiliser des caractères génériques de ligne de commande standard pour fournir plusieurs assemblys.  
  
## <a name="example"></a>Exemple  
 La commande suivante illustre le service myServiceName implémenté dans le fichier exécutable myServiceHost.exe.  Le fichier de configuration pour le service (myServiceHost.exe.config) est chargé automatiquement.  
  
```  
svcutil /validate /serviceName:myServiceName myServiceHost.exe  
```  
  
## <a name="see-also"></a>Voir aussi
- [Outil ServiceModel Metadata Utility (Svcutil.exe)](../../../../docs/framework/wcf/servicemodel-metadata-utility-tool-svcutil-exe.md)
