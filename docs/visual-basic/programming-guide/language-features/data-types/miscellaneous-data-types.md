---
title: Types de données divers (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- Object data type [Visual Basic], data types
- data types [Visual Basic], choosing
ms.assetid: 64c71a12-9057-4dbf-baca-7379c4aada69
ms.openlocfilehash: 9261a02f3dc286dc37b3073158ccc0c151030fe0
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
---
# <a name="miscellaneous-data-types-visual-basic"></a>Types de données divers (Visual Basic)
Visual Basic fournit plusieurs types de données qui ne sont pas adaptés pour les nombres ou de caractères. Au lieu de cela, ils traitent des données particulières telles qu’Oui/non valeurs, les valeurs de date/heure et des adresses de l’objet.  
  
 Pour un tableau présentant une comparaison côte-à-côte des types de données Visual Basic, consultez [des Types de données](../../../../visual-basic/language-reference/data-types/data-type-summary.md).  
  
## <a name="boolean-type"></a>Type booléen  
 Le [Type de données booléen](../../../../visual-basic/language-reference/data-types/boolean-data-type.md) est une valeur non signée qui est interprétée comme `True` ou `False`. Sa largeur de données dépend de la plateforme d’implémentation. Si une variable peut contenir uniquement des valeurs de deux États telles que true/false, Oui/Non, ou activé/désactivé, déclarez-le en tant que `Boolean`.  
  
## <a name="date-type"></a>Type de date  
 Le [Type de données Date](../../../../visual-basic/language-reference/data-types/date-data-type.md) est une valeur 64 bits qui contient des informations de date et heure. Chaque incrément représente 100 nanosecondes du temps écoulé depuis le début (12:00 AM), du 1er janvier de l’année 1 du calendrier grégorien. Si une variable peut contenir une valeur de date, une valeur d’heure ou les deux, déclarez-le en tant que `Date`.  
  
## <a name="object-type"></a>Type d'objet  
 Le [Type de données d’objet](../../../../visual-basic/language-reference/data-types/object-data-type.md) est une adresse 32 bits qui pointe vers une instance d’objet dans votre application ou dans une autre application. Une `Object` variable peut faire référence à n’importe quel objet que votre application reconnaît ou à des données de n’importe quel type de données. Cela inclut les deux *types valeur*, tel que `Integer`, `Boolean`et les instances de la structure, et *types référence*, qui sont des instances d’objets créés à partir de classes comme `String`et <xref:System.Windows.Forms.Form>et les instances de tableau.  
  
 Si une variable stocke un pointeur vers une instance d’une classe que vous ne connaissez pas au moment de la compilation, ou si elle peut pointer vers des données de différents types de données, déclarez-le en tant que `Object`.  
  
 L’avantage de le `Object` est de type de données que vous pouvez l’utiliser pour stocker les données de n’importe quel type de données. L’inconvénient est que vous encourez des opérations supplémentaires qui prennent plus de temps d’exécution et que votre application plus lentes. Si vous utilisez un `Object` variable pour les types valeur, vous encourez *boxing* et *unboxing*. Si vous l’utilisez pour les types référence, vous subissez *liaison tardive*.  
  
## <a name="see-also"></a>Voir aussi  
 [Caractères de type](../../../../visual-basic/programming-guide/language-features/data-types/type-characters.md)  
 [Types de données élémentaires](../../../../visual-basic/programming-guide/language-features/data-types/elementary-data-types.md)  
 [Types de données numériques](../../../../visual-basic/programming-guide/language-features/data-types/numeric-data-types.md)  
 [Types de données caractère](../../../../visual-basic/programming-guide/language-features/data-types/character-data-types.md)  
 [Dépannage des types de données](../../../../visual-basic/programming-guide/language-features/data-types/troubleshooting-data-types.md)  
 [Liaison anticipée et liaison tardive](../../../../visual-basic/programming-guide/language-features/early-late-binding/index.md)
