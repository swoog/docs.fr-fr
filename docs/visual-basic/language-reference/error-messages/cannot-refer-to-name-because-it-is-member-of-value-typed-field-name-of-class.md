---
title: Ne peut pas faire référence à &#39; &lt;nom&gt; &#39; , car il est membre du champ de valeur typée &#39; &lt;nom&gt; &#39; de classe &#39; &lt;classname&gt; &#39;qui a &#39;System.MarshalByRefObject&#39; comme classe de base
ms.date: 07/20/2015
f1_keywords:
- vbc30310
- bc30310
helpviewer_keywords:
- BC30310
ms.assetid: 2aeb8872-7c87-4f01-98ef-9714ba3eebbe
ms.openlocfilehash: f44d33c9d51148e6bbcfbf5db4dbc115101df1f1
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33586345"
---
# <a name="cannot-refer-to-39ltnamegt39-because-it-is-a-member-of-the-value-typed-field-39ltnamegt39-of-class-39ltclassnamegt39-which-has-39systemmarshalbyrefobject39-as-a-base-class"></a>Ne peut pas faire référence à &#39; &lt;nom&gt; &#39; , car il est membre du champ de valeur typée &#39; &lt;nom&gt; &#39; de classe &#39; &lt;classname&gt; &#39;qui a &#39;System.MarshalByRefObject&#39; comme classe de base
La `System.MarshalByRefObject` classe permet aux applications qui prennent en charge l’accès à distance à des objets entre les limites du domaine d’application. Types doivent hériter la `MarshalByRejectObject` classe lorsque le type est utilisé dans les limites du domaine d’application. L’état de l’objet ne doit pas être copié, car les membres de l’objet ne sont pas utilisables en dehors du domaine d’application dans lequel ils ont été créés.  
  
 **ID d’erreur :** BC30310  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Vérification de la référence de s’assurer que le membre fait référence est valide.  
  
2.  Qualifier explicitement le membre avec le `Me` (mot clé).  
  
## <a name="see-also"></a>Voir aussi  
 <xref:System.MarshalByRefObject>  
 [Dim (instruction)](../../../visual-basic/language-reference/statements/dim-statement.md)
