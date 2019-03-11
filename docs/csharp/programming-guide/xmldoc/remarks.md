---
title: <remarks> - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- remarks
- <remarks>
helpviewer_keywords:
- remarks C# XML tag
- <remarks> C# XML tag
ms.assetid: f8641391-31f3-4735-af7a-c502a5b6a251
ms.openlocfilehash: b2e91b868c35773033418c796b7c43b08e87a28b
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57480375"
---
# <a name="remarks-c-programming-guide"></a><span data-ttu-id="9a987-102">\<remarks> (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="9a987-102">\<remarks> (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="9a987-103">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a987-103">Syntax</span></span>  
  
```xml  
<remarks>description</remarks>  
```  
  
## <a name="parameters"></a><span data-ttu-id="9a987-104">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9a987-104">Parameters</span></span>  
 `Description`  
 <span data-ttu-id="9a987-105">Description du membre.</span><span class="sxs-lookup"><span data-stu-id="9a987-105">A description of the member.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="9a987-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="9a987-106">Remarks</span></span>  
 <span data-ttu-id="9a987-107">La balise \<remarks> permet d’ajouter des informations sur un type en complétant les informations spécifiées par [\<summary>](../../../csharp/programming-guide/xmldoc/summary.md).</span><span class="sxs-lookup"><span data-stu-id="9a987-107">The \<remarks> tag is used to add information about a type, supplementing the information specified with [\<summary>](../../../csharp/programming-guide/xmldoc/summary.md).</span></span> <span data-ttu-id="9a987-108">Ces informations sont affichées dans la fenêtre Explorateur d’objets.</span><span class="sxs-lookup"><span data-stu-id="9a987-108">This information is displayed in the Object Browser window.</span></span>  
  
 <span data-ttu-id="9a987-109">Compilez avec [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="9a987-109">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9a987-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="9a987-110">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#9](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideDocComments/CS/DocComments.cs#9)]  
  
## <a name="see-also"></a><span data-ttu-id="9a987-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9a987-111">See also</span></span>

- [<span data-ttu-id="9a987-112">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="9a987-112">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="9a987-113">Balises recommandées pour les commentaires de documentation</span><span class="sxs-lookup"><span data-stu-id="9a987-113">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
