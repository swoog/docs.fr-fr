---
title: '&lt;typeparam&gt; (Guide de programmation C#)'
ms.date: 07/20/2015
f1_keywords:
- typeparam
helpviewer_keywords:
- <typeparam> C# XML tag
- typeparam C# XML tag
ms.assetid: 9b99d400-e911-4e55-99c6-64367c96aa4f
ms.openlocfilehash: ec19060008c1c06c54c89dbddee7d24001bcdebc
ms.sourcegitcommit: 6eac9a01ff5d70c6d18460324c016a3612c5e268
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45677745"
---
# <a name="lttypeparamgt-c-programming-guide"></a><span data-ttu-id="ad5a9-102">&lt;typeparam&gt; (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="ad5a9-102">&lt;typeparam&gt; (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="ad5a9-103">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ad5a9-103">Syntax</span></span>  
  
```xml  
<typeparam name="name">description</typeparam>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="ad5a9-104">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ad5a9-104">Parameters</span></span>  
 `name`  
 <span data-ttu-id="ad5a9-105">Nom du paramètre de type.</span><span class="sxs-lookup"><span data-stu-id="ad5a9-105">The name of the type parameter.</span></span> <span data-ttu-id="ad5a9-106">Mettez le nom entre guillemets doubles (" ").</span><span class="sxs-lookup"><span data-stu-id="ad5a9-106">Enclose the name in double quotation marks (" ").</span></span>  
  
 `description`  
 <span data-ttu-id="ad5a9-107">Description du paramètre de type.</span><span class="sxs-lookup"><span data-stu-id="ad5a9-107">A description for the type parameter.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ad5a9-108">Notes</span><span class="sxs-lookup"><span data-stu-id="ad5a9-108">Remarks</span></span>  
 <span data-ttu-id="ad5a9-109">La balise `<typeparam>` doit être utilisée dans le commentaire d’une déclaration de méthode ou de type générique pour décrire un paramètre de type.</span><span class="sxs-lookup"><span data-stu-id="ad5a9-109">The `<typeparam>` tag should be used in the comment for a generic type or method declaration to describe a type parameter.</span></span> <span data-ttu-id="ad5a9-110">Ajoutez une balise pour chaque paramètre de type de la méthode et du type générique.</span><span class="sxs-lookup"><span data-stu-id="ad5a9-110">Add a tag for each type parameter of the generic type or method.</span></span>  
  
 <span data-ttu-id="ad5a9-111">Pour plus d’informations, consultez la page [Génériques](../../../csharp/programming-guide/generics/index.md).</span><span class="sxs-lookup"><span data-stu-id="ad5a9-111">For more information, see [Generics](../../../csharp/programming-guide/generics/index.md).</span></span>  
  
 <span data-ttu-id="ad5a9-112">Le texte de la balise `<typeparam>` s’affiche dans IntelliSense, dans la [fenêtre Explorateur d’objets](https://msdn.microsoft.com/library/3c7f1673-1f0d-41b1-94ca-a3dcfcb82cda) et dans le rapport web de commentaire de code.</span><span class="sxs-lookup"><span data-stu-id="ad5a9-112">The text for the `<typeparam>` tag will be displayed in IntelliSense, the [Object Browser Window](https://msdn.microsoft.com/library/3c7f1673-1f0d-41b1-94ca-a3dcfcb82cda) code comment web report.</span></span>  
  
 <span data-ttu-id="ad5a9-113">Compilez avec [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="ad5a9-113">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ad5a9-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="ad5a9-114">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#13](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/typeparam_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="ad5a9-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ad5a9-115">See Also</span></span>

- [<span data-ttu-id="ad5a9-116">Référence C#</span><span class="sxs-lookup"><span data-stu-id="ad5a9-116">C# Reference</span></span>](../../../csharp/language-reference/index.md)  
- [<span data-ttu-id="ad5a9-117">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="ad5a9-117">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="ad5a9-118">Balises recommandées pour les commentaires de documentation</span><span class="sxs-lookup"><span data-stu-id="ad5a9-118">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
