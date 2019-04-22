---
title: <returns> (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- returns XML tag
- <returns> XML tag
ms.assetid: a03a6469-d907-425d-882f-083187950e7e
ms.openlocfilehash: 5a0ff0da7cf26a1cea75a5b2e4678593d9b72f54
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58827161"
---
# <a name="returns-visual-basic"></a><span data-ttu-id="04217-102">\<Retourne > (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="04217-102">\<returns> (Visual Basic)</span></span>
<span data-ttu-id="04217-103">Spécifie la valeur de retour de la propriété ou la fonction.</span><span class="sxs-lookup"><span data-stu-id="04217-103">Specifies the return value of the property or function.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="04217-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="04217-104">Syntax</span></span>  
  
```xml  
<returns>description</returns>  
```  
  
## <a name="parameters"></a><span data-ttu-id="04217-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="04217-105">Parameters</span></span>  
 `description`  
 <span data-ttu-id="04217-106">Description de la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="04217-106">A description of the return value.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="04217-107">Notes</span><span class="sxs-lookup"><span data-stu-id="04217-107">Remarks</span></span>  
 <span data-ttu-id="04217-108">Utilisez le `<returns>` balise dans le commentaire pour une déclaration de méthode décrire la valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="04217-108">Use the `<returns>` tag in the comment for a method declaration to describe the return value.</span></span>  
  
 <span data-ttu-id="04217-109">Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="04217-109">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="04217-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="04217-110">Example</span></span>  
 <span data-ttu-id="04217-111">Cet exemple utilise le `<returns>` balise à expliquer en quoi le `DoesRecordExist` fonction renvoie.</span><span class="sxs-lookup"><span data-stu-id="04217-111">This example uses the `<returns>` tag to explain what the `DoesRecordExist` function returns.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#6)]  
  
## <a name="see-also"></a><span data-ttu-id="04217-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="04217-112">See also</span></span>

- [<span data-ttu-id="04217-113">Étiquettes XML pour les commentaires</span><span class="sxs-lookup"><span data-stu-id="04217-113">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
