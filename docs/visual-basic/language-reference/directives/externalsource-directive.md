---
title: '#ExternalSource, Directive (Visual Basic)'
ms.date: 07/20/2015
f1_keywords:
- '#Externalsource'
- '#ExternalSource'
- vb.ExternalSource
- Externalsource
- vb.#ExternalSource
- ExternalSource
helpviewer_keywords:
- ExternalSource directive (#ExternalSource)
- '#ExternalSource directive'
ms.assetid: 243bc6a2-34c3-4eeb-a776-9fd2bf988149
ms.openlocfilehash: 39e6963c97340daab3f0ab7ad6860695f1f6c135
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61747036"
---
# <a name="externalsource-directive"></a>#ExternalSource, directive
Indique un mappage entre des lignes spécifiques de code source et du texte externe à la source.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
#ExternalSource( StringLiteral , IntLiteral )  
    [ LogicalLine+ ]  
#End ExternalSource  
```  
  
## <a name="parts"></a>Composants  
 `StringLiteral`  
 Le chemin d’accès à la source externe.  
  
 `IntLiteral`  
 Le numéro de ligne de la première ligne de la source externe.  
  
 `LogicalLine`  
 La ligne où l’erreur se produit dans la source externe.  
  
 `#End ExternalSource`  
 Met fin au bloc `#ExternalSource`.  
  
## <a name="remarks"></a>Notes  
 Cette directive est utilisée uniquement par le compilateur et le débogueur.  
  
 Un fichier source peut inclure des directives de source externe, qui indiquent un mappage entre des lignes spécifiques de code dans le fichier source et du texte externe à la source, tel qu’un fichier .aspx. Si des erreurs sont rencontrées dans le code source désigné lors de la compilation, ils sont identifiés comme provenant de la source externe.  
  
 Directives de source externe n’ont aucun effet sur la compilation et ne peut pas être imbriquées. Ils sont destinés à un usage interne par l’application uniquement.  
  
## <a name="see-also"></a>Voir aussi

- [Compilation conditionnelle](../../../visual-basic/programming-guide/program-structure/conditional-compilation.md)
