---
title: 'Procédure : Définir plusieurs Versions d’une procédure (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- procedures [Visual Basic], defining
- Visual Basic code, procedures
- procedures [Visual Basic], overloading
- procedures [Visual Basic], multiple versions
- procedure overloading [Visual Basic], multiple versions
ms.assetid: 71ccdd66-1b00-4b66-bee4-6926c0d696f4
ms.openlocfilehash: fc7a8e18394b904f0c22a80f71dee091d4f786ab
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59324030"
---
# <a name="how-to-define-multiple-versions-of-a-procedure-visual-basic"></a>Procédure : Définir plusieurs Versions d’une procédure (Visual Basic)
Vous pouvez définir une procédure dans plusieurs versions par *surcharge* il, à l’aide du même nom mais une liste de paramètres différente pour chaque version. L’objectif de la surcharge consiste à définir plusieurs versions étroitement liées d’une procédure sans avoir à les différencier par nom.  
  
 Pour plus d'informations, consultez [Procedure Overloading](./procedure-overloading.md).  
  
### <a name="to-define-multiple-versions-of-a-procedure"></a>Pour définir plusieurs versions d’une procédure  
  
1. Écrire un `Sub` ou `Function` instruction de déclaration pour chaque version de la procédure que vous souhaitez définir. Utilisez le même nom de procédure dans chaque déclaration.  
  
2. Faites précéder le `Sub` ou `Function` mot clé dans chaque déclaration avec la [surcharges](../../../../visual-basic/language-reference/modifiers/overloads.md) mot clé. Vous pouvez omettre `Overloads` dans les déclarations, mais si vous l’incluez dans une des déclarations, vous devez l’inclure dans toutes les déclarations.  
  
3. Après chaque instruction de déclaration, écrire du code de procédure pour gérer le cas spécifique où le code appelant fournit des arguments de liste de paramètres de cette version de mise en correspondance. Vous n’avez pas à tester pour quels paramètres le code appelant a fourni. Visual Basic passe le contrôle à la version correspondante de votre procédure.  
  
4. Mettre fin à chaque version de la procédure avec le `End Sub` ou `End Function` instruction comme il convient.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant définit un `Sub` procédure pour publier une transaction de solde d’un client. Il utilise le `Overloads` mot clé pour définir deux versions de la procédure, un autre qui accepte le client par nom et l’autre par numéro de compte.  
  
 [!code-vb[VbVbcnProcedures#72](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#72)]  
  
 Le code appelant peut obtenir l’identification du client selon un `String` ou un `Integer`, puis utilisez la même instruction appelante dans les deux cas.  
  
 Pour plus d’informations sur l’appel de ces versions de la `post` procédure, consultez [Comment : Appeler une procédure surchargée](./how-to-call-an-overloaded-procedure.md).  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Assurez-vous que chacune de vos versions surchargées a le même nom de procédure mais une autre liste de paramètres.  
  
## <a name="see-also"></a>Voir aussi

- [Procédures](./index.md)
- [Paramètres et arguments d’une procédure](./procedure-parameters-and-arguments.md)
- [Procédures de dépannage](./troubleshooting-procedures.md)
- [Guide pratique pour Surcharger une procédure qui accepte des paramètres optionnels](./how-to-overload-a-procedure-that-takes-optional-parameters.md)
- [Guide pratique pour Surcharger une procédure qui accepte un nombre indéfini de paramètres](./how-to-overload-a-procedure-that-takes-an-indefinite-number-of-parameters.md)
- [Considérations sur les surcharges de procédures](./considerations-in-overloading-procedures.md)
- [Résolution de surcharge](./overload-resolution.md)
