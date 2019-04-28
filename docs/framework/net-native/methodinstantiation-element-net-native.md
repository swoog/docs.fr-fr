---
title: <MethodInstantiation> Élément (.NET Native)
ms.date: 03/30/2017
ms.assetid: a3355d78-2a88-4109-8521-830d7cae260a
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ae15e6d61267feb0388170ee27dcd939035329b0
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61867079"
---
# <a name="methodinstantiation-element-net-native"></a>\<MethodInstantiation >, élément (.NET Native)
Applique la stratégie de réflexion runtime à une méthode générique construite.  
  
## <a name="syntax"></a>Syntaxe  
  
```xml  
<MethodInstantiation Name="method_name"  
                     Signature="method_signature"  
                     Arguments="method_arguments"  
                     Browse="policy_type"  
                     Dynamic="policy_type" />  
```  
  
## <a name="attributes-and-elements"></a>Attributs et éléments  
 Les sections suivantes décrivent des attributs, des éléments enfants et des éléments parents.  
  
### <a name="attributes"></a>Attributs  
  
|Attribut|Type d'attribut|Description|  
|---------------|--------------------|-----------------|  
|`Name`|Général|Attribut requis. Spécifie le nom de la méthode.|  
|`Signature`|Général|Attribut facultatif. Spécifie les paramètres nommés de la méthode. Si plusieurs paramètres nommés sont présents, ils sont séparés par des virgules. L'attribut `Signature` est utilisé pour différencier les méthodes surchargées.|  
|`Arguments`|Général|Attribut requis. Spécifie les arguments de type générique. Si plusieurs arguments sont présents, ils sont séparés par des virgules.|  
|`Browse`|Réflexion|Attribut facultatif. Contrôle la demande d'informations sur une méthode ou l'énumération de celle-ci, mais ne permet pas d'effectuer un appel dynamique au moment de l'exécution.|  
|`Dynamic`|Réflexion|Attribut facultatif. Contrôle l'accès à un constructeur ou à une méthode au moment de l'exécution pour activer la programmation dynamique. Cette stratégie garantit que le membre peut être appelé dynamiquement au moment de l'exécution.|  
  
## <a name="name-attribute"></a>Name (attribut)  
  
|Value|Description|  
|-----------|-----------------|  
|*nom_méthode*|Nom de la méthode. Le type de la méthode est défini par le [\<Type>](../../../docs/framework/net-native/type-element-net-native.md) parent ou l’élément [\<TypeInstantiation>](../../../docs/framework/net-native/typeinstantiation-element-net-native.md).|  
  
## <a name="signature-attribute"></a>Attribut de signature  
  
|Value|Description|  
|-----------|-----------------|  
|*signature_méthode*|Spécifie les paramètres nommés de la méthode. Si plusieurs paramètres sont présents, ils sont séparés par des virgules.|  
  
## <a name="arguments-attribute"></a>Attribut Arguments  
  
|Value|Description|  
|-----------|-----------------|  
|*arguments_méthode*|Spécifie les arguments de type générique. Si plusieurs arguments sont présents, ils sont séparés par des virgules. Chaque argument doit être composé du nom de type qualifié complet.|  
  
## <a name="all-other-attributes"></a>Tous les autres attributs  
  
|Value|Description|  
|-----------|-----------------|  
|*paramètre_stratégie*|Paramètre à appliquer à ce type de stratégie pour la méthode. Les valeurs possibles sont `Auto`, `Excluded`, `Included` et `Required`. Pour plus d’informations, consultez [Paramètres de stratégie de directive runtime](../../../docs/framework/net-native/runtime-directive-policy-settings.md).|  
  
### <a name="child-elements"></a>Éléments enfants  
 Aucun.  
  
### <a name="parent-elements"></a>Éléments parents  
  
|Élément|Description|  
|-------------|-----------------|  
|[\<Type>](../../../docs/framework/net-native/type-element-net-native.md)|Applique la stratégie de réflexion à un type et à tous ses membres.|  
|[\<TypeInstantiation>](../../../docs/framework/net-native/typeinstantiation-element-net-native.md)|Applique la stratégie de réflexion à un type générique construit et à tous ses membres.|  
  
## <a name="remarks"></a>Notes  
 L'élément `<MethodInstantiation>` remplace la stratégie de réflexion runtime de la méthode générique ouverte correspondante.  
  
## <a name="see-also"></a>Voir aussi

- [Guide de référence du fichier de configuration des directives runtime (rd.xml)](../../../docs/framework/net-native/runtime-directives-rd-xml-configuration-file-reference.md)
- [Éléments de directive runtime](../../../docs/framework/net-native/runtime-directive-elements.md)
- [Paramètres de stratégie de directive runtime](../../../docs/framework/net-native/runtime-directive-policy-settings.md)
- [\<Method>, élément](../../../docs/framework/net-native/method-element-net-native.md)
