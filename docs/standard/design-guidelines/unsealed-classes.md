---
title: Classes unsealed
ms.date: 10/22/2008
ms.technology: dotnet-standard
helpviewer_keywords:
- classes [.NET Framework], unsealed
- unsealed classes
- inheritance, classes
ms.assetid: 9a3bd505-90f5-4053-9f0d-3cf5fa3d3ebf
author: KrzysztofCwalina
ms.openlocfilehash: d7174de7ddf062b829672e04952c1010fcb74058
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61778792"
---
# <a name="unsealed-classes"></a>Classes unsealed
Les classes sealed ne peut pas être héritées, et ils empêchent d’extensibilité. En revanche, les classes qui peuvent être héritées sont appelées des classes non scellés.  
  
 **✓ CONSIDER** à l’aide des classes unsealed sans aucune ajouté des membres virtuels ou protégés comme un excellent moyen de fournir un peu coûteux encore apprécié extensibilité à une infrastructure.  
  
 Les développeurs souhaitent souvent hériter de classes unsealed afin d’ajouter des membres de commodité telles que les constructeurs personnalisés, les nouvelles méthodes ou les surcharges de méthode. Par exemple, `System.Messaging.MessageQueue` est non scellé et permet ainsi aux utilisateurs de créer des files d’attente personnalisées de cette valeur par défaut pour un chemin d’accès de la file d’attente particulière ou pour ajouter des méthodes personnalisées qui simplifient l’API pour des scénarios spécifiques.  
  
 Les classes sont non scellés par défaut dans les langages de programmation de plus, et c’est aussi la valeur par défaut recommandée pour la plupart des classes dans les infrastructures. L’extensibilité offerte par les types unsealed est très appréciés par les utilisateurs du framework et relativement peu coûteux fournir en raison des coûts de test relativement peu associées aux types non scellés.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson éducation, Inc. à partir de [instructions de conception Framework : Conventions, les idiomes et les modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement de Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)
- [Conception en vue de l’extensibilité](../../../docs/standard/design-guidelines/designing-for-extensibility.md)
- [Scellement](../../../docs/standard/design-guidelines/sealing.md)
