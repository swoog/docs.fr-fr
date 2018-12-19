---
title: '&lt;typeparamref&gt; - Guide de programmation C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- typeparamref
helpviewer_keywords:
- typeparamref C# XML tag
- <typeparamref> C# XML tag
ms.assetid: 6d8ffc58-12c5-4688-8db6-833a7ded5886
ms.openlocfilehash: bbe9bed5a32e463424b98f4066e95374401931e2
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53243918"
---
# <a name="lttypeparamrefgt-c-programming-guide"></a><span data-ttu-id="96339-102">&lt;typeparamref&gt; (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="96339-102">&lt;typeparamref&gt; (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="96339-103">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="96339-103">Syntax</span></span>  
  
```xml  
<typeparamref name="name"/>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="96339-104">Paramètres</span><span class="sxs-lookup"><span data-stu-id="96339-104">Parameters</span></span>  
 `name`  
 <span data-ttu-id="96339-105">Nom du paramètre de type.</span><span class="sxs-lookup"><span data-stu-id="96339-105">The name of the type parameter.</span></span> <span data-ttu-id="96339-106">Mettez le nom entre guillemets doubles (" ").</span><span class="sxs-lookup"><span data-stu-id="96339-106">Enclose the name in double quotation marks (" ").</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="96339-107">Notes</span><span class="sxs-lookup"><span data-stu-id="96339-107">Remarks</span></span>  
 <span data-ttu-id="96339-108">Pour plus d’informations sur les paramètres de type dans les types et méthodes génériques, consultez [Génériques](../../../csharp/programming-guide/generics/index.md).</span><span class="sxs-lookup"><span data-stu-id="96339-108">For more information on type parameters in generic types and methods, see [Generics](../../../csharp/programming-guide/generics/index.md).</span></span>  
  
 <span data-ttu-id="96339-109">Utilisez cette balise pour permettre aux consommateurs du fichier de documentation d’appliquer une mise en forme particulière au mot, par exemple l’italique.</span><span class="sxs-lookup"><span data-stu-id="96339-109">Use this tag to enable consumers of the documentation file to format the word in some distinct way, for example in italics.</span></span>  
  
 <span data-ttu-id="96339-110">Compilez avec [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="96339-110">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="96339-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="96339-111">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#13](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/typeparamref_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="96339-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="96339-112">See Also</span></span>

- [<span data-ttu-id="96339-113">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="96339-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="96339-114">Balises recommandées pour les commentaires de documentation</span><span class="sxs-lookup"><span data-stu-id="96339-114">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
