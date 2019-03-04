---
title: <paramref> - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- paramref
- <paramref>
helpviewer_keywords:
- <paramref> C# XML tag
- paramref C# XML tag
ms.assetid: 756c24c1-f591-40e8-a838-559761539b0b
ms.openlocfilehash: e6d6c62c97179d74bdb6bdd88eeb1ee129226fed
ms.sourcegitcommit: 41c0637e894fbcd0713d46d6ef1866f08dc321a2
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/01/2019
ms.locfileid: "57201402"
---
# <a name="paramref-c-programming-guide"></a><span data-ttu-id="62cc6-102">\<paramref> (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="62cc6-102">\<paramref> (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="62cc6-103">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62cc6-103">Syntax</span></span>  
  
```xml  
<paramref name="name"/>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="62cc6-104">Paramètres</span><span class="sxs-lookup"><span data-stu-id="62cc6-104">Parameters</span></span>  
 `name`  
 <span data-ttu-id="62cc6-105">Nom du paramètre auquel faire référence.</span><span class="sxs-lookup"><span data-stu-id="62cc6-105">The name of the parameter to refer to.</span></span> <span data-ttu-id="62cc6-106">Mettez le nom entre guillemets doubles (" ").</span><span class="sxs-lookup"><span data-stu-id="62cc6-106">Enclose the name in double quotation marks (" ").</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="62cc6-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="62cc6-107">Remarks</span></span>  
 <span data-ttu-id="62cc6-108">La balise \<paramref> vous offre un moyen d’indiquer qu’un mot dans les commentaires du code, par exemple dans un bloc \<summary> ou \<remarks>, fait référence à un paramètre.</span><span class="sxs-lookup"><span data-stu-id="62cc6-108">The \<paramref> tag gives you a way to indicate that a word in the code comments, for example in a \<summary> or \<remarks> block refers to a parameter.</span></span> <span data-ttu-id="62cc6-109">Le fichier XML peut être traité de manière à mettre en forme ce mot d’une façon particulière, par exemple en gras ou en italique.</span><span class="sxs-lookup"><span data-stu-id="62cc6-109">The XML file can be processed to format this word in some distinct way, such as with a bold or italic font.</span></span>  
  
 <span data-ttu-id="62cc6-110">Compilez avec [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="62cc6-110">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="62cc6-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="62cc6-111">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#7](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideDocComments/CS/DocComments.cs#7)]  
  
## <a name="see-also"></a><span data-ttu-id="62cc6-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="62cc6-112">See also</span></span>

- [<span data-ttu-id="62cc6-113">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="62cc6-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="62cc6-114">Balises recommandées pour les commentaires de documentation</span><span class="sxs-lookup"><span data-stu-id="62cc6-114">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
