---
title: Références d'objets interopérables
ms.date: 03/30/2017
ms.assetid: cb8da4c8-08ca-4220-a16b-e04c8f527f1b
ms.openlocfilehash: 9cbbd5a34269a7c4a5c33d72487a02df21f2f0fb
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59222703"
---
# <a name="interoperable-object-references"></a>Références d'objets interopérables
Par défaut, le <xref:System.Runtime.Serialization.DataContractSerializer> sérialise les objets par valeur. Vous pouvez utiliser la propriété <xref:System.Runtime.Serialization.DataContractAttribute.IsReference%2A> pour indiquer au sérialiseur de contrat de données qu'il conserve les références d'objet lors de la sérialisation des objets du type.  
  
## <a name="generated-xml"></a>XML généré  
 À titre d'exemple, considérez l'objet suivant :  
  
```  
[DataContract]  
public class X  
{  
    SomeClass someInstance = new SomeClass();  
    [DataMember]  
    public SomeClass A = someInstance;  
    [DataMember]  
    public SomeClass B = someInstance;  
}  
  
public class SomeClass   
{  
}  
```  
  
 Lorsque <xref:System.Runtime.Serialization.DataContractSerializer.PreserveObjectReferences%2A> a la valeur `false` (valeur par défaut), le code XML suivant est généré :  
  
```xml  
<X>  
   <A>contents of someInstance</A>  
   <B>contents of someInstance</B>  
</X>  
```  
  
 Lorsque <xref:System.Runtime.Serialization.DataContractSerializer.PreserveObjectReferences%2A> a la valeur `true`, le code XML suivant est généré :  
  
```xml  
<X>  
   <A id="1">contents of someInstance</A>  
   <B ref="1" />  
</X>  
```  
  
 Toutefois, <xref:System.Runtime.Serialization.XsdDataContractExporter> ne décrit pas les attributs `id` et `ref` dans son schéma, y compris quand la propriété `preserveObjectReferences` a la valeur `true`.  
  
## <a name="using-isreference"></a>Utilisation d'IsReference  
 Pour générer des informations de référence d'objet valides d'après le schéma qui les décrit, appliquez l'attribut <xref:System.Runtime.Serialization.DataContractAttribute> à un type et attribuez à l'indicateur <xref:System.Runtime.Serialization.DataContractAttribute.IsReference%2A> la valeur `true`. En utilisant `IsReference` dans la classe illustrée dans l'exemple `X` précédent :  
  
 `[DataContract(IsReference=true)] public class X`  
  
 `{`  
  
 `SomeClass someInstance = new SomeClass();`  
  
 `[DataMember]`  
  
 `public SomeClass A = someInstance;`  
  
 `[DataMember]`  
  
 `public SomeClass B = someInstance;`  
  
 `}`  
  
 `public class SomeClass`  
  
 `{`  
  
 `}`  
  
 Le XML généré est le suivant :  
  
 `<X>`  
  
 `<A id="1">`  
  
 `<Value>contents of A</Value>`  
  
 `</A>`  
  
 `<B ref="1">`  
  
 `</B>`  
  
 `</X>`  
  
 L'utilisation d'`IsReference` garantit la conformité dans l'aller-retour du message. Sans lui, lorsqu'un type est généré à partir du schéma, les données renvoyées comme XML pour ce type ne sont pas forcément compatibles avec le schéma supposé initialement. En d'autres termes, bien que les attributs `id` et `ref` aient été sérialisés, le schéma d'origine aurait pu empêcher ces attributs (ou tous les attributs) d'apparaître dans le XML. Lorsqu'`IsReference` est appliqué à un membre de données, ce dernier continue à être reconnu comme étant « référençable » lorsqu'il fait l'aller-retour.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Runtime.Serialization.DataContractAttribute>
- <xref:System.Runtime.Serialization.CollectionDataContractAttribute>
- <xref:System.Runtime.Serialization.DataContractAttribute.IsReference%2A>
- <xref:System.Runtime.Serialization.CollectionDataContractAttribute.IsReference%2A>
