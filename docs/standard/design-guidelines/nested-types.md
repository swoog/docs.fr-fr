---
title: Types imbriqués
ms.date: 10/22/2008
ms.technology: dotnet-standard
helpviewer_keywords:
- types, nested
- public nested types
- type design guidelines, nested types
- nested types
- members [.NET Framework], type
- class library design guidelines [.NET Framework], nested types
ms.assetid: 12feb7f0-b793-4d96-b090-42d6473bab8c
author: KrzysztofCwalina
ms.openlocfilehash: 7e5fe66106ad34e88bbf435794a08a159c045b02
ms.sourcegitcommit: ccd8c36b0d74d99291d41aceb14cf98d74dc9d2b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2018
ms.locfileid: "53148874"
---
# <a name="nested-types"></a>Types imbriqués
Un type imbriqué est un type défini dans l’étendue d’un autre type, qui est appelé le type englobant. Un type imbriqué a accès à tous les membres de son type englobant. Par exemple, il a accès aux champs privés définis dans le type englobant et protégés des champs définis dans tous les ascendants du type englobant.  
  
 En règle générale, les types imbriqués doivent être utilisés avec parcimonie. et ce, pour plusieurs raisons. Certains développeurs ne sont pas entièrement familiarisés avec le concept. Ces développeurs peuvent, par exemple, avoir des problèmes avec la syntaxe de déclaration de variables des types imbriqués. Les types imbriqués sont également très étroitement avec leurs types englobants et par conséquent ne sont pas adaptées à des types à usage général.  
  
 Les types imbriqués sont mieux adaptés à la modélisation des détails d’implémentation de leurs types englobants. L’utilisateur final doivent rarement avoir à déclarer des variables d’un type imbriqué et presque jamais doit avoir instancier explicitement les types imbriqués. Par exemple, l’énumérateur d’une collection peut être un type imbriqué de cette collection. En général, les énumérateurs sont instanciés par leur type englobant et nombreux langages prenant en charge l’instruction foreach, variables de l’énumérateur doivent rarement être déclaré par l’utilisateur final.  
  
 **✓ DO** utilisez des types imbriqués lorsque la relation entre le type imbriqué et son type externe est telle que sémantique de l’accessibilité des membres est souhaitable.  
  
 **X DO NOT** utiliser les types imbriqués publics en tant qu’un regroupement logique construire ; utilisez des espaces de noms pour ce.  
  
 **X AVOID** exposées publiquement des types imbriqués. La seule exception à cela est que si les variables du type imbriqué doivent être déclarées que dans les scénarios rares comme sous-classement ou d’autres scénarios de personnalisation avancée.  
  
 **X DO NOT** utilisez des types imbriqués, si le type est susceptible d’être référencés en dehors du type conteneur.  
  
 Par exemple, un enum passé à une méthode définie sur une classe ne doit pas être défini comme un type imbriqué dans la classe.  
  
 **X DO NOT** utilisez des types imbriqués s’ils doivent être instancié par le code client.  Si un type a un constructeur public, il ne doit probablement pas être imbriqué.  
  
 Si un type peut être instancié, il semble que pour indiquer le type a un lieu dans le cadre de son propre (vous pouvez créez-le, fonctionnent avec lui et détruire sans passer par le type externe) et ne doivent donc pas être imbriquées. Types internes ne doivent pas être réutilisés largement en dehors du type externe sans aucune relation que ce soit pour le type externe.  
  
 **X DO NOT** définir un type imbriqué en tant que membre d’une interface. De nombreux langages ne gèrent pas une telle construction.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson éducation, Inc. à partir de [instructions de conception Framework : Conventions, les idiomes et les modèles pour les bibliothèques .NET réutilisable, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série de développement de Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Instructions pour la conception des types](../../../docs/standard/design-guidelines/type.md)  
- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)
