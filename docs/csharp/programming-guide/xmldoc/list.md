---
title: '&lt;list&gt; - Guide de programmation C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- list
- <list>
helpviewer_keywords:
- list C# XML tag
- listheader C# XML tag
- <listheader> C# XML tag
- item C# XML tag
- <item> C# XML tag
- <list> C# XML tag
ms.assetid: c9620b1b-c2e6-43f1-ab88-8ab47308ffec
ms.openlocfilehash: b960349d26a4addb5f4723bd7aa3f19b07e5f4d2
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53241546"
---
# <a name="ltlistgt-c-programming-guide"></a><span data-ttu-id="6bec0-102">&lt;list&gt; (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="6bec0-102">&lt;list&gt; (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="6bec0-103">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6bec0-103">Syntax</span></span>  
  
```xml  
<list type="bullet" | "number" | "table">  
    <listheader>  
        <term>term</term>  
        <description>description</description>  
    </listheader>  
    <item>  
        <term>term</term>  
        <description>description</description>  
    </item>  
</list>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6bec0-104">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6bec0-104">Parameters</span></span>  
 `term`  
 <span data-ttu-id="6bec0-105">Terme à définir, qui est défini dans `description`.</span><span class="sxs-lookup"><span data-stu-id="6bec0-105">A term to define, which will be defined in `description`.</span></span>  
  
 `description`  
 <span data-ttu-id="6bec0-106">Élément contenu dans une puce ou une liste numérotée ou définition d’un `term`.</span><span class="sxs-lookup"><span data-stu-id="6bec0-106">Either an item in a bullet or numbered list or the definition of a `term`.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6bec0-107">Notes</span><span class="sxs-lookup"><span data-stu-id="6bec0-107">Remarks</span></span>  
 <span data-ttu-id="6bec0-108">Le bloc \<listheader> permet de définir la ligne d’en-tête d’une table ou d’une liste de définitions.</span><span class="sxs-lookup"><span data-stu-id="6bec0-108">The \<listheader> block is used to define the heading row of either a table or definition list.</span></span> <span data-ttu-id="6bec0-109">Au moment de définir une table, il vous suffit de fournir une entrée pour le terme figurant dans l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="6bec0-109">When defining a table, you only need to supply an entry for term in the heading.</span></span>  
  
 <span data-ttu-id="6bec0-110">Chaque élément de la liste est spécifié avec un bloc \<item>.</span><span class="sxs-lookup"><span data-stu-id="6bec0-110">Each item in the list is specified with an \<item> block.</span></span> <span data-ttu-id="6bec0-111">Au moment de créer une liste de définitions, vous devez spécifier à la fois `term` et `description`.</span><span class="sxs-lookup"><span data-stu-id="6bec0-111">When creating a definition list, you will need to specify both `term` and `description`.</span></span> <span data-ttu-id="6bec0-112">Cependant, pour une table, une liste à puces ou une liste numérotée, il vous suffit de fournir une entrée pour `description`.</span><span class="sxs-lookup"><span data-stu-id="6bec0-112">However, for a table, bulleted list, or numbered list, you only need to supply an entry for `description`.</span></span>  
  
 <span data-ttu-id="6bec0-113">Une liste ou une table peut comporter autant de blocs \<item> que nécessaire.</span><span class="sxs-lookup"><span data-stu-id="6bec0-113">A list or table can have as many \<item> blocks as needed.</span></span>  
  
 <span data-ttu-id="6bec0-114">Compilez avec [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="6bec0-114">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6bec0-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="6bec0-115">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#6](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/list_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="6bec0-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6bec0-116">See Also</span></span>

- [<span data-ttu-id="6bec0-117">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="6bec0-117">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="6bec0-118">Balises recommandées pour les commentaires de documentation</span><span class="sxs-lookup"><span data-stu-id="6bec0-118">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
