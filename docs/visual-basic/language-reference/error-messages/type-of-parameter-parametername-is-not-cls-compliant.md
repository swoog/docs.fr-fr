---
title: Le type de paramètre '<parametername>' n'est pas conforme CLS
ms.date: 07/20/2015
f1_keywords:
- vbc40028
- bc40028
helpviewer_keywords:
- BC40028
ms.assetid: dfa1f6f9-bb88-44ad-b85f-149144363d41
ms.openlocfilehash: e7cf058ef5e6b007a39213aa0ca5748a3b77458a
ms.sourcegitcommit: c7a7e1468bf0fa7f7065de951d60dfc8d5ba89f5
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/14/2019
ms.locfileid: "65590645"
---
# <a name="type-of-parameter-parametername-is-not-cls-compliant"></a>Type de paramètre '\<nom_paramètre >' n’est pas conforme CLS
Une procédure est marquée comme `<CLSCompliant(True)>` mais déclare un paramètre avec un type qui est marqué comme `<CLSCompliant(False)>`, n’est pas marqué ou non qualifié, car il est un type non conforme.  
  
 Pour qu’une procédure soit conforme à CLS ([Indépendance du langage et composants indépendants du langage](../../../standard/language-independence-and-language-independent-components.md)), elle doit utiliser uniquement des types conformes à CLS. Cette règle s’applique aux types des paramètres, au type de retour et aux types de toutes ses variables locales.  
  
 Les types de données Visual Basic suivants ne sont pas conformes CLS :  
  
- [SByte (type de données)](../../../visual-basic/language-reference/data-types/sbyte-data-type.md)  
  
- [UInteger (type de données)](../../../visual-basic/language-reference/data-types/uinteger-data-type.md)  
  
- [ULong (type de données)](../../../visual-basic/language-reference/data-types/ulong-data-type.md)  
  
- [UShort (type de données)](../../../visual-basic/language-reference/data-types/ushort-data-type.md)  
  
 Quand vous appliquez l’attribut <xref:System.CLSCompliantAttribute> à un élément de programmation, vous affectez au paramètre `isCompliant` de l’attribut la valeur `True` ou `False` pour indiquer la conformité ou la non-conformité. Il n’existe pas de valeur par défaut pour ce paramètre et vous devez fournir une valeur.  
  
 Si vous n’appliquez pas <xref:System.CLSCompliantAttribute> à un élément, il est considéré comme étant non conforme.  
  
 Par défaut, ce message est un avertissement. Pour plus d’informations sur le masquage des avertissements ou leur traitement en tant qu’erreurs, consultez [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).  
  
 **ID d’erreur :** BC40028  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Si la procédure doit prendre un paramètre de ce type particulier, supprimez le <xref:System.CLSCompliantAttribute>. La procédure ne peut pas être conforme à CLS.  
  
- Si la procédure doit être conforme CLS, modifier le type de ce paramètre pour le type conforme CLS le plus proche. Par exemple, vous pouvez utiliser `UInteger` au lieu de `Integer` si vous n’avez pas besoin de la plage de valeurs située au-dessus de 2 147 483 647. Si vous avez besoin de la plage étendue, vous pouvez remplacer `UInteger` par `Long`.  
  
- Si vous utilisez des objets Automation ou COM, n’oubliez pas que certains types ont des largeurs différentes données que dans le .NET Framework. Par exemple, `int` correspond souvent à 16 bits dans d’autres environnements. Si vous passez un entier 16 bits à partir d’un tel composant, déclarez-le en tant que `Short` au lieu de `Integer` dans votre code managé de Visual Basic.
