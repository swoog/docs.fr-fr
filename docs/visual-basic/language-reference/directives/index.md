---
title: Directives (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- directives, Visual Basic compiler
- Visual Basic code, directives
- directives
ms.assetid: 20d5fe65-490a-4c23-88c2-ee4f490ed762
ms.openlocfilehash: 38d54feae5cf7bf41a825d1f6000811e2b56f319
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/27/2018
ms.locfileid: "43000884"
---
# <a name="directives-visual-basic"></a>Directives (Visual Basic)
Les rubriques de cette section documentent les directives du compilateur de code source Visual Basic.  
  
## <a name="in-this-section"></a>Dans cette section  
 [#Const, Directive](../../../visual-basic/language-reference/directives/const-directive.md) --définir une constante de compilation  
  
 [#ExternalSource (directive)](../../../visual-basic/language-reference/directives/externalsource-directive.md) --indiquer un mappage entre les lignes sources et du texte externe à la source  
  
 [#If... Then... #Else Directives](../../../visual-basic/language-reference/directives/if-then-else-directives.md) --compiler des blocs de code sélectionnés  
  
 [Directive #Region](../../../visual-basic/language-reference/directives/region-directive.md) : réduire et masquer des sections de code dans l’éditeur Visual Studio  
  
 **#Disable, #Enable** : désactiver et activer des avertissements spécifiques pour les régions de code.  
  
```vb  
#Disable Warning BC42356 ' suppress warning about no awaits in this method  
    Async Function TestAsync() As Task  
        Console.WriteLine("testing")  
    End Function  
#Enable Warning BC42356  
```  
  
 Vous pouvez désactiver et activer une liste séparée par des virgules de codes d'avertissement.  
  
## <a name="related-sections"></a>Rubriques connexes  
 [Informations de référence sur le langage Visual Basic](../../../visual-basic/language-reference/index.md)  
  
 [Visual Basic](../../../visual-basic/index.md)
