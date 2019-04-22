---
title: Le type de '<variablename>' ne peut pas être déduit, car les limites de la boucle et la clause d'incrémentation ne sont pas converties en un même type
ms.date: 07/20/2015
f1_keywords:
- bc30982
- vbc30982
helpviewer_keywords:
- BC30982
ms.assetid: 741e85d9-a747-42ad-a1e1-a3f1928aaff5
ms.openlocfilehash: e90e881546c12df2c8b19ff03a4d4c7304c4596c
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "58815873"
---
# <a name="type-of-variablename-cannot-be-inferred-because-the-loop-bounds-and-the-step-variable-do-not-widen-to-the-same-type"></a>Type de '\<nom_variable >' ne peut pas être déduit, car les limites de la boucle et la variable étape s’étend pas au même type
Vous avez écrit un `For...Next` boucle dans laquelle le compilateur ne peut pas déduire un type de données pour la variable de contrôle de boucle, car les conditions suivantes sont remplies :  
  
-   Le type de données de la variable de contrôle de boucle n’est pas spécifié avec une clause `As` .  
  
-   Les limites de la boucle et l’incrémentation contiennent au moins deux types de données.  
  
-   Il n’existe aucune conversion standard entre les types de données.  
  
 Par conséquent, le compilateur ne peut pas déduire le type de données de variable de contrôle d’une boucle.  
  
 Dans l’exemple suivant, la variable de l’étape est un caractère et les limites de la boucle sont les deux entiers. Comme il n’existe aucune conversion standard entre les caractères et les entiers, cette erreur est signalée.  
  
```vb  
Dim stepVar = "1"c  
Dim m = 0  
Dim n = 20  
  
' Not valid.  
' For i = 1 To 10 Step stepVar  
    ' Loop processing  
' Next  
```  
  
 **ID d’erreur :** BC30982  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Modifier les types des limites de la boucle et selon vos besoins afin qu’au moins un d'entre eux est un type de la clause d’incrémentation. Dans l’exemple précédent, remplacez le type de `stepVar` à `Integer`.  
  
    ```  
    Dim stepVar = 1  
    ```  
  
     - ou -  
  
    ```  
    Dim stepVar As Integer = 1  
    ```  
  
-   Utiliser les fonctions de conversion explicite pour convertir les limites de la boucle et la variable de l’étape pour les types appropriés. Dans l’exemple précédent, vous devez appliquer le `Val` à fonction `stepVar`.  
  
    ```  
    For i = 1 To 10 Step Val(stepVar)  
        ' Loop processing  
    Next  
    ```  
  
## <a name="see-also"></a>Voir aussi

- <xref:Microsoft.VisualBasic.Conversion.Val%2A>
- [For...Next (instruction)](../../../visual-basic/language-reference/statements/for-next-statement.md)
- [Conversions implicites et explicites](../../../visual-basic/programming-guide/language-features/data-types/implicit-and-explicit-conversions.md)
- [Inférence de type local](../../../visual-basic/programming-guide/language-features/variables/local-type-inference.md)
- [Option Infer (instruction)](../../../visual-basic/language-reference/statements/option-infer-statement.md)
- [Fonctions de conversion de types](../../../visual-basic/language-reference/functions/type-conversion-functions.md)
- [Conversions étendues et restrictives](../../../visual-basic/programming-guide/language-features/data-types/widening-and-narrowing-conversions.md)
