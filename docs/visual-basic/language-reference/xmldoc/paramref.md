---
title: <paramref> (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- paramref XML tag
- <paramref> XML tag
ms.assetid: 8979d53b-beb1-41b7-b41e-6bbea1c17a03
ms.openlocfilehash: 1ef8d76699534a7408912424bcdea651d8314364
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55283983"
---
# <a name="paramref-visual-basic"></a><span data-ttu-id="abc3d-102">\<paramref > (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="abc3d-102">\<paramref> (Visual Basic)</span></span>
<span data-ttu-id="abc3d-103">Met en forme un mot en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="abc3d-103">Formats a word as a parameter.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="abc3d-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="abc3d-104">Syntax</span></span>  
  
```xml  
<paramref name="name"/>  
```  
  
#### <a name="parameters"></a><span data-ttu-id="abc3d-105">Paramètres</span><span class="sxs-lookup"><span data-stu-id="abc3d-105">Parameters</span></span>  
 `name`  
 <span data-ttu-id="abc3d-106">Nom du paramètre auquel faire référence.</span><span class="sxs-lookup"><span data-stu-id="abc3d-106">The name of the parameter to refer to.</span></span> <span data-ttu-id="abc3d-107">Mettez le nom entre guillemets doubles (" ").</span><span class="sxs-lookup"><span data-stu-id="abc3d-107">Enclose the name in double quotation marks (" ").</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="abc3d-108">Notes</span><span class="sxs-lookup"><span data-stu-id="abc3d-108">Remarks</span></span>  
 <span data-ttu-id="abc3d-109">Le `<paramref>` balise vous donne un moyen d’indiquer qu’un mot est un paramètre.</span><span class="sxs-lookup"><span data-stu-id="abc3d-109">The `<paramref>` tag gives you a way to indicate that a word is a parameter.</span></span> <span data-ttu-id="abc3d-110">Le fichier XML peut être traité pour mettre en forme ce paramètre d’une manière distincte.</span><span class="sxs-lookup"><span data-stu-id="abc3d-110">The XML file can be processed to format this parameter in some distinct way.</span></span>  
  
 <span data-ttu-id="abc3d-111">Compilez avec [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) pour placer les commentaires de documentation dans un fichier en vue de les traiter.</span><span class="sxs-lookup"><span data-stu-id="abc3d-111">Compile with [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) to process documentation comments to a file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="abc3d-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="abc3d-112">Example</span></span>  
 <span data-ttu-id="abc3d-113">Cet exemple utilise le `<paramref>` balise pour faire référence à la `id` paramètre.</span><span class="sxs-lookup"><span data-stu-id="abc3d-113">This example uses the `<paramref>` tag to refer to the `id` parameter.</span></span>  
  
 [!code-vb[VbVbcnXmlDocComments#6](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/paramref_1.vb)]  
  
## <a name="see-also"></a><span data-ttu-id="abc3d-114">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="abc3d-114">See also</span></span>
- [<span data-ttu-id="abc3d-115">Étiquettes XML pour les commentaires</span><span class="sxs-lookup"><span data-stu-id="abc3d-115">XML Comment Tags</span></span>](../../../visual-basic/language-reference/xmldoc/index.md)
