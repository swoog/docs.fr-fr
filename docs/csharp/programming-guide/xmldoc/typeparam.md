---
title: '&lt;typeparam&gt; - Guide de programmation C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- typeparam
helpviewer_keywords:
- <typeparam> C# XML tag
- typeparam C# XML tag
ms.assetid: 9b99d400-e911-4e55-99c6-64367c96aa4f
ms.openlocfilehash: 21819bebbb304eaace3950f40b97033762cd6ce8
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54568047"
---
# <a name="lttypeparamgt-c-programming-guide"></a><span data-ttu-id="d8338-102">&lt;typeparam&gt; (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="d8338-102">&lt;typeparam&gt; (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="d8338-103">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8338-103">Syntax</span></span>  
  
```xml  
<typeparam name="name">description</typeparam>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d8338-104">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8338-104">Parameters</span></span>  
 `name`  
 <span data-ttu-id="d8338-105">Nom du paramètre de type.</span><span class="sxs-lookup"><span data-stu-id="d8338-105">The name of the type parameter.</span></span> <span data-ttu-id="d8338-106">Mettez le nom entre guillemets doubles (" ").</span><span class="sxs-lookup"><span data-stu-id="d8338-106">Enclose the name in double quotation marks (" ").</span></span>  
  
 `description`  
 <span data-ttu-id="d8338-107">Description du paramètre de type.</span><span class="sxs-lookup"><span data-stu-id="d8338-107">A description for the type parameter.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d8338-108">Notes</span><span class="sxs-lookup"><span data-stu-id="d8338-108">Remarks</span></span>  
 <span data-ttu-id="d8338-109">La balise `<typeparam>` doit être utilisée dans le commentaire d’une déclaration de méthode ou de type générique pour décrire un paramètre de type.</span><span class="sxs-lookup"><span data-stu-id="d8338-109">The `<typeparam>` tag should be used in the comment for a generic type or method declaration to describe a type parameter.</span></span> <span data-ttu-id="d8338-110">Ajoutez une balise pour chaque paramètre de type de la méthode et du type générique.</span><span class="sxs-lookup"><span data-stu-id="d8338-110">Add a tag for each type parameter of the generic type or method.</span></span>  
  
 <span data-ttu-id="d8338-111">Pour plus d’informations, consultez la page [Génériques](../../../csharp/programming-guide/generics/index.md).</span><span class="sxs-lookup"><span data-stu-id="d8338-111">For more information, see [Generics](../../../csharp/programming-guide/generics/index.md).</span></span>  
  
 <span data-ttu-id="d8338-112">Le texte de la balise `<typeparam>` s’affiche dans IntelliSense, dans la [fenêtre Explorateur d’objets](/visualstudio/ide/viewing-the-structure-of-code#BKMK_ObjectBrowser) et dans le rapport web de commentaire de code.</span><span class="sxs-lookup"><span data-stu-id="d8338-112">The text for the `<typeparam>` tag will be displayed in IntelliSense, the [Object Browser Window](/visualstudio/ide/viewing-the-structure-of-code#BKMK_ObjectBrowser) code comment web report.</span></span>  
  
 <span data-ttu-id="d8338-113">Compilez avec [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="d8338-113">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d8338-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="d8338-114">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#13](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/typeparam_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="d8338-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8338-115">See also</span></span>

- [<span data-ttu-id="d8338-116">Référence C#</span><span class="sxs-lookup"><span data-stu-id="d8338-116">C# Reference</span></span>](../../../csharp/language-reference/index.md)
- [<span data-ttu-id="d8338-117">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="d8338-117">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="d8338-118">Balises recommandées pour les commentaires de documentation</span><span class="sxs-lookup"><span data-stu-id="d8338-118">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
