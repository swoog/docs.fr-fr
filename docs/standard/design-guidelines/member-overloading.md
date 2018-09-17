---
title: Surcharge de membre
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- default arguments
- members [.NET Framework], overloaded
- member design guidelines [.NET Framework], overloading
- overloaded members
- signatures, members
ms.assetid: 964ba19e-8b94-4b5b-b1e3-5a0b531a0bb1
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 2127497d294cbfd4e1bb24d033f432378627ff13
ms.sourcegitcommit: 5bbfe34a9a14e4ccb22367e57b57585c208cf757
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/17/2018
ms.locfileid: "45964200"
---
# <a name="member-overloading"></a>Surcharge de membre
Surcharge de membre signifie que la création de deux ou plusieurs membres sur le même type qui diffèrent uniquement par le nombre ou le type de paramètres mais qui ont le même nom. Par exemple, dans la commande suivante, le `WriteLine` méthode est surchargée :  
  
```  
public static class Console {  
    public void WriteLine();  
    public void WriteLine(string value);  
    public void WriteLine(bool value);  
    ...  
}  
```  
  
 Uniquement les méthodes, les constructeurs et les propriétés indexées pouvant avoir des paramètres, seuls les membres peuvent être surchargés.  
  
 La surcharge est une des techniques plus importantes pour améliorer la facilité d’utilisation, la productivité et la lisibilité des bibliothèques réutilisables. La surcharge sur le nombre de paramètres rend possible fournir des versions plus simples de constructeurs et méthodes. La surcharge sur le type de paramètre rend possible d’utiliser le même nom de membre pour effectuer des opérations identiques sur un ensemble sélectionné de différents types de membres.  
  
 **✓ DO** essayez d’utiliser des noms de paramètres descriptifs pour indiquer la valeur par défaut utilisée par les surcharges plus courts.  
  
 **X AVOID** Variant de façon arbitraire les noms de paramètres dans les surcharges. Si un paramètre d’une surcharge représente la même entrée en tant que paramètre dans une autre surcharge, les paramètres doivent avoir le même nom.  
  
 **X AVOID** incohérent dans l’ordre des paramètres de surcharge membres. Paramètres portant le même nom doivent apparaître dans la même position dans toutes les surcharges.  
  
 **✓ DO** créer uniquement la surcharge la plus longue virtuelle (si l’extensibilité est requise). Les surcharges plus courtes doivent appeler simplement une surcharge plus longue.  
  
 **X DO NOT** utiliser `ref` ou `out` modificateurs pour surcharger les membres.  
  
 Certains langages ne peuvent pas résoudre les appels aux surcharges comme suit. En outre, ces surcharges ont généralement une sémantique complètement différente et ne doivent pas être surcharges mais les deux méthodes distinctes à la place.  
  
 **X DO NOT** ont des surcharges avec des paramètres à la même position et les types semblables, mais avec une sémantique différente.  
  
 **✓ DO** autoriser `null` à passer les arguments facultatifs.  
  
 **✓ DO** utiliser membre surcharge plutôt que de définir des membres avec des arguments par défaut.  
  
 Arguments par défaut ne sont pas compatibles CLS.  
  
 *Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*  
  
 *Réimprimé avec l’autorisation de Pearson Education, Inc. et extrait de [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) par Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série sur le développement Microsoft Windows.*  
  
## <a name="see-also"></a>Voir aussi

- [Instructions de conception des membres](../../../docs/standard/design-guidelines/member.md)  
- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)
