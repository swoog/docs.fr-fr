---
title: Conception d'événements
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- pre-events
- events [.NET Framework], design guidelines
- member design guidelines, events
- event handlers [.NET Framework], event design guidelines
- post-events
- signatures, event handling
ms.assetid: 67b3c6e2-6a8f-480d-a78f-ebeeaca1b95a
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b257da73d33fae54ef464e9dd69906316b87fd88
ms.sourcegitcommit: 2350a091ef6459f0fcfd894301242400374d8558
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/21/2018
ms.locfileid: "46540292"
---
# <a name="event-design"></a>Conception d'événements
Les événements sont le plus couramment utilisé formulaire des rappels (constructions qui permettent l’infrastructure d’appeler dans le code utilisateur). Autres mécanismes de rappel incluent les membres en prenant les délégués, les membres virtuels et basée sur l’interface de plug-ins. Données à partir des études de convivialité indiquent que la majorité des développeurs sont plus à l’aise avec les événements qu’ils sont à l’aide des autres méthodes de rappel. Les événements sont bien intégrées à Visual Studio et de nombreux langages.  
  
 Il est important de noter qu’il existe deux groupes d’événements : événements déclenchés avant un état des modifications système, appelé pré-événements et les événements déclenchés après un état change, appelés post événements. Voici un exemple d’un événement pre `Form.Closing`, qui est déclenché avant la fermeture d’un formulaire. Voici un exemple d’un post-événement `Form.Closed`, qui est déclenché après qu’un formulaire est fermé.  
  
 **✓ DO** utiliser le terme « r » pour les événements plutôt que « fire » ou « déclenche ».  
  
 **✓ DO** utiliser <xref:System.EventHandler%601?displayProperty=nameWithType> au lieu de créer manuellement les nouveaux délégués à utiliser en tant que gestionnaires d’événements.  
  
 **✓ CONSIDER** à l’aide d’une sous-classe de <xref:System.EventArgs> comme argument d’événement, sauf si vous êtes absolument que l’événement n’est jamais nécessaire de transporter des données à l’événement de gestion de la méthode, auquel cas vous pouvez utiliser la `EventArgs` taper directement.  
  
 Si vous envoyez un à l’aide de l’API `EventArgs` directement, vous ne serez jamais en mesure d’ajouter des données à effectuer avec l’événement sans perdre la compatibilité. Si vous utilisez une sous-classe, même si initialement vide, vous serez en mesure d’ajouter des propriétés à la sous-classe lorsque nécessaire.  
  
 **✓ DO** utiliser une méthode virtuelle protégée pour déclencher chaque événement. Cela s’applique uniquement aux événements non statiques sur des classes unsealed, pas pour les structs, les classes sealed ou des événements statiques.  
  
 L’objectif de la méthode est de fournir un moyen d’une classe dérivée gérer l’événement à l’aide d’un remplacement. Substitution est un moyen plus flexible, plus rapide et plus naturel pour gérer les événements de classe de base dans les classes dérivées. Par convention, le nom de la méthode doit commencer par « On » et être suivi par le nom de l’événement.  
  
 La classe dérivée peut choisissez de ne pas appeler l’implémentation de base de la méthode dans son remplacement. Face à cette situation en n’incluant ne pas de traitement dans la méthode qui est requise pour la classe de base fonctionne correctement.  
  
 **✓ DO** doit accepter un paramètre à la méthode protégée qui déclenche un événement.  
  
 Le paramètre doit être nommé `e` et doit être tapé sous forme de la classe d’argument d’événement.  
  
 **X DO NOT** passez la valeur null en tant que l’expéditeur lors du déclenchement d’un événement non statique.  
  
 **✓ DO** passez la valeur null en tant que l’expéditeur lors du déclenchement d’un événement statique.  
  
 **X DO NOT** passez la valeur null en tant que le paramètre de données d’événement lors du déclenchement d’un événement.  
  
 Vous devez passer `EventArgs.Empty` si vous ne souhaitez pas passer des données à la méthode de gestion d’événements. Les développeurs s’attendent à ce paramètre ne pas pour avoir la valeur null.  
  
 **✓ CONSIDER** le déclenchement d’événements de l’utilisateur final peut annuler. Cela s’applique uniquement aux pré-événements.  
  
 Utilisez <xref:System.ComponentModel.CancelEventArgs?displayProperty=nameWithType> ou sa sous-classe comme argument d’événement pour autoriser l’utilisateur final d’annuler des événements.  
  
### <a name="custom-event-handler-design"></a>Conception de gestionnaire d’événements personnalisés  
 Il existe des cas dans lesquels `EventHandler<T>` ne peut pas être utilisées, comme lorsque le framework doit fonctionner avec les versions antérieures du CLR, qui ne prenait pas en charge des génériques. Dans ce cas, vous devez concevoir et développer un délégué de gestionnaire d’événements personnalisé.  
  
 **✓ DO** utiliser un type de retour void pour les gestionnaires d’événements.  
  
 Un gestionnaire d’événements peut appeler plusieurs méthodes, éventuellement sur plusieurs objets de gestion d’événement. Si les méthodes de gestion des événements ont été autorisées pour retourner une valeur, il y aura plusieurs valeurs de retour pour chaque appel de l’événement.  
  
 **✓ DO** utiliser `object` en tant que le type du premier paramètre du Gestionnaire d’événements et l’appeler `sender`.  
  
 **✓ DO** utiliser <xref:System.EventArgs?displayProperty=nameWithType> ou sa sous-classe en tant que le type du deuxième paramètre du Gestionnaire d’événements et l’appeler `e`.  
  
 **X DO NOT** avoir plus de deux paramètres sur les gestionnaires d’événements.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson Education, Inc. et extrait de [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) par Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série sur le développement Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Instructions de conception des membres](../../../docs/standard/design-guidelines/member.md)  
- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)
