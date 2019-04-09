---
title: Classement des membres de données
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data contracts [WCF], ordering members
ms.assetid: 0658a47d-b6e5-4ae0-ba72-ababc3c6ff33
ms.openlocfilehash: c78cc682c0776bfb0ce09dec7ba1ff8cab504285
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59198567"
---
# <a name="data-member-order"></a><span data-ttu-id="221c4-102">Classement des membres de données</span><span class="sxs-lookup"><span data-stu-id="221c4-102">Data Member Order</span></span>
<span data-ttu-id="221c4-103">Dans certaines applications, il peut s'avérer utile de connaître l'ordre dans lequel les données émanant des divers membres de données sont envoyées ou l'ordre selon lequel leur réception est attendue (il peut, par exemple s'agir de l'ordre dans lequel les données apparaissent dans le langage XML sérialisé).</span><span class="sxs-lookup"><span data-stu-id="221c4-103">In some applications, it is useful to know the order in which data from the various data members is sent or is expected to be received (such as the order in which data appears in the serialized XML).</span></span> <span data-ttu-id="221c4-104">Dans certains cas, la modification de cet ordre peut s'avérer nécessaire.</span><span class="sxs-lookup"><span data-stu-id="221c4-104">Sometimes it may be necessary to change this order.</span></span> <span data-ttu-id="221c4-105">Cette rubrique contient des explications sur les règles régissant ces types de classements.</span><span class="sxs-lookup"><span data-stu-id="221c4-105">This topic explains the ordering rules.</span></span>  
  
## <a name="basic-rules"></a><span data-ttu-id="221c4-106">Règles de base</span><span class="sxs-lookup"><span data-stu-id="221c4-106">Basic Rules</span></span>  
 <span data-ttu-id="221c4-107">Les règles de base concernant le classement des données sont notamment :</span><span class="sxs-lookup"><span data-stu-id="221c4-107">The basic rules for data ordering include:</span></span>  
  
-   <span data-ttu-id="221c4-108">Si un type de contrat de données fait partie d'une hiérarchie d'héritage, les membres de données des types de base de ce type sont toujours classés en premier.</span><span class="sxs-lookup"><span data-stu-id="221c4-108">If a data contract type is a part of an inheritance hierarchy, data members of its base types are always first in the order.</span></span>  
  
-   <span data-ttu-id="221c4-109">Viennent ensuite, par ordre alphabétique, les membres de données du type en cours dont la propriété <xref:System.Runtime.Serialization.DataMemberAttribute.Order%2A> de l'attribut <xref:System.Runtime.Serialization.DataMemberAttribute> n'est pas définie.</span><span class="sxs-lookup"><span data-stu-id="221c4-109">Next in order are the current type’s data members that do not have the <xref:System.Runtime.Serialization.DataMemberAttribute.Order%2A> property of the <xref:System.Runtime.Serialization.DataMemberAttribute> attribute set, in alphabetical order.</span></span>  
  
-   <span data-ttu-id="221c4-110">Viennent ensuite tous les membres de données dont la propriété <xref:System.Runtime.Serialization.DataMemberAttribute.Order%2A> de l'attribut <xref:System.Runtime.Serialization.DataMemberAttribute> est définie.</span><span class="sxs-lookup"><span data-stu-id="221c4-110">Next are any data members that have the <xref:System.Runtime.Serialization.DataMemberAttribute.Order%2A> property of the <xref:System.Runtime.Serialization.DataMemberAttribute> attribute set.</span></span> <span data-ttu-id="221c4-111">Ils sont d'abord classés en fonction de la valeur de la propriété `Order`, puis par ordre alphabétique si plusieurs membres ont une certaine valeur `Order`.</span><span class="sxs-lookup"><span data-stu-id="221c4-111">These are ordered by the value of the `Order` property first and then alphabetically if there is more than one member of a certain `Order` value.</span></span> <span data-ttu-id="221c4-112">Les valeurs de classement peuvent être ignorées.</span><span class="sxs-lookup"><span data-stu-id="221c4-112">Order values may be skipped.</span></span>  
  
 <span data-ttu-id="221c4-113">L'ordre alphabétique est établi par l'appel de la méthode <xref:System.String.CompareOrdinal%2A>.</span><span class="sxs-lookup"><span data-stu-id="221c4-113">Alphabetical order is established by calling the <xref:System.String.CompareOrdinal%2A> method.</span></span>  
  
## <a name="examples"></a><span data-ttu-id="221c4-114">Exemples</span><span class="sxs-lookup"><span data-stu-id="221c4-114">Examples</span></span>  
 <span data-ttu-id="221c4-115">Prenons le code suivant.</span><span class="sxs-lookup"><span data-stu-id="221c4-115">Consider the following code.</span></span>  
  
 [!code-csharp[C_DataContractNames#4](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_datacontractnames/cs/source.cs#4)]
 [!code-vb[C_DataContractNames#4](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/c_datacontractnames/vb/source.vb#4)]  
  
 <span data-ttu-id="221c4-116">Le langage XML généré ressemble au langage suivant.</span><span class="sxs-lookup"><span data-stu-id="221c4-116">The XML produced is similar to the following.</span></span>  
  
```xml  
<DerivedType>  
    <!-- Zebra is a base data member, and appears first. -->  
    <zebra/>   
  
    <!-- Cat has no Order, appears alphabetically first. -->  
    <cat/>  
  
   <!-- Dog has no Order, appears alphabetically last. -->  
    <dog/>   
  
    <!-- Bird is the member with the smallest Order value -->  
    <bird/>  
  
    <!-- Albatross has the next Order value, alphabetically first. -->  
    <albatross/>  
  
    <!-- Parrot, with the next Order value, alphabetically last. -->  
     <parrot/>  
  
    <!-- Antelope is the member with the highest Order value. Note that   
    Order=2 is skipped -->  
     <antelope/>   
</DerivedType>  
```  
  
## <a name="see-also"></a><span data-ttu-id="221c4-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="221c4-117">See also</span></span>

- <xref:System.Runtime.Serialization.DataContractAttribute>
- [<span data-ttu-id="221c4-118">Équivalence de contrats de données</span><span class="sxs-lookup"><span data-stu-id="221c4-118">Data Contract Equivalence</span></span>](../../../../docs/framework/wcf/feature-details/data-contract-equivalence.md)
- [<span data-ttu-id="221c4-119">Utilisation de contrats de données</span><span class="sxs-lookup"><span data-stu-id="221c4-119">Using Data Contracts</span></span>](../../../../docs/framework/wcf/feature-details/using-data-contracts.md)
