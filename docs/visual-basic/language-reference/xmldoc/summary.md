---
title: '&lt;Résumé&gt; (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- <summary> XML tag
- summary XML tag
ms.assetid: 861c847d-dd94-478a-aa23-bf4899cdc848
ms.openlocfilehash: cf320b61a2ca1c54b22e3c3d31ae51d003366efd
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33602647"
---
# <a name="ltsummarygt-visual-basic"></a><span data-ttu-id="79485-102">&lt;Résumé&gt; (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="79485-102">&lt;summary&gt; (Visual Basic)</span></span>
<span data-ttu-id="79485-103">Spécifie le résumé du membre.</span><span class="sxs-lookup"><span data-stu-id="79485-103">Specifies the summary of the member.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="79485-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79485-104">Syntax</span></span>  
  
```xml  
<summary>description</summary>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="79485-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79485-105">Parameters</span></span>  
 `description`  
 <span data-ttu-id="79485-106">Résumé de l’objet.</span><span class="sxs-lookup"><span data-stu-id="79485-106">A summary of the object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="79485-107">Notes</span><span class="sxs-lookup"><span data-stu-id="79485-107">Remarks</span></span>  
 <span data-ttu-id="79485-108">Utilisez le `<summary>` balises pour décrire un type ou un membre de type.</span><span class="sxs-lookup"><span data-stu-id="79485-108">Use the `<summary>` tag to describe a type or a type member.</span></span> <span data-ttu-id="79485-109">Utilisez [\<remarks>](../../../visual-basic/language-reference/xmldoc/remarks.md) pour ajouter des informations supplémentaires à une description de type.</span><span class="sxs-lookup"><span data-stu-id="79485-109">Use [\<remarks>](../../../visual-basic/language-reference/xmldoc/remarks.md) to add supplemental information to a type description.</span></span>  
  
 <span data-ttu-id="79485-110">Le texte de la `<summary>` balise est la seule source d’informations sur le type dans IntelliSense et s’affiche également dans l’Explorateur d’objets.</span><span class="sxs-lookup"><span data-stu-id="79485-110">The text for the `<summary>` tag is the only source of information about the type in IntelliSense, and is also displayed in the Object Browser.</span></span> <span data-ttu-id="79485-111">Pour plus d’informations sur l’Explorateur d’objets, consultez [affichage de la Structure du Code](/visualstudio/ide/viewing-the-structure-of-code).</span><span class="sxs-lookup"><span data-stu-id="79485-111">For information about the Object Browser, see [Viewing the Structure of Code](/visualstudio/ide/viewing-the-structure-of-code).</span></span>  
  
 <span data-ttu-id="79485-112">Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="79485-112">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="79485-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="79485-113">Example</span></span>  
 <span data-ttu-id="79485-114">Cet exemple utilise le `<summary>` balises pour décrire le `ResetCounter` méthode et `Counter` propriété.</span><span class="sxs-lookup"><span data-stu-id="79485-114">This example uses the `<summary>` tag to describe the `ResetCounter` method and `Counter` property.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#1](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/summary_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="79485-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79485-115">See Also</span></span>  
 [<span data-ttu-id="79485-116">Étiquettes XML pour les commentaires</span><span class="sxs-lookup"><span data-stu-id="79485-116">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md)
