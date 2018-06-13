---
title: '&lt;value&gt; (Guide de programmation C#)'
ms.date: 07/20/2015
f1_keywords:
- <value>
helpviewer_keywords:
- <value> C# XML tag
- value C# XML tag
ms.assetid: 08dbadaf-9ab6-43d9-9493-98e43bed199a
ms.openlocfilehash: 22de15560d6db6e8a70cea744dd9d85359336306
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33356429"
---
# <a name="ltvaluegt-c-programming-guide"></a><span data-ttu-id="6b023-102">&lt;value&gt; (Guide de programmation C#)</span><span class="sxs-lookup"><span data-stu-id="6b023-102">&lt;value&gt; (C# Programming Guide)</span></span>
## <a name="syntax"></a><span data-ttu-id="6b023-103">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6b023-103">Syntax</span></span>  
  
```xml  
<value>property-description</value>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="6b023-104">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6b023-104">Parameters</span></span>  
 `property-description`  
 <span data-ttu-id="6b023-105">Description de la propriété.</span><span class="sxs-lookup"><span data-stu-id="6b023-105">A description for the property.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="6b023-106">Notes</span><span class="sxs-lookup"><span data-stu-id="6b023-106">Remarks</span></span>  
 <span data-ttu-id="6b023-107">La balise \<value> vous permet de décrire la valeur représentée par une propriété.</span><span class="sxs-lookup"><span data-stu-id="6b023-107">The \<value> tag lets you describe the value that a property represents.</span></span> <span data-ttu-id="6b023-108">Notez que lorsque vous ajoutez une propriété via l’Assistant Code de l’environnement de développement Visual Studio .NET, il ajoute une balise [\<summary>](../../../csharp/programming-guide/xmldoc/summary.md) pour la nouvelle propriété.</span><span class="sxs-lookup"><span data-stu-id="6b023-108">Note that when you add a property via code wizard in the Visual Studio .NET development environment, it will add a [\<summary>](../../../csharp/programming-guide/xmldoc/summary.md) tag for the new property.</span></span> <span data-ttu-id="6b023-109">Vous devez ensuite ajouter manuellement une balise \<value> pour décrire la valeur représentée par la propriété.</span><span class="sxs-lookup"><span data-stu-id="6b023-109">You should then manually add a \<value> tag to describe the value that the property represents.</span></span>  
  
 <span data-ttu-id="6b023-110">Compilez avec [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="6b023-110">Compile with [/doc](../../../csharp/language-reference/compiler-options/doc-compiler-option.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6b023-111">Exemple</span><span class="sxs-lookup"><span data-stu-id="6b023-111">Example</span></span>  
 [!code-csharp[csProgGuideDocComments#14](../../../csharp/programming-guide/xmldoc/codesnippet/CSharp/value_1.cs)]  
  
## <a name="see-also"></a><span data-ttu-id="6b023-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b023-112">See Also</span></span>  
 [<span data-ttu-id="6b023-113">Guide de programmation C#</span><span class="sxs-lookup"><span data-stu-id="6b023-113">C# Programming Guide</span></span>](../../../csharp/programming-guide/index.md)  
 [<span data-ttu-id="6b023-114">Balises recommandées pour les commentaires de documentation</span><span class="sxs-lookup"><span data-stu-id="6b023-114">Recommended Tags for Documentation Comments</span></span>](../../../csharp/programming-guide/xmldoc/recommended-tags-for-documentation-comments.md)
