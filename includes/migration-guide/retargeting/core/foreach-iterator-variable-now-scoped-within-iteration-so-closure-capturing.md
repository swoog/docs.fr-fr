---
ms.openlocfilehash: 1805c26f1eff46719f30de8a14ca6d35f01948a6
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59234757"
---
### <a name="foreach-iterator-variable-is-now-scoped-within-the-iteration-so-closure-capturing-semantics-are-different-in-c5"></a>La variable d’itérateur foreach est désormais délimitée au sein de l’itération. La sémantique de capture de clôture est donc différente (en C# 5)

|   |   |
|---|---|
|Détails|À compter de C# 5 (Visual Studio 2012), les variables d’itérateur <code>foreach</code> sont délimitées au sein de l’itération. Cela peut provoquer des arrêts d’exécution si le code dépendait du fait que les variables ne soient pas incluses dans la clôture de <code>foreach</code>. Les conséquences de ce changement sont qu’une variable d’itérateur passée à un délégué est considérée comme la valeur qu’elle a au moment où le délégué est créé, plutôt que comme la valeur qu’elle a au moment où le délégué est appelé.|
|Suggestion|Dans l’idéal, le code doit être mis à jour pour prévoir ce nouveau comportement du compilateur. Si vous avez besoin de l’ancienne sémantique, la variable d’itérateur peut être remplacée par une autre variable placée explicitement en dehors de la portée de la boucle.|
|Portée|Majeur|
|Version|4.5|
|Type|Reciblage|
