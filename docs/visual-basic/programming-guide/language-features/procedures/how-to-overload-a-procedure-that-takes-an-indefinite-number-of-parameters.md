---
title: 'Procédure : Surcharger une procédure qui accepte un nombre indéfini de paramètres (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- procedures [Visual Basic], parameters
- procedure overloading [Visual Basic], indefinite number of parameters
- procedures [Visual Basic], defining
- Visual Basic code, procedures
- procedure parameters
- procedures [Visual Basic], overloading
- procedures [Visual Basic], multiple versions
ms.assetid: c7042de2-2422-4039-94e8-ac298896af69
ms.openlocfilehash: 3cf75fc6221364704379eb23d308481c34e6c0d6
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59316451"
---
# <a name="how-to-overload-a-procedure-that-takes-an-indefinite-number-of-parameters-visual-basic"></a>Procédure : Surcharger une procédure qui accepte un nombre indéfini de paramètres (Visual Basic)
Si une procédure possède un [ParamArray](../../../../visual-basic/language-reference/modifiers/paramarray.md) paramètre, vous ne pouvez pas définir une version surchargée acceptant un tableau unidimensionnel pour le tableau de paramètres. Pour plus d’informations, consultez « Implicite des surcharges pour un paramètre ParamArray » dans [considérations dans les procédures de surcharge](./considerations-in-overloading-procedures.md).  
  
### <a name="to-overload-a-procedure-that-takes-a-variable-number-of-parameters"></a>Surcharger une procédure qui accepte un nombre variable de paramètres  
  
1. S’assurer que la procédure et les avantages de logique de code à partir de l’appel surchargées versions plus d’à partir d’un `ParamArray` paramètre. Consultez « Surcharges et ParamArrays » dans [considérations sur les surcharges de procédures](./considerations-in-overloading-procedures.md).  
  
2. Déterminer les numéros des valeurs fournies que la procédure doit accepter dans la partie variable de la liste de paramètres. Cela peut inclure le cas d’aucune valeur, et il peut inclure le cas d’un tableau unidimensionnel unique.  
  
3. Pour chaque nombre acceptable de valeurs fournies, écrivez un `Sub` ou `Function` instruction de déclaration qui définit la liste des paramètres correspondants. N’utilisez pas le `Optional` ou `ParamArray` mot clé dans la version surchargée.  
  
4. Dans chaque déclaration, faites précéder le `Sub` ou `Function` mot clé avec le [surcharges](../../../../visual-basic/language-reference/modifiers/overloads.md) mot clé.  
  
5. Après chaque déclaration, écrivez le code de procédure qui doit s’exécuter lorsque le code appelant fournit des valeurs correspondant à la liste des paramètres de cette déclaration.  
  
6. Terminez chaque procédure par le `End Sub` ou `End Function` instruction comme il convient.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant montre une procédure définie avec un [ParamArray](../../../../visual-basic/language-reference/modifiers/paramarray.md) paramètre, puis sur un ensemble de procédures surchargées équivalent.  
  
 [!code-vb[VbVbcnProcedures#69](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#69)]  
  
 [!code-vb[VbVbcnProcedures#70](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#70)]  
  
 Vous ne pouvez pas surcharger une procédure avec une liste de paramètres qui accepte un tableau unidimensionnel pour le tableau de paramètres. Toutefois, vous pouvez utiliser les signatures des autres surcharges implicites. Les déclarations suivantes illustrent ce principe.  
  
 [!code-vb[VbVbcnProcedures#71](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#71)]  
  
 Le code dans les versions surchargées n’a pas tester si le code appelant a fourni une ou plusieurs valeurs pour le `ParamArray` paramètre, ou si c’est le cas, combien. Visual Basic passe le contrôle à la version correspondant à la liste d’arguments appelante.  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Car une procédure avec un `ParamArray` paramètre équivaut à un ensemble de versions surchargées, vous ne pouvez pas surcharger une procédure avec une liste de paramètres correspondant à chacune de ces surcharges implicites. Pour plus d’informations, consultez [considérations dans les procédures de surcharge](./considerations-in-overloading-procedures.md).  
  
## <a name="net-framework-security"></a>Sécurité .NET Framework  
 Chaque fois que vous avez affaire à un tableau qui peut s’avérer indéfiniment volumineux, il existe un risque de saturer la capacité interne de votre application. Si vous acceptez un tableau de paramètres, vous devez tester la longueur du tableau passé par le code appelant à celui-ci et prendre les mesures appropriées si elle est trop grande pour votre application.  
  
## <a name="see-also"></a>Voir aussi

- [Procédures](./index.md)
- [Paramètres et arguments d’une procédure](./procedure-parameters-and-arguments.md)
- [Paramètres facultatifs](./optional-parameters.md)
- [tableaux de paramètres](./parameter-arrays.md)
- [Surcharge de procédure](./procedure-overloading.md)
- [Procédures de dépannage](./troubleshooting-procedures.md)
- [Guide pratique pour Définir plusieurs Versions d’une procédure](./how-to-define-multiple-versions-of-a-procedure.md)
- [Guide pratique pour Appeler une procédure surchargée](./how-to-call-an-overloaded-procedure.md)
- [Guide pratique pour Surcharger une procédure qui accepte des paramètres optionnels](./how-to-overload-a-procedure-that-takes-optional-parameters.md)
- [Résolution de surcharge](./overload-resolution.md)
