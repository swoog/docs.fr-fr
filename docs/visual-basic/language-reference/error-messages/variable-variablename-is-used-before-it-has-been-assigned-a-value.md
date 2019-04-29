---
title: La variable '<variablename>' est utilisée avant qu'une valeur ne lui ait été assignée
ms.date: 07/20/2015
f1_keywords:
- vbc42104
- BC42104
helpviewer_keywords:
- BC42104
ms.assetid: 6909aa0b-b4a1-46f5-a18c-ba3e565c1dd8
ms.openlocfilehash: 46551a917aeb794c8d35985076b67a315386f628
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61766725"
---
# <a name="variable-variablename-is-used-before-it-has-been-assigned-a-value"></a>Variable '\<nom_variable >' est utilisée avant qu’il a reçu une valeur
Variable '\<nom_variable >' est utilisée avant une valeur lui ait été assignée. Cela peut provoquer une exception de référence null au moment de l’exécution.  
  
 Une application a au moins un chemin d’accès possible via son code qui lit une variable avant toute valeur est attribuée à ce dernier.  
  
 Si aucune valeur n’a jamais été assignée à une variable, elle contient la valeur par défaut de son type de données. Pour un type de données de référence, cette valeur par défaut est [Nothing](../../../visual-basic/language-reference/nothing.md). La lecture d’une variable de référence qui a la valeur `Nothing` peut provoquer une <xref:System.NullReferenceException> dans certaines circonstances.  
  
 Par défaut, ce message est un avertissement. Pour plus d’informations sur le masquage des avertissements ou le traitement des avertissements en tant qu’erreurs, consultez [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).  
  
 **ID d’erreur :** BC42104  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Vérifiez votre logique de flux de contrôle et assurez-vous que la variable a une valeur valide avant que le contrôle est passé à n’importe quelle instruction qui le lit.  
  
- Pour garantir que la variable a toujours une valeur valide consiste à initialiser dans le cadre de sa déclaration. Consultez « Initialisation » dans [Dim, instruction](../../../visual-basic/language-reference/statements/dim-statement.md).  
  
## <a name="see-also"></a>Voir aussi

- [Dim (instruction)](../../../visual-basic/language-reference/statements/dim-statement.md)
- [Déclaration de variable](../../../visual-basic/programming-guide/language-features/variables/variable-declaration.md)
- [Dépannage des variables](../../../visual-basic/programming-guide/language-features/variables/troubleshooting-variables.md)
