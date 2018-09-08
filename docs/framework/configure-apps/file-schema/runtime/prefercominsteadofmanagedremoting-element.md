---
title: '&lt;PreferComInsteadOfManagedRemoting&gt; élément'
ms.date: 03/30/2017
helpviewer_keywords:
- <PreferComInsteadOfManagedRemoting> element
- PreferComInsteadOfManagedRemoting element
ms.assetid: a279a42a-c415-4e79-88cf-64244ebda613
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c05e27226a58086c806e8977ba50a55873d1167e
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44222660"
---
# <a name="ltprefercominsteadofmanagedremotinggt-element"></a>&lt;PreferComInsteadOfManagedRemoting&gt; élément
Spécifie si le runtime utilisera COM interop au lieu de la communication à distance pour tous les appels entre les limites du domaine d’application.  
  
 \<configuration>  
\<runtime>  
\<PreferComInsteadOfManagedRemoting >  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<PreferComInsteadOfManagedRemoting enabled="true|false"/>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`enabled`|Attribut requis.<br /><br /> Indique si le runtime utilisera COM interop au lieu de la communication à distance au-delà des limites du domaine d’application.|  
  
## <a name="enabled-attribute"></a>Attribut enabled  
  
|Valeur|Description|  
|-----------|-----------------|  
|`false`|Le runtime utilisera la communication à distance entre les limites du domaine d’application. Il s'agit de la valeur par défaut.|  
|`true`|Le runtime utilisera COM interop dans les limites du domaine d’application.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|`configuration`|Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.|  
|`runtime`|Contient des informations sur les liaisons d’assembly et l’opération garbage collection.|  
  
## <a name="remarks"></a>Notes  
 Lorsque vous définissez la `enabled` attribut `true`, le runtime se comporte comme suit :  
  
-   Le runtime n’appelle pas [IUnknown::QueryInterface](https://go.microsoft.com/fwlink/?LinkID=144867) pour un [IManagedObject](../../../../../docs/framework/unmanaged-api/hosting/imanagedobject-interface.md) interface quand un [IUnknown](https://go.microsoft.com/fwlink/?LinkId=148003) accède au domaine via une interface COM. Au lieu de cela, il construit un [Runtime Callable Wrapper](../../../../../docs/framework/interop/runtime-callable-wrapper.md) (RCW) autour de l’objet.  
  
-   Le runtime retourne E_NOINTERFACE lorsqu’il reçoit un `QueryInterface` appeler pour un [IManagedObject](../../../../../docs/framework/unmanaged-api/hosting/imanagedobject-interface.md) interface pour toute [Wrapper CCW](../../../../../docs/framework/interop/com-callable-wrapper.md) (wrapper CCW) qui a été créé dans ce domaine.  
  
 Ces deux comportements garantissent que tous les appels via COM des interfaces entre les objets gérés sur l’utilisation des limites de domaine l’application COM et COM interop au lieu de la communication à distance.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment spécifier que le runtime doit utiliser COM interop au-delà des limites d’isolation :  
  
```xml  
<configuration>  
  <runtime>  
    <PreferComInsteadOfManagedRemoting enabled="true"/>  
  </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi  
 [Schéma des paramètres d’exécution](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)  
 [Schéma des fichiers de configuration](../../../../../docs/framework/configure-apps/file-schema/index.md)
