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
ms.openlocfilehash: cfee16ad1cdc1e019a4133259c1603f5a0a09ac8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54536553"
---
# <a name="lttypeparamrefgt-c-programming-guide"></a><span data-ttu-id="eb283-102">&lt;typeparamref&gt; (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="eb283-102">&lt;typeparamref&gt; (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="eb283-103">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eb283-103">Syntax</span></span>  
  
```xml  
<typeparamref name="name"/>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="eb283-104">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eb283-104">Parameters</span></span>  
 `name`  
 <span data-ttu-id="eb283-105">Nom du paramètre de type.</span><span class="sxs-lookup"><span data-stu-id="eb283-105">The name of the type parameter.</span></span> <span data-ttu-id="eb283-106">Mettez le nom entre guillemets doubles (" ").</span><span class="sxs-lookup"><span data-stu-id="eb283-106">Enclose the name in double quotation marks (" ").</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="eb283-107">Notes</span><span class="sxs-lookup"><span data-stu-id="eb283-107">Remarks</span></span>  
 <span data-ttu-id="eb283-108">Pour plus d’informations sur les paramètres de type dans les types et méthodes génériques, consultez [Génériques](../../../csharp/programming-guide/generics/index.md).</span><span class="sxs-lookup"><span data-stu-id="eb283-108">For more information on type parameters in generic types and methods, see [Generics](../../../csharp/programming-guide/generics/index.md).</span></span>  
  
 <span data-ttu-id="eb283-109">Utilisez cette balise pour permettre aux consommateurs du fichier de documentation d’appliquer une mise en forme particulière au mot, par exemple l’italique.</span><span class="sxs-lookup"><span data-stu-id="eb283-109">Use this tag to enable consumers of the documentation file to format the word in some distinct way, for example in italics.</span></span>  
  
 <span data-ttu-id="eb283-110">Compilez avec [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="eb283-110">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="eb283-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="eb283-111">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#13](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/typeparamref_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="eb283-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eb283-112">See also</span></span>

- [<span data-ttu-id="eb283-113">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="eb283-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="eb283-114">Balises recommandées pour les commentaires de documentation</span><span class="sxs-lookup"><span data-stu-id="eb283-114">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
