---
title: Erase, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.Erase
helpviewer_keywords:
- Erase keyword [Visual Basic]
- Erase statement [Visual Basic]
ms.assetid: 7a8133d7-b750-4d74-8b66-ba1dd9778d4b
ms.openlocfilehash: bf3eb6476dc1485faeddab475f29e508175d3378
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61638185"
---
# <a name="erase-statement-visual-basic"></a>Erase, instruction (Visual Basic)
Permet de libérer des variables tableau ainsi que la mémoire utilisée pour leurs éléments.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Erase arraylist  
```  
  
## <a name="parts"></a>Composants  
 `arraylist`  
 Obligatoire. Liste des variables tableau à effacer. Les variables multiples sont séparées par des virgules.  
  
## <a name="remarks"></a>Notes  
 La `Erase` instruction peut apparaître seulement au niveau de la procédure. Cela signifie que vous pouvez libérer des tableaux à l’intérieur d’une procédure mais pas au niveau de classe ou le module.  
  
 Le `Erase` instruction est équivalente à l’attribution `Nothing` à chaque variable de tableau.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant utilise la `Erase` instruction pour effacer les deux tableaux et libérer leur mémoire (1 000 et 100 éléments de stockage, respectivement). La `ReDim` instruction assigne ensuite une nouvelle instance de tableau au tableau tridimensionnel.  
  
 [!code-vb[VbVbalrStatements#19](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrStatements/VB/Class1.vb#19)]  
  
## <a name="see-also"></a>Voir aussi

- [Nothing](../../../visual-basic/language-reference/nothing.md)
- [ReDim (instruction)](../../../visual-basic/language-reference/statements/redim-statement.md)
