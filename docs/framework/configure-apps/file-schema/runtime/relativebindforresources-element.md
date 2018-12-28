---
title: '&lt;relativeBindForResources&gt; élément'
ms.date: 03/30/2017
helpviewer_keywords:
- RelativeBindForResources element
- <relativeBindForResources> element
ms.assetid: 846ffa47-7257-4ce3-8cac-7ff627e0e34f
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 1933fad8ea87351a56fcc7dd4a4fd67e890b58f5
ms.sourcegitcommit: fa38fe76abdc8972e37138fcb4dfdb3502ac5394
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53613893"
---
# <a name="ltrelativebindforresourcesgt-element"></a>&lt;relativeBindForResources&gt; élément
Optimise la sonde pour les assemblys satellites.  
  
 \<configuration > élément  
\<runtime > élément  
\<relativeBindForResources > élément  
  
## <a name="syntax"></a>Syntaxe  
  
```xml
<relativeBindForResources    
   enabled="true|false" />  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`enabled`|Attribut requis.<br /><br /> Spécifie si le common language runtime optimise la sonde pour les assemblys satellites.|  
  
## <a name="enabled-attribute"></a>Attribut enabled  
  
|Valeur|Description|  
|-----------|-----------------|  
|`false`|Le runtime n’optimise pas la sonde pour les assemblys satellites. Valeur par défaut.|  
|`true`|Le runtime optimise la sonde pour les assemblys satellites.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|`configuration`|Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.|  
|`runtime`|Contient des informations sur les options d'initialisation du runtime.|  
  
## <a name="remarks"></a>Notes  
 En règle générale, Resource Manager tente de détecter des ressources, comme indiqué dans le [Packaging and Deploying Resources](../../../../../docs/framework/resources/packaging-and-deploying-resources-in-desktop-apps.md) rubrique. Cela signifie que lorsque Resource Manager tente de détecter une version localisée particulière d’une ressource, il peut rechercher dans le global assembly cache, de rechercher dans un dossier spécifique à la culture dans la requête de base, de code de l’application Windows Installer pour les assemblys satellites et déclencher le <xref:System.AppDomain.AssemblyResolve?displayProperty=nameWithType> événement. Le `<relativeBindForResources>` élément optimise celle dans laquelle Resource Manager tente de détecter les assemblys satellites. Elle peut améliorer les performances lors de la détection pour les ressources dans les conditions suivantes :  
  
-   Lorsque l’assembly satellite est déployé dans le même emplacement que l’assembly de code. En d’autres termes, si l’assembly de code est installé dans le global assembly cache, les assemblys satellites doivent également être installés il. Si l’assembly de code est installé dans la base de code de l’application, les assemblys satellites doivent également être installés dans un dossier spécifique à la culture dans la base de code.  
  
-   Lorsque le programme d’installation de Windows n’est pas utilisé ou est rarement utilisé pour l’installation à la demande des assemblys satellites.  
  
-   Lorsque le code d’application ne gère pas la <xref:System.AppDomain.AssemblyResolve?displayProperty=nameWithType> événement.  
  
 Définition de la `enabled` attribut de la `<relativeBindForResources>` élément à `true` optimise la sonde du Gestionnaire de ressources pour les assemblys satellites comme suit :  
  
-   Il utilise l’emplacement de l’assembly de code parent pour détecter l’assembly satellite.  
  
-   Il n’interroge pas le programme d’installation de Windows pour les assemblys satellites.  
  
-   Elle ne déclenche pas le <xref:System.AppDomain.AssemblyResolve?displayProperty=nameWithType> événement.  
  
## <a name="see-also"></a>Voir aussi  
- [Empaquetage et déploiement de ressources](../../../../../docs/framework/resources/packaging-and-deploying-resources-in-desktop-apps.md)  
- [Schéma des paramètres d’exécution](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)  
- [Schéma des fichiers de configuration](../../../../../docs/framework/configure-apps/file-schema/index.md)
