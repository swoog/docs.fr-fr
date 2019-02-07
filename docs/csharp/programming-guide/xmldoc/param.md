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
ms.openlocfilehash: 3f1099da6a43ed7f48389a16e3be6a3b6b98a148
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55271575"
---
# <a name="param-c-programming-guide"></a><span data-ttu-id="1db53-102">\<param> (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="1db53-102">\<param> (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="1db53-103">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1db53-103">Syntax</span></span>  
  
```xml  
<param name="name">description</param>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="1db53-104">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1db53-104">Parameters</span></span>  
 `name`  
 <span data-ttu-id="1db53-105">Nom d’un paramètre de méthode.</span><span class="sxs-lookup"><span data-stu-id="1db53-105">The name of a method parameter.</span></span> <span data-ttu-id="1db53-106">Mettez le nom entre guillemets doubles (" ").</span><span class="sxs-lookup"><span data-stu-id="1db53-106">Enclose the name in double quotation marks (" ").</span></span>  
  
 `description`  
 <span data-ttu-id="1db53-107">Description du paramètre.</span><span class="sxs-lookup"><span data-stu-id="1db53-107">A description for the parameter.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="1db53-108">Notes</span><span class="sxs-lookup"><span data-stu-id="1db53-108">Remarks</span></span>  
 <span data-ttu-id="1db53-109">La balise \<param> doit être utilisée dans le commentaire de la déclaration d’une méthode pour décrire l’un des paramètres de la méthode.</span><span class="sxs-lookup"><span data-stu-id="1db53-109">The \<param> tag should be used in the comment for a method declaration to describe one of the parameters for the method.</span></span> <span data-ttu-id="1db53-110">Pour documenter plusieurs paramètres, utilisez plusieurs balises \<param>.</span><span class="sxs-lookup"><span data-stu-id="1db53-110">To document multiple parameters, use multiple \<param> tags.</span></span>  
  
 <span data-ttu-id="1db53-111">Le texte de la balise \<param> s’affiche dans IntelliSense, dans l’Explorateur d’objets et dans le rapport web de commentaire de code.</span><span class="sxs-lookup"><span data-stu-id="1db53-111">The text for the \<param> tag will be displayed in IntelliSense, the Object Browser, and in the Code Comment Web Report.</span></span>  
  
 <span data-ttu-id="1db53-112">Compilez avec [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="1db53-112">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1db53-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="1db53-113">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#1](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/param_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="1db53-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1db53-114">See also</span></span>

- [<span data-ttu-id="1db53-115">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="1db53-115">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)
- [<span data-ttu-id="1db53-116">Balises recommandées pour les commentaires de documentation</span><span class="sxs-lookup"><span data-stu-id="1db53-116">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
