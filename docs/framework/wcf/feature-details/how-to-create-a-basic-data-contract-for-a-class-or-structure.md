---
title: 'Procédure : Créer un contrat de données de base pour une classe ou Structure'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataMemberAttribute
- DataContractAttribute class
- data contracts [WCF], creating for a class or structure
ms.assetid: bc464889-3070-4a2f-91d2-e788a0f686a7
ms.openlocfilehash: 29105b7f3177403aacf5f8e628f2dceda4e26354
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54747867"
---
# <a name="how-to-create-a-basic-data-contract-for-a-class-or-structure"></a><span data-ttu-id="49fc5-102">Procédure : Créer un contrat de données de base pour une classe ou Structure</span><span class="sxs-lookup"><span data-stu-id="49fc5-102">How to: Create a Basic Data Contract for a Class or Structure</span></span>
<span data-ttu-id="49fc5-103">Cette rubrique illustre les étapes de base pour créer un contrat de données à l'aide d'une classe ou d'une structure.</span><span class="sxs-lookup"><span data-stu-id="49fc5-103">This topic shows the basic steps to create a data contract using a class or structure.</span></span> <span data-ttu-id="49fc5-104">Pour plus d’informations sur les contrats de données et comment elles sont utilisées, consultez [à l’aide de contrats de données](../../../../docs/framework/wcf/feature-details/using-data-contracts.md).</span><span class="sxs-lookup"><span data-stu-id="49fc5-104">For more information about data contracts and how they are used, see [Using Data Contracts](../../../../docs/framework/wcf/feature-details/using-data-contracts.md).</span></span>  
  
 <span data-ttu-id="49fc5-105">Pour obtenir un didacticiel qui vous guide à travers les étapes de création d’un client et le service Windows Communication Foundation (WCF) de base, consultez le [Getting Started Tutorial](../../../../docs/framework/wcf/getting-started-tutorial.md).</span><span class="sxs-lookup"><span data-stu-id="49fc5-105">For a tutorial that walks through the steps of creating a basic Windows Communication Foundation (WCF) service and client, see the [Getting Started Tutorial](../../../../docs/framework/wcf/getting-started-tutorial.md).</span></span> <span data-ttu-id="49fc5-106">Pour un exemple d’application fonctionnel qui se compose d’un service de base et un client, consultez [Basic Data Contract](../../../../docs/framework/wcf/samples/basic-data-contract.md).</span><span class="sxs-lookup"><span data-stu-id="49fc5-106">For a working sample application that consists of a basic service and client, see [Basic Data Contract](../../../../docs/framework/wcf/samples/basic-data-contract.md).</span></span>  
  
### <a name="to-create-a-basic-data-contract-for-a-class-or-structure"></a><span data-ttu-id="49fc5-107">Pour créer un contrat de données de base destiné à une classe ou une structure</span><span class="sxs-lookup"><span data-stu-id="49fc5-107">To create a basic data contract for a class or structure</span></span>  
  
1.  <span data-ttu-id="49fc5-108">Déclarez que le type a un contrat de données en appliquant l'attribut <xref:System.Runtime.Serialization.DataContractAttribute> à la classe.</span><span class="sxs-lookup"><span data-stu-id="49fc5-108">Declare that the type has a data contract by applying the <xref:System.Runtime.Serialization.DataContractAttribute> attribute to the class.</span></span> <span data-ttu-id="49fc5-109">Notez que tous les types publics, y compris ceux sans attributs, sont sérialisables.</span><span class="sxs-lookup"><span data-stu-id="49fc5-109">Note that all public types, including those without attributes, are serializable.</span></span> <span data-ttu-id="49fc5-110">Le <xref:System.Runtime.Serialization.DataContractSerializer> déduit un contrat de données si l'attribut <xref:System.Runtime.Serialization.DataContractAttribute> est absent.</span><span class="sxs-lookup"><span data-stu-id="49fc5-110">The <xref:System.Runtime.Serialization.DataContractSerializer> infers a data contract if the <xref:System.Runtime.Serialization.DataContractAttribute> attribute is absent.</span></span> <span data-ttu-id="49fc5-111">Pour plus d’informations, consultez [Types sérialisables](../../../../docs/framework/wcf/feature-details/serializable-types.md).</span><span class="sxs-lookup"><span data-stu-id="49fc5-111">For more information, see [Serializable Types](../../../../docs/framework/wcf/feature-details/serializable-types.md).</span></span>  
  
2.  <span data-ttu-id="49fc5-112">Définissez les membres (propriétés, champs ou événements) sérialisés en appliquant l'attribut <xref:System.Runtime.Serialization.DataMemberAttribute> à chaque membre.</span><span class="sxs-lookup"><span data-stu-id="49fc5-112">Define the members (properties, fields, or events) that are serialized by applying the <xref:System.Runtime.Serialization.DataMemberAttribute> attribute to each member.</span></span> <span data-ttu-id="49fc5-113">Ces membres sont appelés des membres de données.</span><span class="sxs-lookup"><span data-stu-id="49fc5-113">These members are called data members.</span></span> <span data-ttu-id="49fc5-114">Par défaut, tous les types publics sont sérialisables.</span><span class="sxs-lookup"><span data-stu-id="49fc5-114">By default, all public types are serializable.</span></span> <span data-ttu-id="49fc5-115">Pour plus d’informations, consultez [Types sérialisables](../../../../docs/framework/wcf/feature-details/serializable-types.md).</span><span class="sxs-lookup"><span data-stu-id="49fc5-115">For more information, see [Serializable Types](../../../../docs/framework/wcf/feature-details/serializable-types.md).</span></span>  
  
    > [!NOTE]
    >  <span data-ttu-id="49fc5-116">Vous pouvez appliquer l'attribut <xref:System.Runtime.Serialization.DataMemberAttribute> aux champs privés, ce qui expose les données aux autres.</span><span class="sxs-lookup"><span data-stu-id="49fc5-116">You can apply the <xref:System.Runtime.Serialization.DataMemberAttribute> attribute to private fields, causing the data to be exposed to others.</span></span> <span data-ttu-id="49fc5-117">Vérifiez que le membre ne contient pas de données sensibles.</span><span class="sxs-lookup"><span data-stu-id="49fc5-117">Be sure that the member does not contain sensitive data.</span></span>  
  
## <a name="example"></a><span data-ttu-id="49fc5-118">Exemple</span><span class="sxs-lookup"><span data-stu-id="49fc5-118">Example</span></span>  
 <span data-ttu-id="49fc5-119">L'exemple suivant montre comment créer un contrat de données pour le type `Person` en appliquant les attributs <xref:System.Runtime.Serialization.DataContractAttribute> et <xref:System.Runtime.Serialization.DataMemberAttribute> à la classe et à ses membres.</span><span class="sxs-lookup"><span data-stu-id="49fc5-119">The following example shows how to create a data contract for the `Person` type by applying the <xref:System.Runtime.Serialization.DataContractAttribute> and <xref:System.Runtime.Serialization.DataMemberAttribute> attributes to the class and its members.</span></span>  
  
 [!code-csharp[DataContractAttribute#2](../../../../samples/snippets/csharp/VS_Snippets_CFX/datacontractattribute/cs/overview.cs#2)]
 [!code-vb[DataContractAttribute#2](../../../../samples/snippets/visualbasic/VS_Snippets_CFX/datacontractattribute/vb/overview.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="49fc5-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="49fc5-120">See also</span></span>
- <xref:System.Runtime.Serialization.DataContractAttribute>
- <xref:System.Runtime.Serialization.DataMemberAttribute>
- [<span data-ttu-id="49fc5-121">Utilisation de contrats de données</span><span class="sxs-lookup"><span data-stu-id="49fc5-121">Using Data Contracts</span></span>](../../../../docs/framework/wcf/feature-details/using-data-contracts.md)
- [<span data-ttu-id="49fc5-122">Didacticiel Bien démarrer</span><span class="sxs-lookup"><span data-stu-id="49fc5-122">Getting Started Tutorial</span></span>](../../../../docs/framework/wcf/getting-started-tutorial.md)
- [<span data-ttu-id="49fc5-123">Prise en main</span><span class="sxs-lookup"><span data-stu-id="49fc5-123">Getting Started</span></span>](../../../../docs/framework/wcf/samples/getting-started-sample.md)
