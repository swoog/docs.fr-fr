---
title: <param> - Guide de programmation C#
ms.custom: seodec18
ms.date: 07/20/2015
f1_keywords:
- param
- <param>
helpviewer_keywords:
- <param> C# XML tag
- param C# XML tag
ms.assetid: 46d329b1-5b84-4537-9e17-73ca97313e4e
ms.openlocfilehash: ffa3bd066ce753f2b953f2d6d0a70a3bf65293ff
ms.sourcegitcommit: 5137208fa414d9ca3c58cdfd2155ac81bc89e917
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/06/2019
ms.locfileid: "57468030"
---
# <a name="param-c-programming-guide"></a><span data-ttu-id="ec066-102">\<param> (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="ec066-102">\<param> (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="ec066-103">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec066-103">Syntax</span></span>  
  
```xml  
<param name="name">description</param>  
```  
  
## <a name="parameters"></a><span data-ttu-id="ec066-104">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ec066-104">Parameters</span></span>  
 `name`  
 <span data-ttu-id="ec066-105">Nom d’un paramètre de méthode.</span><span class="sxs-lookup"><span data-stu-id="ec066-105">The name of a method parameter.</span></span> <span data-ttu-id="ec066-106">Mettez le nom entre guillemets doubles (" ").</span><span class="sxs-lookup"><span data-stu-id="ec066-106">Enclose the name in double quotation marks (" ").</span></span>  
  
 `description`  
 <span data-ttu-id="ec066-107">Description du paramètre.</span><span class="sxs-lookup"><span data-stu-id="ec066-107">A description for the parameter.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="ec066-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="ec066-108">Remarks</span></span>  
 <span data-ttu-id="ec066-109">La balise \<param> doit être utilisée dans le commentaire de la déclaration d’une méthode pour décrire l’un des paramètres de la méthode.</span><span class="sxs-lookup"><span data-stu-id="ec066-109">The \<param> tag should be used in the comment for a method declaration to describe one of the parameters for the method.</span></span> <span data-ttu-id="ec066-110">Pour documenter plusieurs paramètres, utilisez plusieurs balises \<param>.</span><span class="sxs-lookup"><span data-stu-id="ec066-110">To document multiple parameters, use multiple \<param> tags.</span></span>  
  
 <span data-ttu-id="ec066-111">Le texte de la balise \<param> s’affiche dans IntelliSense, dans l’Explorateur d’objets et dans le rapport web de commentaire de code.</span><span class="sxs-lookup"><span data-stu-id="ec066-111">The text for the \<param> tag will be displayed in IntelliSense, the Object Browser, and in the Code Comment Web Report.</span></span>  
  
 <span data-ttu-id="ec066-112">Compilez avec [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="ec066-112">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ec066-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="ec066-113">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#1](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csProgGuideDocComments/CS/DocComments.cs#1)]  
  
## <a name="see-also"></a><span data-ttu-id="ec066-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ec066-114">See also</span></span>

- [<span data-ttu-id="ec066-115">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="ec066-115">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="ec066-116">Balises recommandées pour les commentaires de documentation</span><span class="sxs-lookup"><span data-stu-id="ec066-116">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
