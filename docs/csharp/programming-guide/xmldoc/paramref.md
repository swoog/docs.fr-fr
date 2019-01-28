---
title: '&lt;paramref&gt; - Guide de programmation C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- paramref
- <paramref>
helpviewer_keywords:
- <paramref> C# XML tag
- paramref C# XML tag
ms.assetid: 756c24c1-f591-40e8-a838-559761539b0b
ms.openlocfilehash: 21f8eb293a006a748c876a3b816eae3a799d3d7c
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54640886"
---
# <a name="ltparamrefgt-c-programming-guide"></a><span data-ttu-id="b807a-102">&lt;paramref&gt; (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="b807a-102">&lt;paramref&gt; (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="b807a-103">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b807a-103">Syntax</span></span>  
  
```xml  
<paramref name="name"/>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="b807a-104">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b807a-104">Parameters</span></span>  
 `name`  
 <span data-ttu-id="b807a-105">Nom du paramètre auquel faire référence.</span><span class="sxs-lookup"><span data-stu-id="b807a-105">The name of the parameter to refer to.</span></span> <span data-ttu-id="b807a-106">Mettez le nom entre guillemets doubles (" ").</span><span class="sxs-lookup"><span data-stu-id="b807a-106">Enclose the name in double quotation marks (" ").</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="b807a-107">Notes</span><span class="sxs-lookup"><span data-stu-id="b807a-107">Remarks</span></span>  
 <span data-ttu-id="b807a-108">La balise \<paramref> vous offre un moyen d’indiquer qu’un mot dans les commentaires du code, par exemple dans un bloc \<summary> ou \<remarks>, fait référence à un paramètre.</span><span class="sxs-lookup"><span data-stu-id="b807a-108">The \<paramref> tag gives you a way to indicate that a word in the code comments, for example in a \<summary> or \<remarks> block refers to a parameter.</span></span> <span data-ttu-id="b807a-109">Le fichier XML peut être traité de manière à mettre en forme ce mot d’une façon particulière, par exemple en gras ou en italique.</span><span class="sxs-lookup"><span data-stu-id="b807a-109">The XML file can be processed to format this word in some distinct way, such as with a bold or italic font.</span></span>  
  
 <span data-ttu-id="b807a-110">Compilez avec [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="b807a-110">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b807a-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="b807a-111">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#7](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/paramref_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="b807a-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b807a-112">See also</span></span>

- [<span data-ttu-id="b807a-113">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="b807a-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="b807a-114">Balises recommandées pour les commentaires de documentation</span><span class="sxs-lookup"><span data-stu-id="b807a-114">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
