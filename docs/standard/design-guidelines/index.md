---
title: Règles de conception de .NET Framework
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- libraries, .NET Framework class library
- class library design guidelines [.NET Framework], about
- class library design guidelines [.NET Framework]
ms.assetid: 5fbcaf4f-ea2a-4d20-b0d6-e61dee202b4b
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: df2ccf3d778e26e16937554304ae847f624cfec0
ms.sourcegitcommit: 64f4baed249341e5bf64d1385bf48e3f2e1a0211
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/07/2018
ms.locfileid: "44085634"
---
# <a name="framework-design-guidelines"></a>Règles de conception de .NET Framework
Cette section fournit des instructions pour la conception de bibliothèques qui étendent et interagissent avec le .NET Framework. L’objectif est d’aider les concepteurs de bibliothèques à garantir la cohérence d’API et la facilité d’utilisation en fournissant un modèle de programmation unifié qui est indépendant du langage de programmation utilisé pour le développement. Nous vous recommandons de suivre ces instructions de conception lors du développement de classes et composants qui étendent .NET Framework. Conception de la bibliothèque incohérent avoir un impact négatif la productivité des développeurs et décourage adoption.  
  
 Les directives sont organisées en tant que recommandation simple avec les termes du contrat le préfixe `Do`, `Consider`, `Avoid`, et `Do not`. Ces instructions sont destinées à aider les concepteurs de bibliothèque de classes à comprendre les compromis entre différentes solutions. Il existe peut-être enfreindre bon design de bibliothèque que vous ces instructions de conception. Ce cas est rare, et il est important que vous avez une raison claire et intéressante pour votre décision.  
  
 Ces instructions sont extraites de l’ouvrage *Framework Design Guidelines : Conventions, les idiomes et les modèles pour les bibliothèques .NET réutilisable, 2nd Edition*, Krzysztof Cwalina et Brad Abrams.  
  
## <a name="in-this-section"></a>Dans cette section  
 [Directives de nommage](../../../docs/standard/design-guidelines/naming-guidelines.md)  
 Fournit des instructions pour nommer les assemblys, espaces de noms, types et membres dans les bibliothèques de classes.  
  
 [Instructions pour la conception des types](../../../docs/standard/design-guidelines/type.md)  
 Fournit des instructions pour l’utilisation des classes statiques et abstraites, des interfaces, des énumérations, des structures et autres types.  
  
 [Instructions de conception des membres](../../../docs/standard/design-guidelines/member.md)  
 Fournit des instructions pour la conception et à l’aide des propriétés, méthodes, constructeurs, champs, événements, opérateurs et paramètres.  
  
 [Conception en vue de l’extensibilité](../../../docs/standard/design-guidelines/designing-for-extensibility.md)  
 Mécanismes d’extensibilité tels que le sous-classement, à l’aide d’événements, les membres virtuels et les rappels et explique comment choisir les mécanismes qui répondent le mieux aux exigences de votre infrastructure.  
  
 [Instructions de conception pour les exceptions](../../../docs/standard/design-guidelines/exceptions.md)  
 Décrit les instructions de conception pour la conception, la levée et l’interception des exceptions.  
  
 [Indications relatives à l’utilisation](../../../docs/standard/design-guidelines/usage-guidelines.md)  
 Fournit des instructions pour l’utilisation des types courants tels que des tableaux, des attributs et des collections, prenant en charge la sérialisation et la surcharge des opérateurs d’égalité.  
  
 [Modèles de design courants](../../../docs/standard/design-guidelines/common-design-patterns.md)  
 Fournit des instructions pour le choix et l’implémentation des propriétés de dépendance et le modèle de suppression.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson Education, Inc. et extrait de [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) par Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série sur le développement Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Vue d’ensemble](../../../docs/framework/get-started/overview.md)  
- [Feuille de route pour le .NET Framework](https://msdn.microsoft.com/library/0b46b7c6-9163-4f99-8e58-0d1ee7da8c67)  
- [Guide de développement](../../../docs/framework/development-guide.md)
