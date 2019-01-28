---
title: Checked et Unchecked - Référence C#
ms.custom: seodec18
ms.date: 05/15/2018
helpviewer_keywords:
- operators [C#], checked and unchecked
- exceptions [C#], overflow checking
- checked statement [C#]
- overflow checking [C#]
- unchecked statement [C#]
- statements [C#], checked and unchecked
ms.assetid: a84bc877-2c7f-4396-8735-1ce97c42f35e
ms.openlocfilehash: 12f65fe4b1dc710ff5c053073817dbd793c86082
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54511835"
---
# <a name="checked-and-unchecked-c-reference"></a>Checked et Unchecked (référence C#)
Les instructions C# peuvent s'exécuter dans un contexte vérifié (checked) ou non vérifié (unchecked). Dans un contexte vérifié, un dépassement de capacité arithmétique lève une exception. Dans un contexte non vérifié (unchecked), ce dépassement de capacité arithmétique est ignoré et le résultat est tronqué en supprimant tous les bits de poids fort qui ne tiennent pas dans le type destinataire.  
  
-   [checked](checked.md) Indique un contexte vérifié.  
  
-   [unchecked](unchecked.md) Indique un contexte non vérifié.  
  
 Les opérations suivantes sont concernées par la vérification du dépassement de capacité :  
  
-   Expressions utilisant les opérateurs prédéfinis suivants dans des types intégraux :  
  
     `++`, `--`, unaire `-`, `+`, `-`, `*`, `/`  
  
-   Conversions numériques explicites entre types intégraux, ou de `float` ou `double` en un type intégral.  
  
 Si ni `checked` ni `unchecked` ne sont spécifiés, le contexte par défaut pour les expressions non constantes (expressions évaluées au moment de l’exécution) est défini par la valeur de l’option [-checked](../compiler-options/checked-compiler-option.md) compilateur. Par défaut, la valeur de cette option n’est pas définie et les opérations arithmétiques sont exécutées dans un contexte non vérifié (unchecked).
 
 Pour les expressions constantes (expressions pouvant être complètement évaluées au moment de la compilation), le contexte par défaut est toujours vérifié (checked). Sauf si une expression constante est placée explicitement dans un contexte non vérifié (unchecked), les dépassements de capacité qui se produisent pendant l’évaluation lors de la compilation de l’expression entraînent des erreurs au moment de la compilation.
  
## <a name="see-also"></a>Voir aussi

- [Référence C#](../index.md)
- [Guide de programmation C#](../../programming-guide/index.md)
- [Mots clés C#](index.md)
- [Mots clés d’instructions](statement-keywords.md)
