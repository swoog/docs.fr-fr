---
title: '&lt;paramref&gt; (Guide de programmation C#)'
ms.date: 07/20/2015
f1_keywords:
- paramref
- <paramref>
helpviewer_keywords:
- <paramref> C# XML tag
- paramref C# XML tag
ms.assetid: 756c24c1-f591-40e8-a838-559761539b0b
ms.openlocfilehash: 0b0d49b90e097e23d3878281f9accda14b057720
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33325131"
---
# <a name="ltparamrefgt-c-programming-guide"></a><span data-ttu-id="f10f1-102">&lt;paramref&gt; (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="f10f1-102">&lt;paramref&gt; (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="f10f1-103">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f10f1-103">Syntax</span></span>  
  
```xml  
<paramref name="name"/>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="f10f1-104">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f10f1-104">Parameters</span></span>  
 `name`  
 <span data-ttu-id="f10f1-105">Nom du paramètre auquel faire référence.</span><span class="sxs-lookup"><span data-stu-id="f10f1-105">The name of the parameter to refer to.</span></span> <span data-ttu-id="f10f1-106">Mettez le nom entre guillemets doubles (" ").</span><span class="sxs-lookup"><span data-stu-id="f10f1-106">Enclose the name in double quotation marks (" ").</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="f10f1-107">Notes</span><span class="sxs-lookup"><span data-stu-id="f10f1-107">Remarks</span></span>  
 <span data-ttu-id="f10f1-108">La balise \<paramref> vous offre un moyen d’indiquer qu’un mot dans les commentaires du code, par exemple dans un bloc \<summary> ou \<remarks>, fait référence à un paramètre.</span><span class="sxs-lookup"><span data-stu-id="f10f1-108">The \<paramref> tag gives you a way to indicate that a word in the code comments, for example in a \<summary> or \<remarks> block refers to a parameter.</span></span> <span data-ttu-id="f10f1-109">Le fichier XML peut être traité de manière à mettre en forme ce mot d’une façon particulière, par exemple en gras ou en italique.</span><span class="sxs-lookup"><span data-stu-id="f10f1-109">The XML file can be processed to format this word in some distinct way, such as with a bold or italic font.</span></span>  
  
 <span data-ttu-id="f10f1-110">Compilez avec [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="f10f1-110">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f10f1-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="f10f1-111">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#7](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/paramref_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="f10f1-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f10f1-112">See Also</span></span>  
 [<span data-ttu-id="f10f1-113">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="f10f1-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="f10f1-114">Balises recommandées pour les commentaires de documentation</span><span class="sxs-lookup"><span data-stu-id="f10f1-114">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
