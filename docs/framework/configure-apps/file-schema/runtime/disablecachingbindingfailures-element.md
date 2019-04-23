---
title: Élément <disableCachingBindingFailures>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#disableCachingBindingFailures
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/runtime/disableCachingBindingFailures
helpviewer_keywords:
- assemblies [.NET Framework],caching binding failures
- caching assembly binding failures
- <disableCachingBindingFailures> element
- disableCachingBindingFailures element
ms.assetid: bf598873-83b7-48de-8955-00b0504fbad0
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 4893adaf528f1a9ef8fc8eab8027406fd8520cc2
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59159274"
---
# <a name="disablecachingbindingfailures-element"></a>\<disableCachingBindingFailures > élément
Spécifie s’il faut désactiver la mise en cache des échecs se produisent, car l’assembly est introuvable par la détection de liaison.  
  
 \<configuration > élément  
\<runtime > élément  
\<disableCachingBindingFailures>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<disableCachingBindingFailures enabled="0|1"/>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|enabled|Attribut requis.<br /><br /> Spécifie s’il faut désactiver la mise en cache des échecs se produisent, car l’assembly est introuvable par la détection de liaison.|  
  
## <a name="enabled-attribute"></a>Attribut enabled  
  
|Value|Description|  
|-----------|-----------------|  
|0|Ne désactivez pas la mise en cache des échecs se produisent, car l’assembly est introuvable par la détection de liaison. Il s’agit du comportement de liaison par défaut en commençant par le .NET Framework version 2.0.|  
|1|Désactiver la mise en cache des échecs se produisent, car l’assembly est introuvable par la détection de liaison. Ce paramètre rétablit le comportement de liaison du .NET Framework version 1.1.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|`configuration`|Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.|  
|`runtime`|Contient des informations sur les liaisons d’assembly et l’opération garbage collection.|  
  
## <a name="remarks"></a>Notes  
 À compter de .NET Framework version 2.0, le comportement par défaut pour le chargement des assemblys est mettre en cache tous les liaison et les échecs de chargement. Autrement dit, si une tentative de chargement d’un assembly échoue, les demandes suivantes pour charger le même assembly échouent immédiatement, sans faire de tentative pour localiser l’assembly. Cet élément désactive ce comportement par défaut pour les échecs de liaison qui se produisent, car l’assembly est introuvable dans le chemin de recherche. Ces défaillances lèvent <xref:System.IO.FileNotFoundException>.  
  
 Une liaison et les échecs de chargement ne sont pas affectées par cet élément et sont toujours mis en cache. Ces échecs se produisent, car l’assembly a été trouvé, mais ne peut pas être chargé. Elles lèvent <xref:System.BadImageFormatException> ou <xref:System.IO.FileLoadException>. La liste suivante comprend quelques exemples de ces défaillances.  
  
-   Si vous tentez de charger un fichier n’est pas un assembly valide, les tentatives suivantes pour charger l’assembly échoue même si le fichier incorrect est remplacé par l’assembly approprié.  
  
-   Si vous essayez de charger un assembly qui est verrouillé par le système de fichiers, les tentatives suivantes pour charger l’assembly échoue même après que l’assembly est libéré par le système de fichiers.  
  
-   Si une ou plusieurs versions de l’assembly que vous tentez de charger est dans le chemin de recherche, mais la version spécifique que vous demandez n’est pas entre eux, les tentatives suivantes pour charger cette version échoue même si la version correcte est déplacée dans le chemin de recherche.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment désactiver la mise en cache des échecs de liaison d’assembly qui se produisent, car l’assembly est introuvable par la détection.  
  
```xml  
<configuration>  
   <runtime>  
      <disableCachingBindingFailures enabled="1" />  
   </runtime>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi

- [Schéma des paramètres d’exécution](../../../../../docs/framework/configure-apps/file-schema/runtime/index.md)
- [Schéma des fichiers de configuration](../../../../../docs/framework/configure-apps/file-schema/index.md)
- [Méthode de localisation des assemblys par le runtime](../../../../../docs/framework/deployment/how-the-runtime-locates-assemblies.md)
