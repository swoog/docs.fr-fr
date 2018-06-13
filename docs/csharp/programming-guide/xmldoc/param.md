---
title: '&lt;param&gt; (Guide de programmation C#)'
ms.date: 07/20/2015
f1_keywords:
- param
- <param>
helpviewer_keywords:
- <param> C# XML tag
- param C# XML tag
ms.assetid: 46d329b1-5b84-4537-9e17-73ca97313e4e
ms.openlocfilehash: 3d89637e5b1238c582390750e8eef30960fa90b6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33338011"
---
# <a name="ltparamgt-c-programming-guide"></a><span data-ttu-id="0c753-102">&lt;param&gt; (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="0c753-102">&lt;param&gt; (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="0c753-103">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c753-103">Syntax</span></span>  
  
```xml  
<param name="name">description</param>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="0c753-104">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0c753-104">Parameters</span></span>  
 `name`  
 <span data-ttu-id="0c753-105">Nom d’un paramètre de méthode.</span><span class="sxs-lookup"><span data-stu-id="0c753-105">The name of a method parameter.</span></span> <span data-ttu-id="0c753-106">Mettez le nom entre guillemets doubles (" ").</span><span class="sxs-lookup"><span data-stu-id="0c753-106">Enclose the name in double quotation marks (" ").</span></span>  
  
 `description`  
 <span data-ttu-id="0c753-107">Description du paramètre.</span><span class="sxs-lookup"><span data-stu-id="0c753-107">A description for the parameter.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="0c753-108">Notes</span><span class="sxs-lookup"><span data-stu-id="0c753-108">Remarks</span></span>  
 <span data-ttu-id="0c753-109">La balise \<param> doit être utilisée dans le commentaire de la déclaration d’une méthode pour décrire l’un des paramètres de la méthode.</span><span class="sxs-lookup"><span data-stu-id="0c753-109">The \<param> tag should be used in the comment for a method declaration to describe one of the parameters for the method.</span></span> <span data-ttu-id="0c753-110">Pour documenter plusieurs paramètres, utilisez plusieurs balises \<param>.</span><span class="sxs-lookup"><span data-stu-id="0c753-110">To document multiple parameters, use multiple \<param> tags.</span></span>  
  
 <span data-ttu-id="0c753-111">Le texte de la balise \<param> s’affiche dans IntelliSense, dans l’Explorateur d’objets et dans le rapport web de commentaire de code.</span><span class="sxs-lookup"><span data-stu-id="0c753-111">The text for the \<param> tag will be displayed in IntelliSense, the Object Browser, and in the Code Comment Web Report.</span></span>  
  
 <span data-ttu-id="0c753-112">Compilez avec [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="0c753-112">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0c753-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="0c753-113">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#1](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/param_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="0c753-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c753-114">See Also</span></span>  
 [<span data-ttu-id="0c753-115">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="0c753-115">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="0c753-116">Balises recommandées pour les commentaires de documentation</span><span class="sxs-lookup"><span data-stu-id="0c753-116">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
