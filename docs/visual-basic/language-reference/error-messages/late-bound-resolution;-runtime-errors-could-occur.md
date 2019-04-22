---
title: Résolution à liaison tardive ; des erreurs d’exécution peuvent se produire
ms.date: 07/20/2015
f1_keywords:
- vbc42017
- BC42017
helpviewer_keywords:
- BC42017
ms.assetid: 45f552c8-57c6-44c0-97d3-e510119b257a
ms.openlocfilehash: 4fe79c74b6ff634223a4f10d8c5dc54bb77571cc
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58822261"
---
# <a name="late-bound-resolution-runtime-errors-could-occur"></a>Résolution à liaison tardive ; des erreurs d’exécution peuvent se produire
Un objet est assigné à une variable déclarée comme étant de la [Object Data Type](../../../visual-basic/language-reference/data-types/object-data-type.md).  
  
 Lorsque vous déclarez une variable en tant que `Object`, le compilateur doit exécuter *liaison tardive*, ce qui entraîne des opérations supplémentaires au moment de l’exécution. Cela expose également votre application à des erreurs d’exécution potentielles. Par exemple, si vous assignez un <xref:System.Windows.Forms.Form> à la `Object` variable et réessayez d’accéder à la <xref:System.Xml.XmlDocument.NameTable%2A?displayProperty=nameWithType> propriété, le runtime lève un <xref:System.MemberAccessException> , car le <xref:System.Windows.Forms.Form> classe n’expose pas un `NameTable` propriété.  
  
 Si vous déclarez la variable comme étant d’un type spécifique, le compilateur peut exécuter *liaison anticipée* au moment de la compilation. Cela entraîne des performances améliorées, un accès contrôlé aux membres du type spécifique et une meilleure lisibilité de votre code.  
  
 Par défaut, ce message est un avertissement. Pour plus d’informations sur le masquage des avertissements ou leur traitement en tant qu’erreurs, consultez [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).  
  
 **ID d’erreur :** BC42017  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Si possible, déclarez la variable comme étant d’un type spécifique.  
  
## <a name="see-also"></a>Voir aussi

- [Liaison anticipée et liaison tardive](../../../visual-basic/programming-guide/language-features/early-late-binding/index.md)
- [Déclaration des variables objets](../../../visual-basic/programming-guide/language-features/variables/object-variable-declaration.md)
