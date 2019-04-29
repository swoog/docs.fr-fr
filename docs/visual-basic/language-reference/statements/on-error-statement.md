---
title: On Error, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.OnError
helpviewer_keywords:
- Visual Basic code, control flow
- Resume Next statement [Visual Basic]
- errors [Visual Basic], trapping
- error handling, On Error statement
- Next statement [Visual Basic], On Error
- control flow [Visual Basic], branching
- Error keyword [Visual Basic]
- execution [Visual Basic], conditional
- Resume statement [Visual Basic], and On Error statement
- Error statement [Visual Basic], and On Error statement
- GoTo statement [Visual Basic], and On Error statement
- branching [Visual Basic], on error
- conditional statements [Visual Basic], On Error
- On Error statement [Visual Basic], syntax
- On keyword [Visual Basic]
- run-time errors [Visual Basic], handling
- On Error statement [Visual Basic]
ms.assetid: ff947930-fb84-40cf-bd66-1ea219561d5c
ms.openlocfilehash: 0a5a5261e6b71178adce02a5635c1f91a1469f3d
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61784070"
---
# <a name="on-error-statement-visual-basic"></a>On Error, instruction (Visual Basic)
Valide une routine de gestion des erreurs et spécifie l’emplacement de la routine au sein d’une procédure ; peut également être utilisé pour désactiver une routine de gestion des erreurs.  
  
 Sans gestion des erreurs, une erreur d’exécution est irrécupérable : un message d’erreur s’affiche et l’exécution s’arrête.  
  
 Autant que possible, nous vous conseillons d’utiliser des exceptions structurées dans votre code de gestion des plutôt qu’à l’aide de la gestion non structurée et la `On Error` instruction. Pour plus d’informations, consultez [Try...Catch...Finally, instruction](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md).  
  
> [!NOTE]
>  Le `Error` clé est également utilisé dans le [Error, instruction](../../../visual-basic/language-reference/statements/error-statement.md), qui est pris en charge pour la compatibilité descendante.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
On Error { GoTo [ line | 0 | -1 ] | Resume Next }  
```  
  
## <a name="parts"></a>Composants  
  
|Terme|Définition|  
|---|---|  
|`GoTo` `line`|Active la routine de gestion des erreurs qui démarre à la ligne spécifiée dans le champ obligatoire `line` argument. Le `line` argument est une étiquette de ligne ou un numéro de ligne. Si une erreur d’exécution se produit, contrôler les branches de la ligne spécifiée, ce qui rend le Gestionnaire d’erreurs actif. La ligne spécifiée doit être dans la même procédure que le `On Error` instruction ou une erreur de compilation se produit.|  
|`GoTo` 0|Désactive le Gestionnaire d’erreurs activé dans la procédure actuelle et réinitialise à `Nothing`.|  
|`GoTo` -1|Désactive l’exception activée dans la procédure actuelle et réinitialise à `Nothing`.|  
|`Resume Next`|Spécifie que lorsqu’une erreur d’exécution se produit, le contrôle est transmis à l’instruction qui suit immédiatement l’instruction où l’erreur s’est produite et l’exécution se poursuit à partir de ce point. Utilisez ce formulaire plutôt que `On Error GoTo` lors de l’accès aux objets.|  
  
## <a name="remarks"></a>Notes  
  
> [!NOTE]
>  Nous vous recommandons d’utiliser Gestion structurée des exceptions dans votre code autant que possible, plutôt que d’à l’aide de la gestion non structurée et la `On Error` instruction. Pour plus d’informations, consultez [Try...Catch...Finally, instruction](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md).  
  
 Un gestionnaire d’erreurs « activé » est activé par un `On Error` instruction. Un gestionnaire d’erreurs « actif » est un gestionnaire activé qui est en cours de la gestion d’une erreur.  
  
 Si une erreur se produit pendant un gestionnaire d’erreurs est actif (entre l’occurrence de l’erreur et un `Resume`, `Exit Sub`, `Exit Function`, ou `Exit Property` instruction), gestionnaire d’erreurs de la procédure en cours ne peut pas gérer l’erreur. Contrôle retourne à la procédure appelante.  
  
 Si la procédure d’appel a un gestionnaire d’erreurs est activée, elle est activée pour gérer l’erreur. Si le Gestionnaire d’erreurs de la procédure appelante est également actif, contrôle passe par le biais de procédures précédentes de l’appelants jusqu'à ce qu’un gestionnaire d’erreurs est activée, mais il est inactif, est trouvé. Si aucun gestionnaire d’erreurs de ce type n’est trouvée, l’erreur est irrécupérable au point auquel elle s’est produite.  
  
 Chaque fois que le Gestionnaire d’erreurs repasse le contrôle à une procédure appelante, cette procédure devient la procédure en cours. Une fois qu’une erreur est gérée par un gestionnaire d’erreurs dans n’importe quelle procédure, l’exécution reprend dans la procédure actuelle à l’emplacement désigné par la `Resume` instruction.  
  
> [!NOTE]
>  Une routine de gestion des erreurs n’est pas un `Sub` procédure ou un `Function` procédure. C’est une section de code marquée par une étiquette de ligne ou un numéro de ligne.  
  
## <a name="number-property"></a>Propriété Number  
 Routines de gestion des erreurs s’appuient sur la valeur dans le `Number` propriété de la `Err` objet pour déterminer la cause de l’erreur. La routine doit tester ou enregistrer les valeurs de propriété pertinente dans le `Err` avant toute autre erreur peut se produire ou avant une procédure qui peut entraîner une erreur est appelée de l’objet. Les valeurs des propriétés dans le `Err` objet reflètent uniquement l’erreur la plus récente. Le message d’erreur associé `Err.Number` est contenue dans `Err.Description`.  
  
## <a name="throw-statement"></a>Throw, instruction  
 Une erreur est générée avec le `Err.Raise` méthode indique le `Exception` propriété à une instance nouvellement créée de la <xref:System.Exception> classe. Pour prendre en charge le déclenchement d’exceptions dérivées des types d’exception, un `Throw` instruction est prise en charge dans le langage. Cela prend un paramètre unique qui est l’instance d’exception levée. L’exemple suivant montre comment ces fonctionnalités peuvent être utilisées avec la prise en charge des exceptions existantes :  
  
 [!code-vb[VbVbalrErrorHandling#17](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrErrorHandling/VB/Class1.vb#17)]  
  
 Notez que la `On Error GoTo` instruction intercepte toutes les erreurs, quel que soit la classe d’exception.  
  
## <a name="on-error-resume-next"></a>On Error Resume Next  
 `On Error Resume Next` l’exécution continue avec l’instruction qui suit immédiatement l’instruction ayant provoqué l’erreur d’exécution, ou avec l’instruction qui suit immédiatement la plus récente d’appel de la procédure contenant le `On Error Resume Next` instruction. Cette instruction permet de continuer l’exécution malgré une erreur d’exécution. Vous pouvez placer la routine de gestion des erreurs où l’erreur peut se produire, plutôt que de transférer le contrôle vers un autre emplacement au sein de la procédure. Un `On Error Resume Next` instruction devient inactive lorsqu’une autre procédure est appelée, vous devez exécuter une `On Error Resume Next` instruction dans chaque appelée routine si vous souhaitez que la gestion au sein de cette routine d’erreur inline.  
  
> [!NOTE]
>  Le `On Error Resume Next` construction peut être préférable `On Error GoTo` lors de la gestion des erreurs générées pendant l’accès à d’autres objets. La vérification `Err` après chaque interaction avec un objet supprime l’ambiguïté dont l’objet est accessible par le code. Vous pouvez être sûr quel objet placé dans le code d’erreur `Err.Number`, ainsi que de l’objet qui a généré l’erreur (l’objet spécifié dans `Err.Source`).  
  
## <a name="on-error-goto-0"></a>On Error GoTo 0  
 `On Error GoTo 0` désactive la gestion des erreurs dans la procédure en cours. Il ne spécifie pas la ligne 0 comme le début du code de gestion des erreurs, même si la procédure contient une ligne numérotée de 0. Sans un `On Error GoTo 0` instruction, un gestionnaire d’erreurs est automatiquement désactivée lorsqu’une procédure se termine.  
  
## <a name="on-error-goto--1"></a>On Error GoTo -1  
 `On Error GoTo -1` désactive l’exception dans la procédure en cours. Il ne spécifie pas la ligne -1 comme le début du code de gestion des erreurs, même si la procédure contient une ligne numérotée -1. Sans un `On Error GoTo -1` instruction, une exception est automatiquement désactivée lorsqu’une procédure se termine.  
  
 Pour éviter que le code de gestion des erreurs en cours d’exécution lorsque aucune erreur ne se n’est produite, placez un `Exit Sub`, `Exit Function`, ou `Exit Property` instruction immédiatement avant la routine de gestion des erreurs, comme dans le fragment suivant :  
  
 [!code-vb[VbVbalrErrorHandling#18](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrErrorHandling/VB/Class1.vb#18)]  
  
 Ici, le code de gestion des erreurs suit la `Exit Sub` instruction et précède le `End Sub` instruction pour le séparer du flux de procédure. Vous pouvez placer n’importe où code de gestion des erreurs dans une procédure.  
  
## <a name="untrapped-errors"></a>Erreurs non interceptées  
 Erreurs non interceptées dans les objets sont retournés à l’application de contrôle lorsque l’objet s’exécute comme un fichier exécutable. Dans l’environnement de développement, les erreurs non interceptées sont retournées à l’application de contrôle uniquement si les options appropriées sont définies. Consultez la documentation de votre application hôte pour obtenir une description des options à jeu pendant le débogage, comment les définir, et la création de classes.  
  
 Si vous créez un objet qui accède à d’autres objets, vous devez tenter de gérer les erreurs non gérées retournées. Si vous ne pouvez pas mapper les codes d’erreur dans `Err.Number` à un de vos propres erreurs et transmettez les renvoyer à l’appelant de votre objet. Vous devez spécifier votre erreur en ajoutant votre code d’erreur à la `VbObjectError` constante. Par exemple, si votre code d’erreur est 1052, attribuez-lui comme suit :  
  
 [!code-vb[VbVbalrErrorHandling#19](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrErrorHandling/VB/Class1.vb#19)]  
  
> [!CAUTION]
>  Erreurs du système pendant les appels aux bibliothèques de liens dynamiques Windows (DLL) ne pas lever d’exceptions et ne peut pas être interceptées par Visual Basic. Lors de l’appel des fonctions DLL, vous devez vérifier chaque valeur de retour pour la réussite ou l’échec (selon les spécifications des API) et en cas de défaillance, vérifiez la valeur le `Err` l’objet `LastDLLError` propriété.  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise d’abord la `On Error GoTo` instruction pour spécifier l’emplacement d’une routine de gestion des erreurs dans une procédure. Dans l’exemple, une tentative de division par zéro génère l’erreur numéro 6. L’erreur est gérée dans la routine de gestion des erreurs, et le contrôle est ensuite retourné à l’instruction qui a provoqué l’erreur. La `On Error GoTo 0` instruction désactive l’interception des erreurs. La `On Error Resume Next` instruction permet de différer l’interception des erreurs afin que le contexte de l’erreur générée par l’instruction suivante peut être déterminé avec certitude. Notez que `Err.Clear` permet d’effacer le `Err` des propriétés de l’objet une fois que l’erreur est gérée.  
  
 [!code-vb[VbVbalrErrorHandling#20](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrErrorHandling/VB/Class1.vb#20)]  
  
## <a name="requirements"></a>Configuration requise  
 **Espace de noms :** [Microsoft.VisualBasic](../../../visual-basic/language-reference/runtime-library-members.md)  
  
 **Assembly :** bibliothèque Visual Basic Runtime (dans Microsoft.VisualBasic.dll)  
  
## <a name="see-also"></a>Voir aussi

- <xref:Microsoft.VisualBasic.Information.Err%2A>
- <xref:Microsoft.VisualBasic.ErrObject.Number%2A>
- <xref:Microsoft.VisualBasic.ErrObject.Description%2A>
- <xref:Microsoft.VisualBasic.ErrObject.LastDllError%2A>
- [End (instruction)](../../../visual-basic/language-reference/statements/end-statement.md)
- [Exit (instruction)](../../../visual-basic/language-reference/statements/exit-statement.md)
- [Resume (instruction)](../../../visual-basic/language-reference/statements/resume-statement.md)
- [Messages d’erreur](../../../visual-basic/language-reference/error-messages/index.md)
- [Try...Catch...Finally (instruction)](../../../visual-basic/language-reference/statements/try-catch-finally-statement.md)
