---
title: <exception> - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- exception
- <exception>
helpviewer_keywords:
- <exception> C# XML tag
- exception C# XML tag
ms.assetid: dd73aac5-3c74-4fcf-9498-f11bff3a2f3c
ms.openlocfilehash: 4036b53674eb680c2df3136e8dd6d8165514dbb8
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57487697"
---
# <a name="exception-c-programming-guide"></a><span data-ttu-id="cb666-102">\<exception> (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="cb666-102">\<exception> (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="cb666-103">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cb666-103">Syntax</span></span>  
  
```xml  
<exception cref="member">description</exception>  
```  
  
## <a name="parameters"></a><span data-ttu-id="cb666-104">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cb666-104">Parameters</span></span>  
 <span data-ttu-id="cb666-105">cref = " `member`"</span><span class="sxs-lookup"><span data-stu-id="cb666-105">cref = " `member`"</span></span>  
 <span data-ttu-id="cb666-106">Référence à une exception qui est disponible à partir de l’environnement de compilation actuel.</span><span class="sxs-lookup"><span data-stu-id="cb666-106">A reference to an exception that is available from the current compilation environment.</span></span> <span data-ttu-id="cb666-107">Le compilateur vérifie que l’exception donnée existe, et il traduit `member` en nom d’élément canonique dans le fichier XML de sortie.</span><span class="sxs-lookup"><span data-stu-id="cb666-107">The compiler checks that the given exception exists and translates `member` to the canonical element name in the output XML.</span></span> <span data-ttu-id="cb666-108">`member` doit apparaître entre guillemets doubles (" ").</span><span class="sxs-lookup"><span data-stu-id="cb666-108">`member` must appear within double quotation marks (" ").</span></span>  
  
 <span data-ttu-id="cb666-109">Pour plus d’informations sur la façon de créer une référence cref à un type générique, consultez [\<see>](../../../csharp/programming-guide/xmldoc/see.md).</span><span class="sxs-lookup"><span data-stu-id="cb666-109">For more information on how to create a cref reference to a generic type, see [\<see>](../../../csharp/programming-guide/xmldoc/see.md).</span></span>  
  
 `description`  
 <span data-ttu-id="cb666-110">Description de l'exception.</span><span class="sxs-lookup"><span data-stu-id="cb666-110">A description of the exception.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cb666-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="cb666-111">Remarks</span></span>  
 <span data-ttu-id="cb666-112">La balise \<exception> vous permet de spécifier quelles exceptions peuvent être levées.</span><span class="sxs-lookup"><span data-stu-id="cb666-112">The \<exception> tag lets you specify which exceptions can be thrown.</span></span> <span data-ttu-id="cb666-113">Cette balise peut être appliquée à des définitions de méthodes, de propriétés, d’événements et d’indexeurs.</span><span class="sxs-lookup"><span data-stu-id="cb666-113">This tag can be applied to definitions for methods, properties, events, and indexers.</span></span>  
  
 <span data-ttu-id="cb666-114">Compilez avec [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) pour traiter les commentaires de documentation dans un fichier.</span><span class="sxs-lookup"><span data-stu-id="cb666-114">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
 <span data-ttu-id="cb666-115">Pour plus d’informations sur la gestion des exceptions, consultez [Exceptions et gestion des exceptions](../../../csharp/programming-guide/exceptions/index.md).</span><span class="sxs-lookup"><span data-stu-id="cb666-115">For more information about exception handling, see [Exceptions and Exception Handling](../../../csharp/programming-guide/exceptions/index.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="cb666-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="cb666-116">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#4](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideDocComments/CS/DocComments.cs#4)]  
  
## <a name="see-also"></a><span data-ttu-id="cb666-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb666-117">See also</span></span>

- [<span data-ttu-id="cb666-118">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="cb666-118">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="cb666-119">Balises recommandées pour les commentaires de documentation</span><span class="sxs-lookup"><span data-stu-id="cb666-119">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
