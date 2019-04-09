---
title: . (Accès aux membres) (Entity SQL)
ms.date: 03/30/2017
ms.assetid: 4733e3b2-3efa-4b96-b591-ac31350e96ad
ms.openlocfilehash: 6ebedd2b381d035d199e151f64632acf7d502ff5
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59139709"
---
# <a name="-member-access-entity-sql"></a>. (Accès aux membres) (Entity SQL)
L’opérateur point (.) est le [!INCLUDE[esql](../../../../../../includes/esql-md.md)] opérateur d’accès au membre. L'opérateur d'accès aux membres permet de produire la valeur d'une propriété ou d'un champ d'une instance de type de modèle conceptuel structurel.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
expression.identifier  
```  
  
## <a name="arguments"></a>Arguments  
 `expression`  
 Instance d'un type de modèle conceptuel structurel.  
  
 `identifier`  
 Propriété ou champ appartenant à une instance d'objet.  
  
## <a name="remarks"></a>Notes  
 L'opérateur point (.) peut être utilisé pour extraire les champs d'un enregistrement, de la même manière que l'on extrait les propriétés d'un type complexe ou d'un type d'entité. Par exemple, si n de type Nom est membre du type Personne et que p est une instance du type Personne, alors p.n est une expression d'accès aux membres valide qui produit une valeur de type Nom.  
  
 `select p.Name.FirstName from LOB.Person as p`  
  
## <a name="see-also"></a>Voir aussi

- [Référence Entity SQL](../../../../../../docs/framework/data/adonet/ef/language-reference/entity-sql-reference.md)
