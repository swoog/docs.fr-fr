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
# <a name="interoperable-object-references"></a><span data-ttu-id="eae63-102">Références d’objets interopérables</span><span class="sxs-lookup"><span data-stu-id="eae63-102">Interoperable object references</span></span>
<span data-ttu-id="eae63-103">Par défaut, <xref:System.Runtime.Serialization.DataContractSerializer> sérialise les objets par valeur.</span><span class="sxs-lookup"><span data-stu-id="eae63-103">By default, <xref:System.Runtime.Serialization.DataContractSerializer> serializes objects by value.</span></span> <span data-ttu-id="eae63-104">Vous pouvez utiliser le <xref:System.Runtime.Serialization.DataContractAttribute.IsReference%2A> propriété pour indiquer le sérialiseur de contrat de données pour conserver les références d’objet lors de la sérialisation d’objets.</span><span class="sxs-lookup"><span data-stu-id="eae63-104">You can use the <xref:System.Runtime.Serialization.DataContractAttribute.IsReference%2A> property to instruct the data contract serializer to preserve object references when serializing objects.</span></span>  
  
## <a name="generated-xml"></a><span data-ttu-id="eae63-105">XML généré</span><span class="sxs-lookup"><span data-stu-id="eae63-105">Generated XML</span></span>  
 <span data-ttu-id="eae63-106">À titre d'exemple, considérez l'objet suivant :</span><span class="sxs-lookup"><span data-stu-id="eae63-106">As an example, consider the following object:</span></span>  
  
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
  
 <span data-ttu-id="eae63-107">Lorsque <xref:System.Runtime.Serialization.DataContractSerializer.PreserveObjectReferences%2A> a la valeur `false` (valeur par défaut), le code XML suivant est généré :</span><span class="sxs-lookup"><span data-stu-id="eae63-107">With <xref:System.Runtime.Serialization.DataContractSerializer.PreserveObjectReferences%2A> set to `false` (the default), the following XML is generated:</span></span>  
  
```xml  
<X>  
   <A>contents of someInstance</A>  
   <B>contents of someInstance</B>  
</X>  
```  
  
 <span data-ttu-id="eae63-108">Lorsque <xref:System.Runtime.Serialization.DataContractSerializer.PreserveObjectReferences%2A> a la valeur `true`, le code XML suivant est généré :</span><span class="sxs-lookup"><span data-stu-id="eae63-108">With <xref:System.Runtime.Serialization.DataContractSerializer.PreserveObjectReferences%2A> set to `true`, the following XML is generated:</span></span>  
  
```xml  
<X>  
   <A id="1">contents of someInstance</A>  
   <B ref="1"></B>  
</X>  
```  
  
 <span data-ttu-id="eae63-109">Toutefois, <xref:System.Runtime.Serialization.XsdDataContractExporter> ne décrit pas le `id` et `ref` attributs dans son schéma, même lorsque le `preserveObjectReferences` propriété est définie sur `true`.</span><span class="sxs-lookup"><span data-stu-id="eae63-109">However, <xref:System.Runtime.Serialization.XsdDataContractExporter> doesn't describe the `id` and `ref` attributes in its schema, even when the `preserveObjectReferences` property is set to `true`.</span></span>  
  
## <a name="using-isreference"></a><span data-ttu-id="eae63-110">Utilisation d'IsReference</span><span class="sxs-lookup"><span data-stu-id="eae63-110">Using IsReference</span></span>  
 <span data-ttu-id="eae63-111">Pour générer des informations de référence d’objet sont valides selon le schéma qui le décrit, appliquez le <xref:System.Runtime.Serialization.DataContractAttribute> à un type d’attribut, puis définissez le <xref:System.Runtime.Serialization.DataContractAttribute.IsReference%2A> indicateur `true`.</span><span class="sxs-lookup"><span data-stu-id="eae63-111">To generate object reference information that's valid according to the schema that describes it, apply the <xref:System.Runtime.Serialization.DataContractAttribute> attribute to a type, and set the <xref:System.Runtime.Serialization.DataContractAttribute.IsReference%2A> flag to `true`.</span></span> <span data-ttu-id="eae63-112">L’exemple suivant modifie la classe `X` dans l’exemple précédent en ajoutant `IsReference`:</span><span class="sxs-lookup"><span data-stu-id="eae63-112">The following example modifies class `X` in the previous example by adding `IsReference`:</span></span>  
  
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

 <span data-ttu-id="eae63-113">Le XML généré est le suivant :</span><span class="sxs-lookup"><span data-stu-id="eae63-113">The generated XML is as follows:</span></span>  

```xml
<X>  
    <A id="1">
        <Value>contents of A</Value>  
    </A> 
    <B ref="1"></B>  
</X>
```  
  
 <span data-ttu-id="eae63-114">L'utilisation d'`IsReference` garantit la conformité dans l'aller-retour du message.</span><span class="sxs-lookup"><span data-stu-id="eae63-114">Using `IsReference` ensures compliance on message round-tripping.</span></span> <span data-ttu-id="eae63-115">Sans lui, lorsqu’un type est généré à partir du schéma, la sortie XML pour type n’est pas forcément compatible avec le schéma supposé initialement.</span><span class="sxs-lookup"><span data-stu-id="eae63-115">Without it, when a type is generated from schema, the XML output for that type isn't necessarily compatible with the schema originally assumed.</span></span> <span data-ttu-id="eae63-116">En d'autres termes, bien que les attributs `id` et `ref` aient été sérialisés, le schéma d'origine aurait pu empêcher ces attributs (ou tous les attributs) d'apparaître dans le XML.</span><span class="sxs-lookup"><span data-stu-id="eae63-116">In other words, although the `id` and `ref` attributes were serialized, the original schema could have barred these attributes (or all attributes) from occurring in the XML.</span></span> <span data-ttu-id="eae63-117">Avec `IsReference` appliqué à un membre de données, le membre continue à être reconnu en tant que *référençable* quand effectuer un aller-retour.</span><span class="sxs-lookup"><span data-stu-id="eae63-117">With `IsReference` applied to a data member, the member continues to be recognized as *referenceable* when round-tripped.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eae63-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eae63-118">See also</span></span>

- <xref:System.Runtime.Serialization.DataContractAttribute>
- <xref:System.Runtime.Serialization.CollectionDataContractAttribute>
- <xref:System.Runtime.Serialization.DataContractAttribute.IsReference?displayProperty=nameWithType>
- <xref:System.Runtime.Serialization.CollectionDataContractAttribute.IsReference?displayProperty=nameWithType>
