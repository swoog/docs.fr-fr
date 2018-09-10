---
title: '&lt;remarks&gt; (Guide de programmation C#)'
ms.date: 07/20/2015
f1_keywords:
- remarks
- <remarks>
helpviewer_keywords:
- remarks C# XML tag
- <remarks> C# XML tag
ms.assetid: f8641391-31f3-4735-af7a-c502a5b6a251
ms.openlocfilehash: 10d8dbe7862514ff2417054b6c1c5e9ef15e20ff
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43514199"
---
# <a name="ltremarksgt-c-programming-guide"></a><span data-ttu-id="0885c-102">&lt;remarks&gt; (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="0885c-102">&lt;remarks&gt; (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="0885c-103">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0885c-103">Syntax</span></span>  
  
```xml  
<remarks>description</remarks>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0885c-104">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0885c-104">Parameters</span></span>  
 `Description`  
 <span data-ttu-id="0885c-105">Description du membre.</span><span class="sxs-lookup"><span data-stu-id="0885c-105">A description of the member.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0885c-106">Notes</span><span class="sxs-lookup"><span data-stu-id="0885c-106">Remarks</span></span>  
 <span data-ttu-id="0885c-107">La balise \<remarks> permet d’ajouter des informations sur un type en complétant les informations spécifiées par [\<summary>](../../../csharp/programming-guide/xmldoc/summary.md).</span><span class="sxs-lookup"><span data-stu-id="0885c-107">The \<remarks> tag is used to add information about a type, supplementing the information specified with [\<summary>](../../../csharp/programming-guide/xmldoc/summary.md).</span></span> <span data-ttu-id="0885c-108">Ces informations sont affichées dans la fenêtre Explorateur d’objets.</span><span class="sxs-lookup"><span data-stu-id="0885c-108">This information is displayed in the Object Browser window.</span></span>  
  
 <span data-ttu-id="0885c-109">Compilez avec [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="0885c-109">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0885c-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="0885c-110">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#9](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/remarks_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="0885c-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0885c-111">See Also</span></span>

- [<span data-ttu-id="0885c-112">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="0885c-112">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="0885c-113">Balises recommandées pour les commentaires de documentation</span><span class="sxs-lookup"><span data-stu-id="0885c-113">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
