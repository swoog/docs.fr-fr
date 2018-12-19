---
title: '&lt;param&gt; - Guide de programmation C#'
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- param
- <param>
helpviewer_keywords:
- <param> C# XML tag
- param C# XML tag
ms.assetid: 46d329b1-5b84-4537-9e17-73ca97313e4e
ms.openlocfilehash: fca53a3cd5490c28c8fabcf69446fe4a55d60b4e
ms.sourcegitcommit: bdd930b5df20a45c29483d905526a2a3e4d17c5b
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2018
ms.locfileid: "53236958"
---
# <a name="ltparamgt-c-programming-guide"></a><span data-ttu-id="7c70b-102">&lt;param&gt; (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="7c70b-102">&lt;param&gt; (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="7c70b-103">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c70b-103">Syntax</span></span>  
  
```xml  
<param name="name">description</param>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="7c70b-104">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7c70b-104">Parameters</span></span>  
 `name`  
 <span data-ttu-id="7c70b-105">Nom d’un paramètre de méthode.</span><span class="sxs-lookup"><span data-stu-id="7c70b-105">The name of a method parameter.</span></span> <span data-ttu-id="7c70b-106">Mettez le nom entre guillemets doubles (" ").</span><span class="sxs-lookup"><span data-stu-id="7c70b-106">Enclose the name in double quotation marks (" ").</span></span>  
  
 `description`  
 <span data-ttu-id="7c70b-107">Description du paramètre.</span><span class="sxs-lookup"><span data-stu-id="7c70b-107">A description for the parameter.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="7c70b-108">Notes</span><span class="sxs-lookup"><span data-stu-id="7c70b-108">Remarks</span></span>  
 <span data-ttu-id="7c70b-109">La balise \<param> doit être utilisée dans le commentaire de la déclaration d’une méthode pour décrire l’un des paramètres de la méthode.</span><span class="sxs-lookup"><span data-stu-id="7c70b-109">The \<param> tag should be used in the comment for a method declaration to describe one of the parameters for the method.</span></span> <span data-ttu-id="7c70b-110">Pour documenter plusieurs paramètres, utilisez plusieurs balises \<param>.</span><span class="sxs-lookup"><span data-stu-id="7c70b-110">To document multiple parameters, use multiple \<param> tags.</span></span>  
  
 <span data-ttu-id="7c70b-111">Le texte de la balise \<param> s’affiche dans IntelliSense, dans l’Explorateur d’objets et dans le rapport web de commentaire de code.</span><span class="sxs-lookup"><span data-stu-id="7c70b-111">The text for the \<param> tag will be displayed in IntelliSense, the Object Browser, and in the Code Comment Web Report.</span></span>  
  
 <span data-ttu-id="7c70b-112">Compilez avec [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="7c70b-112">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7c70b-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="7c70b-113">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#1](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/param_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="7c70b-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c70b-114">See Also</span></span>

- [<span data-ttu-id="7c70b-115">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="7c70b-115">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
- [<span data-ttu-id="7c70b-116">Balises recommandées pour les commentaires de documentation</span><span class="sxs-lookup"><span data-stu-id="7c70b-116">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
