---
title: L'inférence de type nullable n'est pas prise en charge dans ce contexte
ms.date: 07/20/2015
f1_keywords:
- vbc36629
- bc36629
helpviewer_keywords:
- BC36629
ms.assetid: 0a1e2dbc-d9a4-433d-9306-c5540782b81d
ms.openlocfilehash: 9f7f878649d8b96f050b56d5b878eb3d67e027ff
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61918220"
---
# <a name="nullable-type-inference-is-not-supported-in-this-context"></a>L'inférence de type nullable n'est pas prise en charge dans ce contexte
Types valeur et les structures peuvent être déclarés nullables.  
  
```vb  
Dim a? As Integer  
Dim b As Integer?  
```  
  
 Toutefois, vous ne pouvez pas utiliser la déclaration nullable en association avec l’inférence de type. Les exemples suivants provoquent cette erreur.  
  
```vb  
' Not valid.  
' Dim c? = 10  
' Dim d? = a  
```  
  
 **ID d’erreur :** BC36629  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Utilisez un `As` clause pour déclarer la variable nullable.  
  
## <a name="see-also"></a>Voir aussi

- [Types valeur Nullable](../../../visual-basic/programming-guide/language-features/data-types/nullable-value-types.md)
- [Inférence de type local](../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md)
