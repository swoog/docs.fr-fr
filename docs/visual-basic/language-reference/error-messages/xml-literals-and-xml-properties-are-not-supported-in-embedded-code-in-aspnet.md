---
title: Les littéraux XML et les propriétés XML ne sont pas pris en charge dans du code incorporé au sein d'ASP.NET
ms.date: 07/20/2015
f1_keywords:
- vbc31200
- bc31200
helpviewer_keywords:
- BC31200
ms.assetid: 053e8cba-8584-45cc-9fa0-43d122779772
ms.openlocfilehash: 893fdb1b9b3b5ace6b869c7b64ce7483ff523023
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2018
ms.locfileid: "44180681"
---
# <a name="xml-literals-and-xml-properties-are-not-supported-in-embedded-code-within-aspnet"></a>Les littéraux XML et les propriétés XML ne sont pas pris en charge dans du code incorporé au sein d'ASP.NET
Littéraux XML et les propriétés XML ne sont pas pris en charge dans du code incorporé au sein d’ASP.NET. Pour utiliser les fonctionnalités XML, déplacez le code au code-behind.  
  
 Un littéral XML ou une propriété d’axe XML est définie dans le code incorporé (`<%= =>`) dans un fichier ASP.NET.  
  
 **ID d’erreur :** BC31200  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Déplacer le code qui inclut le littéral XML ou une propriété d’axe XML vers un fichier de code-behind ASP.NET.  
  
## <a name="see-also"></a>Voir aussi  
 [Littéraux XML](../../../visual-basic/language-reference/xml-literals/index.md)  
 [Propriétés d’axe XML](../../../visual-basic/language-reference/xml-axis/index.md)  
 [XML](../../../visual-basic/programming-guide/language-features/xml/index.md)
