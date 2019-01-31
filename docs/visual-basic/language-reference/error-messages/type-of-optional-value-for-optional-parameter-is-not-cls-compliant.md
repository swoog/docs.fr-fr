---
title: Le type de la valeur facultative pour le paramètre optionnel <parametername> n'est pas conforme CLS
ms.date: 07/20/2015
f1_keywords:
- BC40042
- vbc40042
helpviewer_keywords:
- BC40042
ms.assetid: 1d6eae29-4ad3-4434-bde4-a53b6051adf5
ms.openlocfilehash: 39054fb6bf82a344cb38613164cb42968aa632f7
ms.sourcegitcommit: 14355b4b2fe5bcf874cac96d0a9e6376b567e4c7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/30/2019
ms.locfileid: "55261419"
---
# <a name="type-of-optional-value-for-optional-parameter-parametername-is-not-cls-compliant"></a>Type de valeur facultative pour le paramètre facultatif \<nom_paramètre > n’est pas conforme CLS
Une procédure est marquée comme `<CLSCompliant(True)>` mais déclare un paramètre [facultatif](../../../visual-basic/language-reference/modifiers/optional.md) avec la valeur par défaut d’un type non conforme.  
  
 Pour qu’une procédure soit conforme à CLS ([Indépendance du langage et composants indépendants du langage](../../../standard/language-independence-and-language-independent-components.md)), elle doit utiliser uniquement des types conformes à CLS. Cette règle s’applique aux types des paramètres, au type de retour et aux types de toutes ses variables locales. Elle s’applique également aux valeurs par défaut des paramètres facultatifs.  
  
 Les types de données Visual Basic suivants ne sont pas conformes CLS :  
  
-   [SByte (type de données)](../../../visual-basic/language-reference/data-types/sbyte-data-type.md)  
  
-   [UInteger (type de données)](../../../visual-basic/language-reference/data-types/uinteger-data-type.md)  
  
-   [ULong (type de données)](../../../visual-basic/language-reference/data-types/ulong-data-type.md)  
  
-   [UShort (type de données)](../../../visual-basic/language-reference/data-types/ushort-data-type.md)  
  
 Quand vous appliquez l’attribut <xref:System.CLSCompliantAttribute> à un élément de programmation, vous affectez au paramètre `isCompliant` de l’attribut la valeur `True` ou `False` pour indiquer la conformité ou la non-conformité. Il n’existe pas de valeur par défaut pour ce paramètre et vous devez fournir une valeur.  
  
 Si vous n’appliquez pas <xref:System.CLSCompliantAttribute> à un élément, il est considéré comme étant non conforme.  
  
 Par défaut, ce message est un avertissement. Pour plus d’informations sur le masquage des avertissements ou leur traitement en tant qu’erreurs, consultez [Configuring Warnings in Visual Basic](/visualstudio/ide/configuring-warnings-in-visual-basic).  
  
 **ID d’erreur :** BC40042  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
-   Si le paramètre facultatif doit avoir une valeur par défaut de ce type particulier, supprimez <xref:System.CLSCompliantAttribute>. La procédure ne peut pas être conforme à CLS.  
  
-   Si la procédure doit être conforme à CLS, remplacez le type de cette valeur par défaut par le type conforme à CLS le plus proche. Par exemple, vous pouvez utiliser `UInteger` au lieu de `Integer` si vous n’avez pas besoin de la plage de valeurs située au-dessus de 2 147 483 647. Si vous avez besoin de la plage étendue, vous pouvez remplacer `UInteger` par `Long`.  
  
-   Si vous interfacez avec des objets Automation ou COM, n’oubliez pas que certains types ont des largeurs de données différentes de celles du [!INCLUDE[dnprdnshort](~/includes/dnprdnshort-md.md)]. Par exemple, `int` correspond souvent à 16 bits dans d’autres environnements. Si vous passez un entier 16 bits à partir d’un tel composant, déclarez-le en tant que `Short` au lieu de `Integer` dans votre code managé de Visual Basic.