---
title: "Remplissage de chaînes dans .NET"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-standard
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- strings [.NET Framework], padding
- white space
- PadRight method
- PadLeft method
- padding strings
ms.assetid: 84a9f142-3244-4c90-ba02-21af9bbaff71
caps.latest.revision: 
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.workload:
- dotnet
- dotnetcore
ms.openlocfilehash: ea903c1f950e7c226e043c1fa7276a66126b2512
ms.sourcegitcommit: e7f04439d78909229506b56935a1105a4149ff3d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/23/2017
---
# <a name="padding-strings-in-net"></a><span data-ttu-id="f8c9c-102">Remplissage de chaînes dans .NET</span><span class="sxs-lookup"><span data-stu-id="f8c9c-102">Padding Strings in .NET</span></span>
<span data-ttu-id="f8c9c-103">Utilisez l’une des méthodes <xref:System.String> suivantes pour créer une chaîne qui se compose d’une chaîne d’origine remplie à l’aide de caractères de début ou de fin sur une longueur totale spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f8c9c-103">Use one of the following <xref:System.String> methods to create a new string that consists of an original string that is padded with leading or trailing characters to a specified total length.</span></span> <span data-ttu-id="f8c9c-104">Le caractère de remplissage peut être un espace ou un caractère spécifié ; il apparaît donc aligné à droite ou aligné à gauche.</span><span class="sxs-lookup"><span data-stu-id="f8c9c-104">The padding character can be spaces or a specified character, and consequently appears to be either right-aligned or left-aligned.</span></span>  
  
|<span data-ttu-id="f8c9c-105">Nom de la méthode</span><span class="sxs-lookup"><span data-stu-id="f8c9c-105">Method name</span></span>|<span data-ttu-id="f8c9c-106">Utilisez</span><span class="sxs-lookup"><span data-stu-id="f8c9c-106">Use</span></span>|  
|-----------------|---------|  
|<xref:System.String.PadLeft%2A?displayProperty=nameWithType>|<span data-ttu-id="f8c9c-107">Remplit une chaîne à l’aide de caractères de début sur une longueur totale spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f8c9c-107">Pads a string with leading characters to a specified total length.</span></span>|  
|<xref:System.String.PadRight%2A?displayProperty=nameWithType>|<span data-ttu-id="f8c9c-108">Remplit une chaîne à l’aide de caractères de fin sur une longueur totale spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f8c9c-108">Pads a string with trailing characters to a specified total length.</span></span>|  
  
## <a name="padleft"></a><span data-ttu-id="f8c9c-109">PadLeft</span><span class="sxs-lookup"><span data-stu-id="f8c9c-109">PadLeft</span></span>  
 <span data-ttu-id="f8c9c-110">La méthode <xref:System.String.PadLeft%2A?displayProperty=nameWithType> crée une chaîne en concaténant suffisamment de caractères de remplissage de début à une chaîne d’origine pour atteindre une longueur totale spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f8c9c-110">The <xref:System.String.PadLeft%2A?displayProperty=nameWithType> method creates a new string by concatenating enough leading pad characters to an original string to achieve a specified total length.</span></span> <span data-ttu-id="f8c9c-111">La méthode <xref:System.String.PadLeft%28System.Int32%29?displayProperty=nameWithType> utilise l’espace blanc comme caractère de remplissage et la méthode <xref:System.String.PadLeft%28System.Int32%2CSystem.Char%29?displayProperty=nameWithType> vous permet de spécifier votre propre caractère de remplissage.</span><span class="sxs-lookup"><span data-stu-id="f8c9c-111">The <xref:System.String.PadLeft%28System.Int32%29?displayProperty=nameWithType> method uses white space as the padding character and the <xref:System.String.PadLeft%28System.Int32%2CSystem.Char%29?displayProperty=nameWithType> method enables you to specify your own padding character.</span></span>  
  
 <span data-ttu-id="f8c9c-112">L’exemple de code suivant utilise la méthode <xref:System.String.PadLeft%2A> pour créer une chaîne longue de vingt caractères.</span><span class="sxs-lookup"><span data-stu-id="f8c9c-112">The following code example uses the <xref:System.String.PadLeft%2A> method to create a new string that is twenty characters long.</span></span> <span data-ttu-id="f8c9c-113">L’exemple affiche « `--------Hello World!` » sur la console.</span><span class="sxs-lookup"><span data-stu-id="f8c9c-113">The example displays "`--------Hello World!`" to the console.</span></span>  
  
 [!code-cpp[Conceptual.String.BasicOps#3](../../../samples/snippets/cpp/VS_Snippets_CLR/conceptual.string.basicops/cpp/padding.cpp#3)]
 [!code-csharp[Conceptual.String.BasicOps#3](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.string.basicops/cs/padding.cs#3)]
 [!code-vb[Conceptual.String.BasicOps#3](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.string.basicops/vb/padding.vb#3)]  
  
## <a name="padright"></a><span data-ttu-id="f8c9c-114">PadRight</span><span class="sxs-lookup"><span data-stu-id="f8c9c-114">PadRight</span></span>  
 <span data-ttu-id="f8c9c-115">La méthode <xref:System.String.PadRight%2A?displayProperty=nameWithType> crée une chaîne en concaténant suffisamment de caractères de remplissage de fin à une chaîne d’origine pour atteindre une longueur totale spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f8c9c-115">The <xref:System.String.PadRight%2A?displayProperty=nameWithType> method creates a new string by concatenating enough trailing pad characters to an original string to achieve a specified total length.</span></span> <span data-ttu-id="f8c9c-116">La méthode <xref:System.String.PadRight%28System.Int32%29?displayProperty=nameWithType> utilise l’espace blanc comme caractère de remplissage et la méthode <xref:System.String.PadRight%28System.Int32%2CSystem.Char%29?displayProperty=nameWithType> vous permet de spécifier votre propre caractère de remplissage.</span><span class="sxs-lookup"><span data-stu-id="f8c9c-116">The <xref:System.String.PadRight%28System.Int32%29?displayProperty=nameWithType> method uses white space as the padding character and the <xref:System.String.PadRight%28System.Int32%2CSystem.Char%29?displayProperty=nameWithType> method enables you to specify your own padding character.</span></span>  
  
 <span data-ttu-id="f8c9c-117">L’exemple de code suivant utilise la méthode <xref:System.String.PadRight%2A> pour créer une chaîne longue de vingt caractères.</span><span class="sxs-lookup"><span data-stu-id="f8c9c-117">The following code example uses the <xref:System.String.PadRight%2A> method to create a new string that is twenty characters long.</span></span> <span data-ttu-id="f8c9c-118">L’exemple affiche « `Hello World!--------` » sur la console.</span><span class="sxs-lookup"><span data-stu-id="f8c9c-118">The example displays "`Hello World!--------`" to the console.</span></span>  
  
 [!code-cpp[Conceptual.String.BasicOps#4](../../../samples/snippets/cpp/VS_Snippets_CLR/conceptual.string.basicops/cpp/padding.cpp#4)]
 [!code-csharp[Conceptual.String.BasicOps#4](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.string.basicops/cs/padding.cs#4)]
 [!code-vb[Conceptual.String.BasicOps#4](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.string.basicops/vb/padding.vb#4)]  
  
## <a name="see-also"></a><span data-ttu-id="f8c9c-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f8c9c-119">See Also</span></span>  
 [<span data-ttu-id="f8c9c-120">Opérations de chaînes de base</span><span class="sxs-lookup"><span data-stu-id="f8c9c-120">Basic String Operations</span></span>](../../../docs/standard/base-types/basic-string-operations.md)
