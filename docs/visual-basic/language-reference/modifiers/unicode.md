---
title: Unicode (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Unicode
helpviewer_keywords:
- Unicode, external references
- Declare statement [Visual Basic], marshaling strings
- Unicode keyword [Visual Basic]
- Unicode, marshaling strings
ms.assetid: 0021d5ff-3209-444e-8497-420f3e6ee075
ms.openlocfilehash: b3c9452f8d144fb18ea3efcb35b85caed80e8692
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61778675"
---
# <a name="unicode-visual-basic"></a><span data-ttu-id="d52b2-102">Unicode (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="d52b2-102">Unicode (Visual Basic)</span></span>
<span data-ttu-id="d52b2-103">Spécifie que Visual Basic doit marshaler toutes les chaînes en valeurs Unicode, quel que soit le nom de la procédure externe déclarée.</span><span class="sxs-lookup"><span data-stu-id="d52b2-103">Specifies that Visual Basic should marshal all strings to Unicode values regardless of the name of the external procedure being declared.</span></span>  
  
 <span data-ttu-id="d52b2-104">Lorsque vous appelez une procédure définie en dehors de votre projet, le compilateur Visual Basic n’a pas accès aux informations qu’il doit avoir pour appeler la procédure correctement.</span><span class="sxs-lookup"><span data-stu-id="d52b2-104">When you call a procedure defined outside your project, the Visual Basic compiler does not have access to the information it must have in order to call the procedure correctly.</span></span> <span data-ttu-id="d52b2-105">Ces informations incluent où se trouve la procédure, comment il est identifié, sa séquence d’appel et de type de retour, et chaîne de jeu de caractères qu’il utilise.</span><span class="sxs-lookup"><span data-stu-id="d52b2-105">This information includes where the procedure is located, how it is identified, its calling sequence and return type, and the string character set it uses.</span></span> <span data-ttu-id="d52b2-106">Le [instruction Declare](../../../visual-basic/language-reference/statements/declare-statement.md) crée une référence à une procédure externe et fournit ces informations nécessaires.</span><span class="sxs-lookup"><span data-stu-id="d52b2-106">The [Declare Statement](../../../visual-basic/language-reference/statements/declare-statement.md) creates a reference to an external procedure and supplies this necessary information.</span></span>  
  
 <span data-ttu-id="d52b2-107">Le `charsetmodifier` dans le `Declare` instruction fournit les informations de jeu de caractères pour marshaler des chaînes lors d’un appel à la procédure externe.</span><span class="sxs-lookup"><span data-stu-id="d52b2-107">The `charsetmodifier` part in the `Declare` statement supplies the character set information to marshal strings during a call to the external procedure.</span></span> <span data-ttu-id="d52b2-108">Elle affecte également la façon dont Visual Basic recherche le fichier externe pour le nom de la procédure externe.</span><span class="sxs-lookup"><span data-stu-id="d52b2-108">It also affects how Visual Basic searches the external file for the external procedure name.</span></span> <span data-ttu-id="d52b2-109">Le `Unicode` modificateur Spécifie que Visual Basic doit marshaler toutes les chaînes en valeurs Unicode et doit rechercher la procédure sans modifier son nom durant la recherche.</span><span class="sxs-lookup"><span data-stu-id="d52b2-109">The `Unicode` modifier specifies that Visual Basic should marshal all strings to Unicode values and should look up the procedure without modifying its name during the search.</span></span>  
  
 <span data-ttu-id="d52b2-110">Si aucun modificateur de jeu de caractères est spécifié, `Ansi` est la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="d52b2-110">If no character set modifier is specified, `Ansi` is the default.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="d52b2-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d52b2-111">Remarks</span></span>  
 <span data-ttu-id="d52b2-112">Le `Unicode` modificateur peut être utilisé dans ce contexte :</span><span class="sxs-lookup"><span data-stu-id="d52b2-112">The `Unicode` modifier can be used in this context:</span></span>  
  
 [<span data-ttu-id="d52b2-113">Declare (instruction)</span><span class="sxs-lookup"><span data-stu-id="d52b2-113">Declare Statement</span></span>](../../../visual-basic/language-reference/statements/declare-statement.md)  
  
## <a name="smart-device-developer-notes"></a><span data-ttu-id="d52b2-114">Remarques sur le développement Smart Device</span><span class="sxs-lookup"><span data-stu-id="d52b2-114">Smart Device Developer Notes</span></span>  
 <span data-ttu-id="d52b2-115">Ce mot clé n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d52b2-115">This keyword is not supported.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d52b2-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d52b2-116">See also</span></span>

- [<span data-ttu-id="d52b2-117">Ansi</span><span class="sxs-lookup"><span data-stu-id="d52b2-117">Ansi</span></span>](../../../visual-basic/language-reference/modifiers/ansi.md)
- [<span data-ttu-id="d52b2-118">Auto</span><span class="sxs-lookup"><span data-stu-id="d52b2-118">Auto</span></span>](../../../visual-basic/language-reference/modifiers/auto.md)
- [<span data-ttu-id="d52b2-119">Mots clés</span><span class="sxs-lookup"><span data-stu-id="d52b2-119">Keywords</span></span>](../../../visual-basic/language-reference/keywords/index.md)
