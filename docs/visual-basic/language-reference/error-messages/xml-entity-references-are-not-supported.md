---
title: Les références d'entité XML ne sont pas prises en charge
ms.date: 07/20/2015
f1_keywords:
- vbc31180
- bc31180
helpviewer_keywords:
- BC31180
ms.assetid: 2a393327-d8e2-4187-85b1-642b4f53b4ae
ms.openlocfilehash: dd7add295641e6a27c361c663d6075413b0f499c
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58824687"
---
# <a name="xml-entity-references-are-not-supported"></a>Les références d'entité XML ne sont pas prises en charge
Une référence d’entité (par exemple, `©`) qui n’est pas défini dans le XML 1.0 specification est incluse en tant que valeur pour un littéral XML. Uniquement `&`, `"`, `<`, `>`, et `'` références d’entité XML sont pris en charge dans les littéraux XML.  
  
 **ID d’erreur :** BC31180  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Supprimez la référence d’entité non pris en charge.  
  
## <a name="see-also"></a>Voir aussi

- [Littéraux XML et spécification XML 1.0](../../../visual-basic/programming-guide/language-features/xml/xml-literals-and-the-xml-1-0-specification.md)
- [Littéraux XML](../../../visual-basic/language-reference/xml-literals/index.md)
- [XML](../../../visual-basic/programming-guide/language-features/xml/index.md)
