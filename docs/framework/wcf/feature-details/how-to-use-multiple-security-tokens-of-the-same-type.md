---
title: 'Procédure : Utiliser plusieurs jetons de sécurité du même Type'
ms.date: 03/30/2017
ms.assetid: cf179f48-4ed4-4caa-86a5-ef8eecc231cd
ms.openlocfilehash: 40fc95c905f8923b8aaf2c97fb9dc2b937dfb06f
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54691345"
---
# <a name="how-to-use-multiple-security-tokens-of-the-same-type"></a><span data-ttu-id="7f731-102">Procédure : Utiliser plusieurs jetons de sécurité du même Type</span><span class="sxs-lookup"><span data-stu-id="7f731-102">How to: Use Multiple Security Tokens of the Same Type</span></span>
-   <span data-ttu-id="7f731-103">Dans le [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] 3.0, un message client ne pouvait contenir qu'un jeton d'un type donné.</span><span class="sxs-lookup"><span data-stu-id="7f731-103">In [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] 3.0, a client message only contained one token of any given type.</span></span> <span data-ttu-id="7f731-104">Désormais, les messages peuvent contenir plusieurs jetons d'un type donné.</span><span class="sxs-lookup"><span data-stu-id="7f731-104">Now client messages can contain multiple tokens of a type.</span></span> <span data-ttu-id="7f731-105">Cette rubrique explique comment inclure plusieurs jetons du même type dans un message client.</span><span class="sxs-lookup"><span data-stu-id="7f731-105">This topic shows how to include multiple tokens of the same type in a client message.</span></span>  
  
-   <span data-ttu-id="7f731-106">Notez que vous ne pouvez pas configurer un service ainsi : un service peut contenir un seul jeton de prise en charge.</span><span class="sxs-lookup"><span data-stu-id="7f731-106">Note that you cannot configure a service in this way: a service can contain only one supporting token.</span></span>  
  
### <a name="to-use-multiple-security-tokens-of-the-same-type"></a><span data-ttu-id="7f731-107">Pour utiliser plusieurs jetons de sécurité du même type</span><span class="sxs-lookup"><span data-stu-id="7f731-107">To use multiple security tokens of the same type</span></span>  
  
1.  <span data-ttu-id="7f731-108">Créez une collection d'éléments de liaison vide à remplir.</span><span class="sxs-lookup"><span data-stu-id="7f731-108">Create an empty binding element collection to be populated.</span></span>  
  
     [!code-csharp[C_CustomBinding#9](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_custombinding/cs/c_custombinding.cs#9)]  
  
2.  <span data-ttu-id="7f731-109">Créez un <xref:System.ServiceModel.Channels.SecurityBindingElement> en appelant <xref:System.ServiceModel.Channels.SecurityBindingElement.CreateMutualCertificateBindingElement%2A>.</span><span class="sxs-lookup"><span data-stu-id="7f731-109">Create a <xref:System.ServiceModel.Channels.SecurityBindingElement> by calling <xref:System.ServiceModel.Channels.SecurityBindingElement.CreateMutualCertificateBindingElement%2A>.</span></span>  
  
     [!code-csharp[C_CustomBinding#10](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_custombinding/cs/c_custombinding.cs#10)]  
  
3.  <span data-ttu-id="7f731-110">Créez une collection <xref:System.ServiceModel.Security.Tokens.SupportingTokenParameters>.</span><span class="sxs-lookup"><span data-stu-id="7f731-110">Create a <xref:System.ServiceModel.Security.Tokens.SupportingTokenParameters> collection.</span></span>  
  
     [!code-csharp[C_CustomBinding#11](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_custombinding/cs/c_custombinding.cs#11)]  
  
4.  <span data-ttu-id="7f731-111">Ajoutez des jetons SAML à la collection.</span><span class="sxs-lookup"><span data-stu-id="7f731-111">Add SAML tokens to the collection.</span></span>  
  
     [!code-csharp[C_CustomBinding#12](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_custombinding/cs/c_custombinding.cs#12)]  
  
5.  <span data-ttu-id="7f731-112">Ajoutez la collection à <xref:System.ServiceModel.Channels.SecurityBindingElement>.</span><span class="sxs-lookup"><span data-stu-id="7f731-112">Add the collection to the <xref:System.ServiceModel.Channels.SecurityBindingElement>.</span></span>  
  
     [!code-csharp[C_CustomBinding#13](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_custombinding/cs/c_custombinding.cs#13)]  
  
6.  <span data-ttu-id="7f731-113">Ajoutez des éléments de liaison à la collection d'éléments de liaison.</span><span class="sxs-lookup"><span data-stu-id="7f731-113">Add binding elements to the binding element collection.</span></span>  
  
     [!code-csharp[C_CustomBinding#14](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_custombinding/cs/c_custombinding.cs#14)]  
  
7.  <span data-ttu-id="7f731-114">Retournez une nouvelle liaison personnalisée créée à partir de la collection d’éléments de liaison.</span><span class="sxs-lookup"><span data-stu-id="7f731-114">Return a new custom binding created from the binding element collection.</span></span>  
  
     [!code-csharp[C_CustomBinding#15](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_custombinding/cs/c_custombinding.cs#15)]  
  
## <a name="example"></a><span data-ttu-id="7f731-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="7f731-115">Example</span></span>  
 <span data-ttu-id="7f731-116">Vous trouverez ci-dessous la méthode complète décrite par la procédure précédente.</span><span class="sxs-lookup"><span data-stu-id="7f731-116">The following is the entire method described by the preceding procedure.</span></span>  
  
 [!code-csharp[C_CustomBinding#7](../../../../samples/snippets/csharp/VS_Snippets_CFX/c_custombinding/cs/c_custombinding.cs#7)]  
  
## <a name="see-also"></a><span data-ttu-id="7f731-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7f731-117">See also</span></span>
- [<span data-ttu-id="7f731-118">Architecture de sécurité</span><span class="sxs-lookup"><span data-stu-id="7f731-118">Security Architecture</span></span>](https://msdn.microsoft.com/library/16593476-d36a-408d-808c-ae6fd483e28f)
