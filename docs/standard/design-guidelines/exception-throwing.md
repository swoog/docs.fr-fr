---
title: Levée d'exceptions
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- exceptions, throwing
- explicitly throwing exceptions
- throwing exceptions, design guidelines
ms.assetid: 5388e02b-52f5-460e-a2b5-eeafe60eeebe
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9fbbe84811e3fa096b9e13c459143311bb75a198
ms.sourcegitcommit: c7f3e2e9d6ead6cc3acd0d66b10a251d0c66e59d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/09/2018
ms.locfileid: "44225147"
---
# <a name="exception-throwing"></a>Levée d'exceptions
Levée d’exceptions des indications décrites dans cette section nécessitent une bonne définition de la signification de l’échec d’exécution. Échec d’exécution se produit chaque fois qu’un membre ne peut pas qu’il a été conçu pour faire (ce que le nom du membre indique). Par exemple, si le `OpenFile` méthode ne peut pas retourner un handle de fichier ouvert à l’appelant, il est considéré comme un échec d’exécution.  
  
 La plupart des développeurs sont devenus à l’aise avec utilisation d’exceptions pour les erreurs d’utilisation telles que la division par zéro ou de références null. Dans le Framework, les exceptions sont utilisées pour toutes les conditions d’erreur, y compris les erreurs d’exécution.  
  
 **X DO NOT** codes d’erreur.  
  
 Les exceptions sont le moyen principal de signalement des erreurs dans les infrastructures.  
  
 **✓ DO** signale les échecs de l’exécution en levant des exceptions.  
  
 **✓ CONSIDER** mettre fin au processus en appelant `System.Environment.FailFast` (fonctionnalité de .NET Framework 2.0) au lieu de lever une exception si votre code rencontre une situation où il est risqué pour obtenir de l’exécution.  
  
 **X DO NOT** utiliser des exceptions pour le flux normal de contrôle, si possible.  
  
 À l’exception des défaillances du système et des opérations avec des conditions de concurrence potentielle, les concepteurs de framework doivent concevoir les API pour les utilisateurs peuvent écrire du code qui ne lève pas d’exceptions. Par exemple, vous pouvez fournir un moyen de vérifier les conditions préalables avant d’appeler un membre pour les utilisateurs peuvent écrire du code qui ne lève pas d’exceptions.  
  
 Le membre utilisé pour vérifier des conditions préalables d’un autre membre est souvent appelé un testeur, et le membre qui effectue réellement le travail est appelé un exécuteur.  
  
 Il existe des cas lorsque le modèle Doer peut avoir une surcharge de performances inacceptables. Dans ce cas, le modèle d’essayer d’analyser ce que l'on appelle doit être considéré comme (consultez [Exceptions et performances](../../../docs/standard/design-guidelines/exceptions-and-performance.md) pour plus d’informations).  
  
 **✓ CONSIDER** l’impact sur les performances de lever des exceptions. Taux de throw au-dessus de 100 par seconde sont susceptibles d’impacter les performances de la plupart des applications.  
  
 **✓ DO** document toutes les exceptions levées par les membres pouvant être appelés publiquement en raison d’une violation du membre de contrat (au lieu d’une défaillance du système) et les traitent en tant que partie de votre contrat.  
  
 Les exceptions qui font partie du contrat de ne doivent pas changer d’une version à l’autre (par exemple, type d’exception ne doit pas modifier, et de nouvelles exceptions ne doivent pas être ajoutées).  
  
 **X DO NOT** ont des membres publics qui peuvent lever ou non basées sur une option.  
  
 **X DO NOT** des membres publics de retournent des exceptions comme valeur de retour ou un `out` paramètre.  
  
 Retourner des exceptions à partir des API publiques, au lieu de lever les va à l’encontre de nombreux avantages de rapport d’erreurs basée sur l’exception.  
  
 **✓ CONSIDER** à l’aide des méthodes de générateur d’exceptions.  
  
 Il est courant pour lever l’exception même à partir de différents endroits. Pour éviter les excès de code, utilisez les méthodes d’assistance qui créent des exceptions et initialisent leurs propriétés.  
  
 En outre, les membres qui lèvent des exceptions ne reçoivent inline. Déplacement de l’instruction throw dans le générateur peut autoriser le membre permet d’être incorporée.  
  
 **X DO NOT** lever des exceptions à partir de blocs de filtre d’exception.  
  
 Lorsqu’un filtre d’exceptions lève une exception, l’exception est interceptée par le CLR, et le filtre retourne false. Ce comportement est indiscernable du filtre de l’exécution et en retournant la valeur false explicitement et est donc très difficile à déboguer.  
  
 **X AVOID** lever explicitement des exceptions à partir de blocs finally. Résultant de l’appel des méthodes qui lèvent les exceptions levées implicitement sont acceptables.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson Education, Inc. et extrait de [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) par Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série sur le développement Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)  
- [Instructions de conception pour les exceptions](../../../docs/standard/design-guidelines/exceptions.md)
