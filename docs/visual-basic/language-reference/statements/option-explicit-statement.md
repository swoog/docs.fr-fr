---
title: Option Explicit, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Explicit
- vb.OptionExplicit
helpviewer_keywords:
- declaring variables [Visual Basic], explicit
- forced variable declaration in Option Explicit statement [Visual Basic]
- Explicit keyword
- explicit variable declaration
- Option Explicit statement [Visual Basic]
ms.assetid: e82ac1ad-2cd3-49b2-b985-8bcf016f3fcc
ms.openlocfilehash: 3a2d81b1441052c132e4739dfe6045f8c3a026d4
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33604599"
---
# <a name="option-explicit-statement-visual-basic"></a>Option Explicit, instruction (Visual Basic)
Force la déclaration explicite de toutes les variables dans un fichier, ou permet les déclarations implicites de variables.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Option Explicit { On | Off }  
```  
  
## <a name="parts"></a>Composants  
 `On`  
 Facultatif. Permet de `Option Explicit` la vérification. Si `On` ou `Off` n’est pas spécifié, la valeur par défaut est `On`.  
  
 `Off`  
 Facultatif. Désactive `Option Explicit` la vérification.  
  
## <a name="remarks"></a>Notes  
 Lorsque `Option Explicit On` ou `Option Explicit` apparaît dans un fichier, vous devez déclarer explicitement toutes les variables à l’aide de la `Dim` ou `ReDim` instructions. Si vous essayez d’utiliser un nom de variable non déclarée, une erreur se produit au moment de la compilation. La `Option Explicit Off` instruction permet une déclaration implicite des variables.  
  
 Si elle est utilisée, l'instruction `Option Explicit` doit apparaître dans un fichier avant toute autre instruction de code source.  
  
> [!NOTE]
>  Paramètre `Option Explicit` à `Off` n’est généralement pas recommandé. Vous risquez de mal orthographier un nom de variable dans un ou plusieurs emplacements, ce qui peut provoquer des résultats inattendus lors de l’exécution du programme.  
  
## <a name="when-an-option-explicit-statement-is-not-present"></a>Lorsqu’une instruction Option Explicit n’est pas présente  
 Si le code source ne contient pas un `Option Explicit` instruction, le **Option Explicit** définition sur le [Page Compiler, Concepteur de projets (Visual Basic)](/visualstudio/ide/reference/compile-page-project-designer-visual-basic) est utilisé. Si le compilateur de ligne de commande est utilisé, le [/optionexplicit](../../../visual-basic/reference/command-line-compiler/optionexplicit.md) option du compilateur est utilisée.  
  
#### <a name="to-set-option-explicit-in-the-ide"></a>Pour définir Option Explicit dans l’IDE  
  
1.  Dans l’**Explorateur de solutions**, sélectionnez un projet. Dans le menu **Projet**, cliquez sur **Propriétés**.  
  
2.  Cliquez sur l’onglet **Compiler**.  
  
3.  Définissez la valeur de la **Option Explicit** boîte.  
  
 Lorsque vous créez un nouveau projet, le **Option Explicit** définition sur le **compiler** onglet est définie sur le **Option Explicit** définition dans le **devaleurspardéfautVB**boîte de dialogue. Pour accéder à la **valeurs par défaut VB** boîte de dialogue le **outils** menu, cliquez sur **Options**. Dans la boîte de dialogue **Options**, développez **Projets et solutions**, puis cliquez sur **Valeurs par défaut VB**. Le paramètre par défaut initial dans **valeurs par défaut VB** est `On`.  
  
#### <a name="to-set-option-explicit-on-the-command-line"></a>Pour définir Option Explicit sur la ligne de commande  
  
-   Inclure le [/optionexplicit](../../../visual-basic/reference/command-line-compiler/optionexplicit.md) option du compilateur dans le **vbc** commande.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise la `Option Explicit` instruction pour forcer la déclaration explicite de toutes les variables. Essayez d’utiliser une variable non déclarée de provoque une erreur au moment de la compilation.  
  
 [!code-vb[VbVbalrStatements#47](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/option-explicit-statement_1.vb)]  
  
 [!code-vb[VbVbalrStatements#48](../../../visual-basic/language-reference/error-messages/codesnippet/VisualBasic/option-explicit-statement_2.vb)]  
  
## <a name="see-also"></a>Voir aussi  
 [Dim (instruction)](../../../visual-basic/language-reference/statements/dim-statement.md)  
 [ReDim (instruction)](../../../visual-basic/language-reference/statements/redim-statement.md)  
 [Option Compare (instruction)](../../../visual-basic/language-reference/statements/option-compare-statement.md)  
 [Option Strict (instruction)](../../../visual-basic/language-reference/statements/option-strict-statement.md)  
 [/optioncompare](../../../visual-basic/reference/command-line-compiler/optioncompare.md)  
 [/optionexplicit](../../../visual-basic/reference/command-line-compiler/optionexplicit.md)  
 [/optionstrict](../../../visual-basic/reference/command-line-compiler/optionstrict.md)  
 [Valeurs par défaut Visual Basic, Projets, boîte de dialogue Options](/visualstudio/ide/reference/visual-basic-defaults-projects-options-dialog-box)
