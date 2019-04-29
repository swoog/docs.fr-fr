---
title: <remarks> (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- <remarks> XML tag
- remarks XML tag
ms.assetid: c6241773-a7ed-41c9-9a8b-9722a0c606a9
ms.openlocfilehash: c5c088472ae09a416953d9c0829cad1cb48646b8
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61940814"
---
# <a name="remarks-visual-basic"></a><span data-ttu-id="47d88-102">\<remarks > (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="47d88-102">\<remarks> (Visual Basic)</span></span>
<span data-ttu-id="47d88-103">Spécifie une section Notes pour le membre.</span><span class="sxs-lookup"><span data-stu-id="47d88-103">Specifies a remarks section for the member.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="47d88-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="47d88-104">Syntax</span></span>  
  
```xml  
<remarks>description</remarks>  
```  
  
## <a name="parameters"></a><span data-ttu-id="47d88-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="47d88-105">Parameters</span></span>  
 `description`  
 <span data-ttu-id="47d88-106">Description du membre.</span><span class="sxs-lookup"><span data-stu-id="47d88-106">A description of the member.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="47d88-107">Notes</span><span class="sxs-lookup"><span data-stu-id="47d88-107">Remarks</span></span>  
 <span data-ttu-id="47d88-108">Utilisez le `<remarks>` balise à ajouter des informations sur un type et de compléter les informations spécifiées avec [ \<Résumé >](../../../visual-basic/language-reference/xmldoc/summary.md).</span><span class="sxs-lookup"><span data-stu-id="47d88-108">Use the `<remarks>` tag to add information about a type, supplementing the information specified with [\<summary>](../../../visual-basic/language-reference/xmldoc/summary.md).</span></span>  
  
 <span data-ttu-id="47d88-109">Ces informations s’affichent dans l’Explorateur d’objets.</span><span class="sxs-lookup"><span data-stu-id="47d88-109">This information appears in the Object Browser.</span></span> <span data-ttu-id="47d88-110">Pour plus d’informations sur l’Explorateur d’objets, consultez [affichage de la Structure du Code](/visualstudio/ide/viewing-the-structure-of-code).</span><span class="sxs-lookup"><span data-stu-id="47d88-110">For information about the Object Browser, see [Viewing the Structure of Code](/visualstudio/ide/viewing-the-structure-of-code).</span></span>  
  
 <span data-ttu-id="47d88-111">Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="47d88-111">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="47d88-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="47d88-112">Example</span></span>  
 <span data-ttu-id="47d88-113">Cet exemple utilise le `<remarks>` balise à expliquer en quoi le `UpdateRecord` méthode effectue.</span><span class="sxs-lookup"><span data-stu-id="47d88-113">This example uses the `<remarks>` tag to explain what the `UpdateRecord` method does.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#6](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnXmlDocComments/VB/Class1.vb#6)]  
  
## <a name="see-also"></a><span data-ttu-id="47d88-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="47d88-114">See also</span></span>

- [<span data-ttu-id="47d88-115">Étiquettes XML pour les commentaires</span><span class="sxs-lookup"><span data-stu-id="47d88-115">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
