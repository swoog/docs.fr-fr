---
title: Paramètres et arguments d’une procédure (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- procedures [Visual Basic], arguments
- procedures [Visual Basic], argument lists
- values [Visual Basic], passing to procedures
- arguments [Visual Basic], passing
- procedures [Visual Basic], parameters
- Visual Basic code, argument lists
- Visual Basic code, procedures
- parameters [Visual Basic], Visual Basic procedures
- parameters [Visual Basic], lists
- arguments [Visual Basic], Visual Basic procedures
- arguments [Visual Basic], procedures
- parameter lists [Visual Basic]
- Visual Basic code, parameter lists
- argument lists [Visual Basic]
- procedures [Visual Basic], parameter lists
ms.assetid: ff275aff-aa13-40df-bd4c-63486db8c1e9
ms.openlocfilehash: 4b62e4b752074bb8d1a660e51ab230a87ff21db4
ms.sourcegitcommit: 15ab532fd5e1f8073a4b678922d93b68b521bfa0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2019
ms.locfileid: "58654235"
---
# <a name="procedure-parameters-and-arguments-visual-basic"></a>Paramètres et arguments d’une procédure (Visual Basic)
Dans la plupart des cas, une procédure a besoin d’informations sur les circonstances dans lesquelles elle a été appelée. Une procédure qui effectue les tâches répétitives ou partagées utilise des informations différentes pour chaque appel. Ces informations se composent des variables, constantes et expressions que vous passez à la procédure lorsque vous l’appelez.  
  
 Un *paramètre* représente une valeur de la procédure suppose que vous fournissez lorsque vous l’appelez. Déclaration de la procédure définit ses paramètres.  
  
 Vous pouvez définir une procédure sans paramètres, un seul paramètre, ou plusieurs fois. La partie de la définition de procédure qui spécifie les paramètres est appelée le *liste de paramètres*.  
  
 Un *argument* représente la valeur que vous fournissez à un paramètre de procédure lorsque vous appelez la procédure. Le code appelant fournit les arguments lorsqu’il appelle la procédure. La partie de l’appel de procédure qui spécifie les arguments est appelée le *liste d’arguments*.  
  
 L’illustration suivante montre le code appelant la procédure `safeSquareRoot` à partir de deux emplacements différents. Le premier appel passe la valeur de la variable `x` (4.0) au paramètre `number`et la valeur de retour dans `root` (2.0) est affectée à la variable `y`. Le deuxième appel passe la valeur de littéral 9.0 à `number`et assigne la valeur de retournée (3.0) à la variable `z`.  
  
 ![Diagramme illustrant le passage d’un argument à un paramètre](./media/procedure-parameters-and-arguments/pass-argument-parameter.gif)  
  
 Pour plus d’informations, consultez [différences entre les paramètres et Arguments](./differences-between-parameters-and-arguments.md).  
  
## <a name="parameter-data-type"></a>Type de données de paramètre  
 Vous définissez un type de données pour un paramètre à l’aide de la `As` clause dans sa déclaration. Par exemple, la fonction suivante accepte une chaîne et un entier.  
  
 [!code-vb[VbVbcnProcedures#32](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#32)]  
  
 Si le commutateur de vérification de type ([Option Strict, instruction](../../../../visual-basic/language-reference/statements/option-strict-statement.md)) est `Off,` le `As` clause est facultative, sauf si un paramètre l’utilise, tous les paramètres doivent l’utiliser. Si la vérification de type est `On`, le `As` clause est requise pour tous les paramètres de procédure.  
  
 Si le code appelant est censé fournir un argument avec un type de données différent de celui de son paramètre correspondant, tel que `Byte` à un `String` paramètre, il doit effectuer l’une des opérations suivantes :  
  
-   Fournissez uniquement des arguments avec les types de données qui s’étendent vers le type de données de paramètre ;  
  
-   Définissez `Option Strict Off` pour permettre les conversions restrictives implicites ; ou  
  
-   Utilisez un mot clé de conversion pour convertir explicitement le type de données.  
  
### <a name="type-parameters"></a>Paramètres de type  
 Un *procédure générique* définit également un ou plusieurs *paramètres de type* en plus de ses paramètres normaux. Une procédure générique permet au code appelant à passer différents types de données chaque fois qu’il appelle la procédure, il peut adapter les types de données sur les exigences de chaque appel. Consultez [Generic Procedures in Visual Basic](../../../../visual-basic/programming-guide/language-features/data-types/generic-procedures.md).  
  
## <a name="see-also"></a>Voir aussi
- [Procédures](./index.md)
- [Procédures Sub](./sub-procedures.md)
- [Procédures Function](./function-procedures.md)
- [Procédures de propriété](./property-procedures.md)
- [Procédures d’opérateur](./operator-procedures.md)
- [Guide pratique pour Définir un paramètre pour une procédure](./how-to-define-a-parameter-for-a-procedure.md)
- [Guide pratique pour Passer des Arguments à une procédure](./how-to-pass-arguments-to-a-procedure.md)
- [Passage d’un argument par valeur et par référence](./passing-arguments-by-value-and-by-reference.md)
- [Surcharge de procédure](./procedure-overloading.md)
- [Conversions de type en Visual Basic](../../../../visual-basic/programming-guide/language-features/data-types/type-conversions.md)
