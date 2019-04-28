---
title: Références d’objets interopérables
ms.date: 04/15/2019
ms.assetid: cb8da4c8-08ca-4220-a16b-e04c8f527f1b
ms.openlocfilehash: ada9084f6ac3c97dc641571c0cb8379a2fac68a8
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61918968"
---
# <a name="interoperable-object-references"></a>Références d’objets interopérables
Par défaut, <xref:System.Runtime.Serialization.DataContractSerializer> sérialise les objets par valeur. Vous pouvez utiliser le <xref:System.Runtime.Serialization.DataContractAttribute.IsReference%2A> propriété pour indiquer le sérialiseur de contrat de données pour conserver les références d’objet lors de la sérialisation d’objets.  
  
## <a name="generated-xml"></a>XML généré  
 À titre d'exemple, considérez l'objet suivant :  
  
```csharp  
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
   <B ref="1"></B>  
</X>  
```  
  
 Toutefois, <xref:System.Runtime.Serialization.XsdDataContractExporter> ne décrit pas le `id` et `ref` attributs dans son schéma, même lorsque le `preserveObjectReferences` propriété est définie sur `true`.  
  
## <a name="using-isreference"></a>Utilisation d'IsReference  
 Pour générer des informations de référence d’objet sont valides selon le schéma qui le décrit, appliquez le <xref:System.Runtime.Serialization.DataContractAttribute> à un type d’attribut, puis définissez le <xref:System.Runtime.Serialization.DataContractAttribute.IsReference%2A> indicateur `true`. L’exemple suivant modifie la classe `X` dans l’exemple précédent en ajoutant `IsReference`:  
  
```csharp
[DataContract(IsReference=true)]
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
````

 Le XML généré est le suivant :  

```xml
<X>  
    <A id="1">
        <Value>contents of A</Value>  
    </A> 
    <B ref="1"></B>  
</X>
```  
  
 L'utilisation d'`IsReference` garantit la conformité dans l'aller-retour du message. Sans lui, lorsqu’un type est généré à partir du schéma, la sortie XML pour type n’est pas forcément compatible avec le schéma supposé initialement. En d'autres termes, bien que les attributs `id` et `ref` aient été sérialisés, le schéma d'origine aurait pu empêcher ces attributs (ou tous les attributs) d'apparaître dans le XML. Avec `IsReference` appliqué à un membre de données, le membre continue à être reconnu en tant que *référençable* quand effectuer un aller-retour.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Runtime.Serialization.DataContractAttribute>
- <xref:System.Runtime.Serialization.CollectionDataContractAttribute>
- <xref:System.Runtime.Serialization.DataContractAttribute.IsReference?displayProperty=nameWithType>
- <xref:System.Runtime.Serialization.CollectionDataContractAttribute.IsReference?displayProperty=nameWithType>
