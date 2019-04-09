---
title: Types de données de base
ms.date: 03/30/2017
ms.assetid: eca2c472-9548-4800-bd31-5d8d9f11752b
ms.openlocfilehash: 00d5c6d866453fe9ece7f2e22a579aa43c09c23e
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59072881"
---
# <a name="basic-data-types"></a>Types de données de base
Les requêtes LINQ to SQL sont traduites en données Transact-SQL avant d'être exécutées sur Microsoft SQL Server. LINQ to SQL prend en charge une grande partie des fonctionnalités intégrées que SQL Server prend en charge pour les types de données de base.  
  
## <a name="casting"></a>Cast  
 Les casts implicites ou explicites sont activés d'un type CLR source en un type CLR cible s'il existe une conversion valide semblable dans SQL Server. Pour plus d’informations sur le cast CLR, consultez [CType Function](~/docs/visual-basic/language-reference/functions/ctype-function.md) (Visual Basic) et [comme](~/docs/csharp/language-reference/keywords/as.md). Après la conversion, les casts modifient le comportement d'opérations effectuées sur une expression CLR pour correspondre au comportement d'autres expressions CLR qui mappent naturellement au type de destination. Les casts sont également traduisibles dans le contexte de mappage d'héritage. Les objets peuvent être castés à des sous-types d'entité plus spécifiques afin que les données spécifiques à leur sous-type soient accessibles.  
  
## <a name="equality-operators"></a>Opérateurs d'égalité  
 LINQ to SQL prend en charge les opérateurs d'égalité suivants sur les types de données de base à l'intérieur des requêtes LINQ to SQL :  
  
-   Égale et opérateur d’inégalité : Opérateurs d’égalité et d’inégalité sont pris en charge pour numérique, <xref:System.Boolean>, <xref:System.DateTime>, et <xref:System.TimeSpan> types. Pour plus d’informations sur les opérateurs de Visual Basic `=` et `<>`, consultez [opérateurs de comparaison](~/docs/visual-basic/language-reference/operators/comparison-operators.md). Pour plus d’informations sur C# opérateurs de comparaison `==` et `!=`, consultez [opérateurs d’égalité](~/docs/csharp/language-reference/operators/equality-operators.md).
  
-   Est un opérateur : Le `IS` opérateur a une traduction prise en charge lorsque le mappage d’héritage est utilisé. Il peut être utilisé à la place du test direct de la colonne de discriminateur afin de déterminer si un objet correspond à un type d'entité spécifique et se traduit en un contrôle sur la colonne de discriminateur. Pour plus d’informations sur Visual Basic et C# est opérateurs, consultez [opérateur Is](~/docs/visual-basic/language-reference/operators/is-operator.md) et [est](~/docs/csharp/language-reference/keywords/is.md).  
  
## <a name="see-also"></a>Voir aussi

- [Mappage de type SQL-CLR](../../../../../../docs/framework/data/adonet/sql/linq/sql-clr-type-mapping.md)
- [Fonctions et types de données](../../../../../../docs/framework/data/adonet/sql/linq/data-types-and-functions.md)
