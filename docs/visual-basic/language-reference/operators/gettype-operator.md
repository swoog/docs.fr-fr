---
title: Opérateur GetType (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.GetType
helpviewer_keywords:
- GetType operator [Visual Basic]
- GetType keyword [Visual Basic]
ms.assetid: 4f733297-2503-4607-850c-15eba65fff90
ms.openlocfilehash: 34ab192814583db5cdc0d0183c73cc22b8633e9c
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58840314"
---
# <a name="gettype-operator-visual-basic"></a>Opérateur GetType (Visual Basic)
Retourne un <xref:System.Type> objet pour le type spécifié. Le <xref:System.Type> objet fournit des informations sur le type telles que ses propriétés, méthodes et événements.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
GetType(typename)  
```  
  
## <a name="parameters"></a>Paramètres  
  
|Paramètre|Description|  
|---|---|  
|`typename`|Le nom du type pour lequel vous souhaitez des informations.|  
  
## <a name="remarks"></a>Notes  
 Le `GetType` opérateur retourne le <xref:System.Type> objet spécifié `typename`. Vous pouvez passer le nom de n’importe quel type défini dans `typename`. Ce dernier est détaillé ci-après :  
  
-   Type de données Visual Basic, tel que `Boolean` ou `Date`.  
  
-   Toute classe .NET Framework, structure, module ou interface, tel que <xref:System.ArgumentException?displayProperty=nameWithType> ou <xref:System.Double?displayProperty=nameWithType>.  
  
-   Toute classe, structure, module ou interface définie par votre application.  
  
-   N’importe quel tableau définie par votre application.  
  
-   Tout délégué défini par votre application.  
  
-   Toute énumération définie par Visual Basic, le .NET Framework ou votre application.  
  
 Si vous souhaitez obtenir l’objet de type d’une variable objet, utilisez le <xref:System.Type.GetType%2A?displayProperty=nameWithType> (méthode).  
  
 Le `GetType` opérateur peut être utile dans les circonstances suivantes :  
  
-   Vous devez accéder à des métadonnées pour un type au moment de l’exécution. Le <xref:System.Type> objet qui fournit des métadonnées telles que les membres de type et des informations sur le déploiement. Vous devez, par exemple, pour refléter sur un assembly. Pour plus d'informations, consultez <xref:System.Reflection?displayProperty=nameWithType>.  
  
-   Vous souhaitez comparer deux références d’objet pour voir si elles font référence aux instances du même type. S’ils le font, `GetType` retourne des références au même <xref:System.Type> objet.  
  
## <a name="example"></a>Exemple  
 Les exemples suivants illustrent le `GetType` opérateur en cours d’utilisation.  
  
 [!code-vb[VbVbalrOperators#26](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrOperators/VB/Class1.vb#26)]  
  
## <a name="see-also"></a>Voir aussi

- [Priorité des opérateurs en Visual Basic](../../../visual-basic/language-reference/operators/operator-precedence.md)
- [Opérateurs répertoriés par fonctionnalité](../../../visual-basic/language-reference/operators/operators-listed-by-functionality.md)
- [Opérateurs et expressions](../../../visual-basic/programming-guide/language-features/operators-and-expressions/index.md)
