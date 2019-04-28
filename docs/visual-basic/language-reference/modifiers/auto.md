---
title: Auto (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Auto
helpviewer_keywords:
- Auto keyword [Visual Basic], external references
- Declare statement [Visual Basic], marshaling strings
- Auto keyword [Visual Basic]
- Auto keyword [Visual Basic], marshaling strings
ms.assetid: bf79ba95-a62c-48a5-916f-0ac7a52c13ec
ms.openlocfilehash: e4beb320b3aa0cadb790dd3ab92255496bc32f05
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61802698"
---
# <a name="auto-visual-basic"></a><span data-ttu-id="2b3a6-102">Auto (Visual Basic)</span><span class="sxs-lookup"><span data-stu-id="2b3a6-102">Auto (Visual Basic)</span></span>
<span data-ttu-id="2b3a6-103">Spécifie que Visual Basic doit marshaler les chaînes selon les règles de .NET Framework en fonction du nom externe de la procédure externe déclarée.</span><span class="sxs-lookup"><span data-stu-id="2b3a6-103">Specifies that Visual Basic should marshal strings according to .NET Framework rules based on the external name of the external procedure being declared.</span></span>  
  
 <span data-ttu-id="2b3a6-104">Lorsque vous appelez une procédure définie en dehors de votre projet, le compilateur Visual Basic n’a pas accès aux informations qu’il doit avoir appeler la procédure correctement.</span><span class="sxs-lookup"><span data-stu-id="2b3a6-104">When you call a procedure defined outside your project, the Visual Basic compiler does not have access to the information it must have to call the procedure correctly.</span></span> <span data-ttu-id="2b3a6-105">Ces informations incluent où se trouve la procédure, comment il est identifié, sa séquence d’appel et de type de retour, et chaîne de jeu de caractères qu’il utilise.</span><span class="sxs-lookup"><span data-stu-id="2b3a6-105">This information includes where the procedure is located, how it is identified, its calling sequence and return type, and the string character set it uses.</span></span> <span data-ttu-id="2b3a6-106">Le [instruction Declare](../../../visual-basic/language-reference/statements/declare-statement.md) crée une référence à une procédure externe et fournit ces informations nécessaires.</span><span class="sxs-lookup"><span data-stu-id="2b3a6-106">The [Declare Statement](../../../visual-basic/language-reference/statements/declare-statement.md) creates a reference to an external procedure and supplies this necessary information.</span></span>  
  
 <span data-ttu-id="2b3a6-107">Le `charsetmodifier` dans le `Declare` instruction fournit les informations de jeu de caractères pour marshaler des chaînes lors d’un appel à la procédure externe.</span><span class="sxs-lookup"><span data-stu-id="2b3a6-107">The `charsetmodifier` part in the `Declare` statement supplies the character set information for marshaling strings during a call to the external procedure.</span></span> <span data-ttu-id="2b3a6-108">Elle affecte également la façon dont Visual Basic recherche le fichier externe pour le nom de la procédure externe.</span><span class="sxs-lookup"><span data-stu-id="2b3a6-108">It also affects how Visual Basic searches the external file for the external procedure name.</span></span> <span data-ttu-id="2b3a6-109">Le `Auto` modificateur Spécifie que Visual Basic doit marshaler les chaînes selon les règles de .NET Framework et qu’elle doit déterminer le caractère de base défini de la plateforme d’exécution et, éventuellement, modifiez le nom de procédure externe si initial de recherche échoue.</span><span class="sxs-lookup"><span data-stu-id="2b3a6-109">The `Auto` modifier specifies that Visual Basic should marshal strings according to .NET Framework rules, and that it should determine the base character set of the run-time platform and possibly modify the external procedure name if the initial search fails.</span></span> <span data-ttu-id="2b3a6-110">Pour plus d’informations, consultez « Jeux de caractères » dans [instruction Declare](../../../visual-basic/language-reference/statements/declare-statement.md).</span><span class="sxs-lookup"><span data-stu-id="2b3a6-110">For more information, see "Character Sets" in [Declare Statement](../../../visual-basic/language-reference/statements/declare-statement.md).</span></span>  
  
 <span data-ttu-id="2b3a6-111">Si aucun modificateur de jeu de caractères est spécifié, `Ansi` est la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="2b3a6-111">If no character set modifier is specified, `Ansi` is the default.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="2b3a6-112">Notes</span><span class="sxs-lookup"><span data-stu-id="2b3a6-112">Remarks</span></span>  
 <span data-ttu-id="2b3a6-113">Le `Auto` modificateur peut être utilisé dans ce contexte :</span><span class="sxs-lookup"><span data-stu-id="2b3a6-113">The `Auto` modifier can be used in this context:</span></span>  
  
 [<span data-ttu-id="2b3a6-114">Declare (instruction)</span><span class="sxs-lookup"><span data-stu-id="2b3a6-114">Declare Statement</span></span>](../../../visual-basic/language-reference/statements/declare-statement.md)  
  
## <a name="smart-device-developer-notes"></a><span data-ttu-id="2b3a6-115">Remarques sur le développement Smart Device</span><span class="sxs-lookup"><span data-stu-id="2b3a6-115">Smart Device Developer Notes</span></span>  
 <span data-ttu-id="2b3a6-116">Ce mot clé n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="2b3a6-116">This keyword is not supported.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2b3a6-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2b3a6-117">See also</span></span>

- [<span data-ttu-id="2b3a6-118">Ansi</span><span class="sxs-lookup"><span data-stu-id="2b3a6-118">Ansi</span></span>](../../../visual-basic/language-reference/modifiers/ansi.md)
- [<span data-ttu-id="2b3a6-119">Unicode</span><span class="sxs-lookup"><span data-stu-id="2b3a6-119">Unicode</span></span>](../../../visual-basic/language-reference/modifiers/unicode.md)
- [<span data-ttu-id="2b3a6-120">Mots clés</span><span class="sxs-lookup"><span data-stu-id="2b3a6-120">Keywords</span></span>](../../../visual-basic/language-reference/keywords/index.md)
