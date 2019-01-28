---
title: '&lt;remarks&gt; - Guide de programmation C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- remarks
- <remarks>
helpviewer_keywords:
- remarks C# XML tag
- <remarks> C# XML tag
ms.assetid: f8641391-31f3-4735-af7a-c502a5b6a251
ms.openlocfilehash: faeb1b07d4778f56ae854d5ece93588cbe5848f6
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54536046"
---
# <a name="ltremarksgt-c-programming-guide"></a><span data-ttu-id="b8152-102">&lt;remarks&gt; (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="b8152-102">&lt;remarks&gt; (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="b8152-103">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b8152-103">Syntax</span></span>  
  
```xml  
<remarks>description</remarks>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b8152-104">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b8152-104">Parameters</span></span>  
 `Description`  
 <span data-ttu-id="b8152-105">Description du membre.</span><span class="sxs-lookup"><span data-stu-id="b8152-105">A description of the member.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b8152-106">Notes</span><span class="sxs-lookup"><span data-stu-id="b8152-106">Remarks</span></span>  
 <span data-ttu-id="b8152-107">La balise \<remarks> permet d’ajouter des informations sur un type en complétant les informations spécifiées par [\<summary>](../../../csharp/programming-guide/xmldoc/summary.md).</span><span class="sxs-lookup"><span data-stu-id="b8152-107">The \<remarks> tag is used to add information about a type, supplementing the information specified with [\<summary>](../../../csharp/programming-guide/xmldoc/summary.md).</span></span> <span data-ttu-id="b8152-108">Ces informations sont affichées dans la fenêtre Explorateur d’objets.</span><span class="sxs-lookup"><span data-stu-id="b8152-108">This information is displayed in the Object Browser window.</span></span>  
  
 <span data-ttu-id="b8152-109">Compilez avec [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="b8152-109">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b8152-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="b8152-110">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#9](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/remarks_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="b8152-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b8152-111">See also</span></span>

- [<span data-ttu-id="b8152-112">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="b8152-112">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="b8152-113">Balises recommandées pour les commentaires de documentation</span><span class="sxs-lookup"><span data-stu-id="b8152-113">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
