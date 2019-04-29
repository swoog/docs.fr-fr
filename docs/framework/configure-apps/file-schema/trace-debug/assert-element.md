---
title: Élément <assert>
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.diagnostics/assert
- http://schemas.microsoft.com/.NetConfiguration/v2.0#assert
helpviewer_keywords:
- <assert> element
- assert element
ms.assetid: ef4c3229-b151-4d85-8091-e6456af9b935
ms.openlocfilehash: 2f3823265e358976f970cdfa36772d2251894280
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61701357"
---
# <a name="assert-element"></a>\<Assert > élément
Indique si une boîte de message doit s’afficher quand vous appelez la méthode <xref:System.Diagnostics.Debug.Assert%2A?displayProperty=nameWithType> ; spécifie également le nom du fichier dans lequel écrire les messages.  
  
 \<configuration>  
\<system.diagnostics>  
\<assert>  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<assert assertuienabled="true|false" logfilename="file name"/>  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Description|  
|---------------|-----------------|  
|`assertuienabled`|Attribut facultatif.<br /><br /> Spécifie si pour afficher un boîte de message lorsque le **Debug.Assert** méthode prend la valeur **false**.|  
|`logfilename`|Attribut facultatif.<br /><br /> Spécifie le nom de fichier dans lequel écrire le message à if **Debug.Assert** prend la valeur **false**.|  
  
## <a name="assertuienabled-attribute"></a>AssertUiEnabled attribut  
  
|Value|Description|  
|-----------|-----------------|  
|`true`|Affiche la boîte de message. Il s'agit de la valeur par défaut.|  
|`false`|Ne pas afficher la boîte de message.|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|`configuration`|Élément racine de chaque fichier de configuration utilisé par le Common Language Runtime et les applications .NET Framework.|  
|`system.diagnostics`|Spécifie les écouteurs de trace qui collectent, stockent et acheminent les messages, ainsi que le niveau auquel un commutateur de trace est défini.|  
  
## <a name="remarks"></a>Notes  
 Les deux attributs dans le  **\<assert >** élément sont facultatifs. Vous pouvez désactiver les boîtes de message sans spécifier de fichier pour écrire les messages, ou vous pouvez spécifier un fichier pour écrire des messages tout en laissant les messages activés.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre comment désactiver l’affichage des messages lorsque vous appelez **Debug.Assert** et écrire les messages à `c:\log.txt`.  
  
```xml  
<configuration>  
   <system.diagnostics>  
      <assert assertuienabled="false" logfilename="c:\log.txt"/>  
   </system.diagnostics>  
</configuration>  
```  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Diagnostics.Debug>
- [Schéma des paramètres de trace et de débogage](../../../../../docs/framework/configure-apps/file-schema/trace-debug/index.md)
