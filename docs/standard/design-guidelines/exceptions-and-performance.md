---
title: Exceptions et performances
ms.date: 10/22/2008
ms.technology: dotnet-standard
helpviewer_keywords:
- tester-doer pattern
- TryParse pattern
- exceptions, throwing
- exceptions, performance
- throwing exceptions, performance
ms.assetid: 3ad6aad9-08e6-4232-b336-0e301f2493e6
author: KrzysztofCwalina
ms.openlocfilehash: f9fe3045d8bd8b4d625c5cd49bc18574ebb740de
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54707724"
---
# <a name="exceptions-and-performance"></a>Exceptions et performances
Un problème courant lié aux exceptions est que si les exceptions sont utilisées pour le code qui échoue régulièrement, les performances de l’implémentation sera inacceptables. Il s’agit d’une inquiétude. Lorsqu’un membre lève une exception, ses performances peuvent être beaucoup plus lents. Toutefois, il est possible d’obtenir de bonnes performances tout en respectant strictement les instructions de l’exception qui interdisent l’utilisation de codes d’erreur. Deux modèles décrits dans cette section proposent des solutions pour ce faire.  
  
 **X DO NOT** utiliser des codes d’erreur en raison de problèmes qu’exceptions peuvent affecter négativement les performances.  
  
 Pour améliorer les performances, il est possible d’utiliser le modèle Doer ou le modèle d’essayer d’analyser, décrites dans les deux sections suivantes.  
  
## <a name="tester-doer-pattern"></a>Tester-Doer (modèle)  
 Parfois, les performances d’un membre de la levée d’exceptions peuvent être améliorées en divisant le membre en deux. Examinons le <xref:System.Collections.Generic.ICollection%601.Add%2A> méthode de la <xref:System.Collections.Generic.ICollection%601> interface.  
  
```  
ICollection<int> numbers = ...   
numbers.Add(1);  
```  
  
 La méthode `Add` lève une exception si la collection est en lecture seule. Cela peut être un problème de performances dans les scénarios où l’appel de méthode est censé échouent souvent. Un des moyens d’atténuer le problème consiste à vérifier si la collection est accessible en écriture avant d’essayer d’ajouter une valeur.  
  
```  
ICollection<int> numbers = ...   
...  
if(!numbers.IsReadOnly){  
    numbers.Add(1);  
}  
```  
  
 Le membre utilisé pour tester une condition qui, dans notre exemple, est la propriété `IsReadOnly`, est appelé par le testeur. Le membre utilisé pour effectuer une opération potentiellement levant, le `Add` méthode dans notre exemple, est appelé à l’exécuteur.  
  
 **✓ CONSIDER** le modèle utilisateur testeur pour les membres qui peuvent lever des exceptions en commun des scénarios pour éviter les problèmes de performances liés aux exceptions.  
  
## <a name="try-parse-pattern"></a>Modèle d’analyse de try  
 Pour les API extrêmement sensibles aux performances, un modèle encore plus rapide que le testeur-Doer (modèle) décrit dans la section précédente doit être utilisé. Le modèle appelle pour ajuster le nom de membre pour effectuer un test bien défini cas une partie de la sémantique de membre. Par exemple, <xref:System.DateTime> définit un <xref:System.DateTime.Parse%2A> méthode qui lève une exception en cas de l’analyse d’une chaîne. Il définit également un correspondant <xref:System.DateTime.TryParse%2A> méthode qui tente d’analyser, mais retourne false si l’analyse échoue et retourne le résultat d’une analyse réussie en utilisant un `out` paramètre.  
  
```  
public struct DateTime {  
    public static DateTime Parse(string dateTime){   
        ...   
    }  
    public static bool TryParse(string dateTime, out DateTime result){  
        ...  
    }  
}  
```  
  
 Lorsque vous utilisez ce modèle, il est important de définir les fonctionnalités de try en termes stricts. Si le membre échoue pour une raison quelconque autre que la tentative de bien définie, le membre doit lève toujours une exception correspondante.  
  
 **✓ CONSIDER** le modèle d’analyse de Try pour les membres qui peuvent lever des exceptions en commun des scénarios pour éviter les problèmes de performances liés aux exceptions.  
  
 **✓ DO** utilisent le préfixe « Try » et la valeur booléenne de type de retour pour les méthodes d’implémentation de ce schéma.  
  
 **✓ DO** fournissent un membre levant des exceptions pour chaque membre de l’utilisation du modèle d’analyse de Try.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson éducation, Inc. à partir de [instructions de conception Framework : Conventions, les idiomes et les modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement de Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)
- [Instructions de conception pour les exceptions](../../../docs/standard/design-guidelines/exceptions.md)
