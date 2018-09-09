---
title: Conception de champs
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- fields, design guidelines
- read-only fields
- member design guidelines, fields
ms.assetid: 7cb4b0f3-7a10-4c93-b84d-733f7134fcf8
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 65c54fe9a076a219c61280a98c390b16f56b5015
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2018
ms.locfileid: "44251990"
---
# <a name="field-design"></a>Conception de champs
Le principe d’encapsulation est un des notions principales dans la conception orientée objet. Ce principe stipule que les données stockées à l’intérieur d’un objet doivent être accessibles uniquement à cet objet.  
  
 Un moyen utile pour interpréter le principe est à dire qu’un type doit être conçu afin que les modifications aux champs de ce type (modifications de nom ou type) peuvent être apportées sans casser le code autre que pour les membres du type. Cette interprétation implique immédiatement que tous les champs doivent être privés.  
  
 Nous excluons constante et statiques des champs en lecture seule à partir de cette restriction stricte, étant donné que ces champs, presque par définition, sont jamais doit modifier.  
  
 **X DO NOT** contiennent des champs d’instance qui sont publics ou protégés.  
  
 Vous devez fournir des propriétés pour accéder à des champs au lieu de les rendre publics ou protégés.  
  
 **✓ DO** utiliser les champs constants pour les constantes qui ne changent pas.  
  
 Le compilateur augmente les valeurs des champs constantes directement dans le code appelant. Par conséquent, les valeurs constantes ne peuvent jamais être modifiées sans risquer de perdre la compatibilité.  
  
 **✓ DO** utiliser statique public `readonly` champs pour les instances d’objet prédéfinies.  
  
 S’il existe des instances prédéfinies du type, déclarez les champs statiques en lecture seule comme publics du type lui-même.  
  
 **X DO NOT** affecter des instances de types mutables à `readonly` champs.  
  
 Un type mutable est un type avec des instances qui peuvent être modifiés une fois qu’ils sont instanciés. Par exemple, les tableaux, la plupart des collections et flux sont des types mutables, mais <xref:System.Int32?displayProperty=nameWithType>, <xref:System.Uri?displayProperty=nameWithType>, et <xref:System.String?displayProperty=nameWithType> sont toutes immuables. Le modificateur en lecture seule sur un champ de type référence empêche l’instance stockée dans le champ ne soit pas remplacé, mais il n’empêche pas les données d’instance du champ d’être modifiées en appelant des membres modification de l’instance.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson Education, Inc. et extrait de [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) par Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série sur le développement Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Instructions de conception des membres](../../../docs/standard/design-guidelines/member.md)  
- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)
