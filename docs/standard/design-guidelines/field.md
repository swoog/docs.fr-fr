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
ms.openlocfilehash: 2d47934c3fed17f75a97ef5da0397c6ceba53d68
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33571111"
---
# <a name="field-design"></a>Conception de champs
Le principe d’encapsulation est un des notions plus importantes dans la conception orientée objet. Ce principe stipule que les données stockées à l’intérieur d’un objet doivent être accessibles uniquement à cet objet.  
  
 Une méthode utile pour interpréter le principe est à dire qu’un type doit être conçu afin que les modifications aux champs de ce type (modification du nom ou type) peuvent être apportées sans rupture du code autre que pour les membres du type. Cette interprétation implique immédiatement que tous les champs doivent être privées.  
  
 Nous exclure constantes et statiques des champs en lecture seule de cette restriction stricte, car ces champs, presque par définition, ne sont jamais tenus à modifier.  
  
 **X ne sont pas** contiennent des champs d’instance qui sont publics ou protégés.  
  
 Vous devez fournir des propriétés pour accéder à des champs au lieu de les rendre publics ou protégés.  
  
 **✓ FAIRE** utiliser les champs constants pour les constantes qui ne changent pas.  
  
 Le compilateur augmente les valeurs des champs const directement dans le code appelant. Par conséquent, les valeurs const ne peuvent jamais être modifiées sans risque de rupture de compatibilité.  
  
 **✓ FAIRE** utiliser statique public `readonly` champs pour les instances d’objet prédéfinies.  
  
 S’il existe des instances prédéfinies du type, déclarez les champs statiques en lecture seule comme publics du type lui-même.  
  
 **X ne sont pas** affecter des instances de types mutables à `readonly` champs.  
  
 Un type mutable est un type avec des instances qui peuvent être modifiées une fois qu’ils sont instanciés. Par exemple, les flux, la plupart des collections et tableaux sont des types mutables, mais <xref:System.Int32?displayProperty=nameWithType>, <xref:System.Uri?displayProperty=nameWithType>, et <xref:System.String?displayProperty=nameWithType> sont toutes immuables. Le modificateur en lecture seule sur un champ de type référence empêche l’instance stockée dans le champ ne soit pas remplacé, mais il n’empêche pas les données d’instance du champ d’être modifié en appelant des membres modification de l’instance.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimées avec l’autorisation de Pearson éducation, Inc. à partir de [règles de conception d’infrastructure : Conventions, idiomes et des modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi  
 [Instructions de conception des membres](../../../docs/standard/design-guidelines/member.md)  
 [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)
