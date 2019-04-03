---
title: <summary> (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- <summary> XML tag
- summary XML tag
ms.assetid: 861c847d-dd94-478a-aa23-bf4899cdc848
ms.openlocfilehash: 0fbe07884f55b7e6f460929e54520de5f718e1af
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58815002"
---
# <a name="summary-visual-basic"></a><span data-ttu-id="01d4f-102">\<Résumé > (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="01d4f-102">\<summary> (Visual Basic)</span></span>
<span data-ttu-id="01d4f-103">Spécifie le résumé du membre.</span><span class="sxs-lookup"><span data-stu-id="01d4f-103">Specifies the summary of the member.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="01d4f-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01d4f-104">Syntax</span></span>  
  
```xml  
<summary>description</summary>  
```  
  
## <a name="parameters"></a><span data-ttu-id="01d4f-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01d4f-105">Parameters</span></span>  
 `description`  
 <span data-ttu-id="01d4f-106">Résumé de l’objet.</span><span class="sxs-lookup"><span data-stu-id="01d4f-106">A summary of the object.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="01d4f-107">Notes</span><span class="sxs-lookup"><span data-stu-id="01d4f-107">Remarks</span></span>  
 <span data-ttu-id="01d4f-108">Utilisez le `<summary>` balise pour décrire un type ou un membre de type.</span><span class="sxs-lookup"><span data-stu-id="01d4f-108">Use the `<summary>` tag to describe a type or a type member.</span></span> <span data-ttu-id="01d4f-109">Utilisez [\<remarks>](../../../visual-basic/language-reference/xmldoc/remarks.md) pour ajouter des informations supplémentaires à une description de type.</span><span class="sxs-lookup"><span data-stu-id="01d4f-109">Use [\<remarks>](../../../visual-basic/language-reference/xmldoc/remarks.md) to add supplemental information to a type description.</span></span>  
  
 <span data-ttu-id="01d4f-110">Le texte pour le `<summary>` balise est la seule source d’informations sur le type dans IntelliSense et s’affiche également dans l’Explorateur d’objets.</span><span class="sxs-lookup"><span data-stu-id="01d4f-110">The text for the `<summary>` tag is the only source of information about the type in IntelliSense, and is also displayed in the Object Browser.</span></span> <span data-ttu-id="01d4f-111">Pour plus d’informations sur l’Explorateur d’objets, consultez [affichage de la Structure du Code](/visualstudio/ide/viewing-the-structure-of-code).</span><span class="sxs-lookup"><span data-stu-id="01d4f-111">For information about the Object Browser, see [Viewing the Structure of Code](/visualstudio/ide/viewing-the-structure-of-code).</span></span>  
  
 <span data-ttu-id="01d4f-112">Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="01d4f-112">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="01d4f-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="01d4f-113">Example</span></span>  
 <span data-ttu-id="01d4f-114">Cet exemple utilise le `<summary>` balises pour décrire le `ResetCounter` méthode et `Counter` propriété.</span><span class="sxs-lookup"><span data-stu-id="01d4f-114">This example uses the `<summary>` tag to describe the `ResetCounter` method and `Counter` property.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="01d4f-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="01d4f-115">See also</span></span>

- [<span data-ttu-id="01d4f-116">Étiquettes XML pour les commentaires</span><span class="sxs-lookup"><span data-stu-id="01d4f-116">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
