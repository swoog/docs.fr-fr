---
title: Différences entre les paramètres et les arguments (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- procedures [Visual Basic], arguments
- procedures [Visual Basic], parameters
- parameters [Visual Basic], and arguments
- procedure arguments
- Visual Basic code, procedures
- arguments [Visual Basic], and parameters
- procedure parameters
- parameters [Visual Basic], definition
ms.assetid: c237c056-74f4-4749-9f2c-15864f139a31
ms.openlocfilehash: a69b956c7cffcc2a26916d6fc92f23dd4e2322d7
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61864245"
---
# <a name="differences-between-parameters-and-arguments-visual-basic"></a>Différences entre les paramètres et les arguments (Visual Basic)
Dans la plupart des cas, une procédure doit avoir des informations sur les circonstances dans lesquelles elle a été appelée. Une procédure qui effectue les tâches répétitives ou partagées utilise des informations différentes pour chaque appel. Ces informations se composent des variables, constantes et expressions que vous passez à la procédure lorsque vous l’appelez.  
  
 Pour communiquer ces informations à la procédure, la procédure définit un *paramètre*, et le code appelant passe un *argument* à ce paramètre. Vous pouvez considérer le paramètre comme un espace de parking et l’argument sous la forme d’une voiture. De même que plusieurs automobiles peuvent se dans un espace de parking à des moments différents, le code appelant peut passer un argument différent au même paramètre chaque fois qu’il appelle la procédure.  
  
## <a name="parameters"></a>Paramètres  
 Un *paramètre* représente une valeur de la procédure que vous devez passer lorsque vous l’appelez. Déclaration de la procédure définit ses paramètres.  
  
 Lorsque vous définissez un `Function` ou `Sub` procédure, vous spécifiez un *liste de paramètres* entre parenthèses immédiatement après le nom de la procédure. Pour chaque paramètre, vous spécifiez un nom, un type de données et un mécanisme de passage ([ByVal](../../../../visual-basic/language-reference/modifiers/byval.md) ou [ByRef](../../../../visual-basic/language-reference/modifiers/byref.md)). Vous pouvez également indiquer qu’un paramètre est facultatif. Cela signifie que le code appelant n’a pas de passer une valeur pour celle-ci.  
  
 Le nom de chaque paramètre sert un *variable locale* dans la procédure. Vous utilisez le nom du paramètre de la même façon que vous utilisez toute autre variable.  
  
## <a name="arguments"></a>Arguments  
 Un *argument* représente la valeur que vous passez à un paramètre de procédure lorsque vous appelez la procédure. Le code appelant fournit les arguments lorsqu’il appelle la procédure.  
  
 Lorsque vous appelez un `Function` ou `Sub` procédure, vous incluez un *liste d’arguments* entre parenthèses immédiatement après le nom de la procédure. Chaque argument correspond au paramètre dans la même position dans la liste.  
  
 Contrairement à la définition de paramètre, les arguments n’ont pas de noms. Chaque argument est une expression qui peut contenir zéro ou plusieurs variables, constantes et des littéraux. Le type de données de l’expression évaluée doit correspondre généralement le type de données défini pour le paramètre correspondant, et dans tous les cas, il doit être convertible au type de paramètre.  
  
## <a name="see-also"></a>Voir aussi

- [Procédures](./index.md)
- [Procédures Sub](./sub-procedures.md)
- [Procédures Function](./function-procedures.md)
- [Procédures de propriété](./property-procedures.md)
- [Procédures d’opérateur](./operator-procedures.md)
- [Guide pratique pour Définir un paramètre pour une procédure](./how-to-define-a-parameter-for-a-procedure.md)
- [Guide pratique pour Passer des Arguments à une procédure](./how-to-pass-arguments-to-a-procedure.md)
- [Passage d’un argument par valeur et par référence](./passing-arguments-by-value-and-by-reference.md)
- [Procédures récursives](./recursive-procedures.md)
- [Surcharge de procédure](./procedure-overloading.md)
