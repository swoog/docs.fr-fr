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
ms.openlocfilehash: b290315cd9c36281c110bbf0c6246468a1a899b2
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55259161"
---
# <a name="remarks-c-programming-guide"></a><span data-ttu-id="733a4-102">\<remarks> (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="733a4-102">\<remarks> (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="733a4-103">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="733a4-103">Syntax</span></span>  
  
```xml  
<remarks>description</remarks>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="733a4-104">Paramètres</span><span class="sxs-lookup"><span data-stu-id="733a4-104">Parameters</span></span>  
 `Description`  
 <span data-ttu-id="733a4-105">Description du membre.</span><span class="sxs-lookup"><span data-stu-id="733a4-105">A description of the member.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="733a4-106">Notes</span><span class="sxs-lookup"><span data-stu-id="733a4-106">Remarks</span></span>  
 <span data-ttu-id="733a4-107">La balise \<remarks> permet d’ajouter des informations sur un type en complétant les informations spécifiées par [\<summary>](../../../csharp/programming-guide/xmldoc/summary.md).</span><span class="sxs-lookup"><span data-stu-id="733a4-107">The \<remarks> tag is used to add information about a type, supplementing the information specified with [\<summary>](../../../csharp/programming-guide/xmldoc/summary.md).</span></span> <span data-ttu-id="733a4-108">Ces informations sont affichées dans la fenêtre Explorateur d’objets.</span><span class="sxs-lookup"><span data-stu-id="733a4-108">This information is displayed in the Object Browser window.</span></span>  
  
 <span data-ttu-id="733a4-109">Compilez avec [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="733a4-109">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="733a4-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="733a4-110">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#9](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/remarks_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="733a4-111">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="733a4-111">See also</span></span>

- [<span data-ttu-id="733a4-112">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="733a4-112">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="733a4-113">Balises recommandées pour les commentaires de documentation</span><span class="sxs-lookup"><span data-stu-id="733a4-113">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
