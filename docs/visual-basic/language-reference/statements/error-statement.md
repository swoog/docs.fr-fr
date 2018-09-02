---
title: Error, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.error
helpviewer_keywords:
- Error statement [Visual Basic], syntax
- Error statement [Visual Basic]
- Error keyword [Visual Basic]
- run-time errors [Visual Basic], codes
- errors [Visual Basic], simulating
ms.assetid: 85cd5c59-5224-4f02-aaf5-fcfefab17a29
ms.openlocfilehash: 84fce92183228cbfa5554a3ba45770a86e83bff5
ms.sourcegitcommit: efff8f331fd9467f093f8ab8d23a203d6ecb5b60
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/01/2018
ms.locfileid: "43400625"
---
# <a name="error-statement"></a><span data-ttu-id="c106c-102">Error, instruction</span><span class="sxs-lookup"><span data-stu-id="c106c-102">Error Statement</span></span>
<span data-ttu-id="c106c-103">Simule la présence d’une erreur.</span><span class="sxs-lookup"><span data-stu-id="c106c-103">Simulates the occurrence of an error.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="c106c-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c106c-104">Syntax</span></span>  
  
```  
Error errornumber  
```  
  
## <a name="parts"></a><span data-ttu-id="c106c-105">Composants</span><span class="sxs-lookup"><span data-stu-id="c106c-105">Parts</span></span>  
 `errornumber`  
 <span data-ttu-id="c106c-106">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="c106c-106">Required.</span></span> <span data-ttu-id="c106c-107">Peut être n’importe quel numéro d’erreur valide.</span><span class="sxs-lookup"><span data-stu-id="c106c-107">Can be any valid error number.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="c106c-108">Notes</span><span class="sxs-lookup"><span data-stu-id="c106c-108">Remarks</span></span>  
 <span data-ttu-id="c106c-109">La `Error` instruction est prise en charge pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="c106c-109">The `Error` statement is supported for backward compatibility.</span></span> <span data-ttu-id="c106c-110">Dans le nouveau code, en particulier lors de la création d’objets, utilisez le `Err` l’objet `Raise` méthode permettant de générer des erreurs d’exécution.</span><span class="sxs-lookup"><span data-stu-id="c106c-110">In new code, especially when creating objects, use the `Err` object's `Raise` method to generate run-time errors.</span></span>  
  
 <span data-ttu-id="c106c-111">Si `errornumber` est défini, le `Error` instruction appelle le Gestionnaire d’erreurs après les propriétés de la `Err` objet sont affectées les valeurs par défaut suivantes :</span><span class="sxs-lookup"><span data-stu-id="c106c-111">If `errornumber` is defined, the `Error` statement calls the error handler after the properties of the `Err` object are assigned the following default values:</span></span>  
  
|<span data-ttu-id="c106c-112">Propriété</span><span class="sxs-lookup"><span data-stu-id="c106c-112">Property</span></span>|<span data-ttu-id="c106c-113">Value</span><span class="sxs-lookup"><span data-stu-id="c106c-113">Value</span></span>|  
|--------------|-----------|  
|`Number`|<span data-ttu-id="c106c-114">Valeur spécifiée comme argument à `Error` instruction.</span><span class="sxs-lookup"><span data-stu-id="c106c-114">Value specified as argument to `Error` statement.</span></span> <span data-ttu-id="c106c-115">Peut être n’importe quel numéro d’erreur valide.</span><span class="sxs-lookup"><span data-stu-id="c106c-115">Can be any valid error number.</span></span>|  
|`Source`|<span data-ttu-id="c106c-116">Nom du projet Visual Basic actuel.</span><span class="sxs-lookup"><span data-stu-id="c106c-116">Name of the current Visual Basic project.</span></span>|  
|`Description`|<span data-ttu-id="c106c-117">Expression de chaîne correspondant à la valeur de retournée de la `Error` fonction spécifié `Number`, si cette chaîne existe.</span><span class="sxs-lookup"><span data-stu-id="c106c-117">String expression corresponding to the return value of the `Error` function for the specified `Number`, if this string exists.</span></span> <span data-ttu-id="c106c-118">Si la chaîne n’existe pas, `Description` contient une chaîne de longueur nulle ( » »).</span><span class="sxs-lookup"><span data-stu-id="c106c-118">If the string does not exist, `Description` contains a zero-length string ("").</span></span>|  
|`HelpFile`|<span data-ttu-id="c106c-119">Le lecteur complet, le chemin d’accès et le nom du fichier d’aide de Visual Basic approprié.</span><span class="sxs-lookup"><span data-stu-id="c106c-119">The fully qualified drive, path, and file name of the appropriate Visual Basic Help file.</span></span>|  
|`HelpContext`|<span data-ttu-id="c106c-120">Les fichier d’aide Visual Basic approprié ID de contexte pour l’erreur correspondant à la `Number` propriété.</span><span class="sxs-lookup"><span data-stu-id="c106c-120">The appropriate Visual Basic Help file context ID for the error corresponding to the `Number` property.</span></span>|  
|`LastDLLError`|<span data-ttu-id="c106c-121">Égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="c106c-121">Zero.</span></span>|  
  
 <span data-ttu-id="c106c-122">Si aucun gestionnaire d’erreur existe, ou si aucune n’est activée, un message d’erreur est créé et affiché à partir de la `Err` propriétés de l’objet.</span><span class="sxs-lookup"><span data-stu-id="c106c-122">If no error handler exists, or if none is enabled, an error message is created and displayed from the `Err` object properties.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="c106c-123">Certaines applications d’hôte de Visual Basic ne peut pas créer des objets.</span><span class="sxs-lookup"><span data-stu-id="c106c-123">Some Visual Basic host applications cannot create objects.</span></span> <span data-ttu-id="c106c-124">Consultez la documentation de votre application hôte pour déterminer si elle peut créer des classes et des objets.</span><span class="sxs-lookup"><span data-stu-id="c106c-124">See your host application's documentation to determine whether it can create classes and objects.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c106c-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="c106c-125">Example</span></span>  
 <span data-ttu-id="c106c-126">Cet exemple utilise la `Error` instruction pour générer le numéro d’erreur 11.</span><span class="sxs-lookup"><span data-stu-id="c106c-126">This example uses the `Error` statement to generate error number 11.</span></span>  
  
```  
On Error Resume Next   ' Defer error handling.  
Error 11   ' Simulate the "Division by zero" error.  
```  
  
## <a name="requirements"></a><span data-ttu-id="c106c-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c106c-127">Requirements</span></span>  
 <span data-ttu-id="c106c-128">**Namespace :** [Microsoft.VisualBasic](../../../visual-basic/language-reference/runtime-library-members.md)</span><span class="sxs-lookup"><span data-stu-id="c106c-128">**Namespace:** [Microsoft.VisualBasic](../../../visual-basic/language-reference/runtime-library-members.md)</span></span>  
  
 <span data-ttu-id="c106c-129">**Assembly :** bibliothèque Visual Basic Runtime (dans Microsoft.VisualBasic.dll)</span><span class="sxs-lookup"><span data-stu-id="c106c-129">**Assembly:** Visual Basic Runtime Library (in Microsoft.VisualBasic.dll)</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c106c-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c106c-130">See Also</span></span>  
 <xref:Microsoft.VisualBasic.ErrObject.Clear%2A>  
 <xref:Microsoft.VisualBasic.Information.Err%2A>  
 <xref:Microsoft.VisualBasic.ErrObject.Raise%2A>  
 [<span data-ttu-id="c106c-131">On Error (instruction)</span><span class="sxs-lookup"><span data-stu-id="c106c-131">On Error Statement</span></span>](../../../visual-basic/language-reference/statements/on-error-statement.md)  
 [<span data-ttu-id="c106c-132">Resume (instruction)</span><span class="sxs-lookup"><span data-stu-id="c106c-132">Resume Statement</span></span>](../../../visual-basic/language-reference/statements/resume-statement.md)  
 [<span data-ttu-id="c106c-133">Messages d’erreur</span><span class="sxs-lookup"><span data-stu-id="c106c-133">Error Messages</span></span>](../../../visual-basic/language-reference/error-messages/index.md)
