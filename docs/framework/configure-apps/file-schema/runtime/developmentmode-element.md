---
title: Élément <developmentMode>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/runtime/developmentMode
- http://schemas.microsoft.com/.NetConfiguration/v2.0#developmentMode
helpviewer_keywords:
- developmentMode element
- container tags, <developmentMode> element
- <developmentMode> element
ms.assetid: 60e79a8c-415a-497d-be29-b9d0fd9bdee3
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 323bc5d18860c00609a92e33f4a2bd2c832b05a9
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55290067"
---
# <a name="developmentmode-element"></a>\<developmentMode > élément
Indique si le runtime recherche des assemblys dans les répertoires spécifiés par la variable d’environnement DEVPATH.  
  
 \<configuration>  
\<runtime>  
\<developmentMode>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<developmentMode developerInstallation="true | false"/>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|**developerInstallation**|Indique si le runtime recherche des assemblys dans les répertoires spécifiés par la variable d’environnement DEVPATH.|  
  
## <a name="developerinstallation-attribute"></a>developerInstallation attribut  
  
|Value|Description|  
|-----------|-----------------|  
|**true**|Recherche les assemblys dans les répertoires spécifiés par la variable d’environnement DEVPATH.|  
|**false**|Ne recherche pas les assemblys dans les répertoires spécifiés par la variable d’environnement DEVPATH. Ceci est la valeur par défaut|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|`configuration`|Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.|  
|`runtime`|Contient des informations sur les liaisons d’assembly et l’opération garbage collection.|  
  
## <a name="remarks"></a>Notes  
 Utilisez ce paramètre uniquement au moment du développement. Le runtime ne vérifie pas les versions sur les assemblys avec nom fort trouvés dans DEVPATH. Elle utilise simplement le premier assembly qu’il trouve.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment entraîner le runtime recherche des assemblys dans les répertoires spécifiés par la variable d’environnement DEVPATH.  
  
```xml  
<configuration>  
   <runtime>  
      <developmentMode developerInstallation="true"/>  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi
- [Schéma des paramètres d’exécution](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [Schéma des fichiers de configuration](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [Guide pratique pour Localiser des assemblys à l’aide de DEVPATH](../../../../../docs/framework/configure-apps/how-to-locate-assemblies-by-using-devpath.md)
