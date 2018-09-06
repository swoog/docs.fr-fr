---
title: Instructions d’utilisation
ms.date: 03/30/2017
ms.technology: dotnet-standard
helpviewer_keywords:
- class library design guidelines [.NET Framework], usage guidelines
ms.assetid: 42215ffa-a099-4a26-b14e-fb2bdb6f95b7
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 04e44a6b58fd334b6a23e113922b980f69de627b
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43869864"
---
# <a name="usage-guidelines"></a>Instructions d’utilisation

Cette section contient des instructions sur l’utilisation de types courants dans les API accessible publiquement. Il porte sur l’utilisation directe de types de Framework (par exemple, les attributs de sérialisation) et de la surcharge des opérateurs courants intégrés.
  
Le <xref:System.IDisposable?displayProperty=nameWithType> interface n’est pas couverte dans cette section, mais est abordée dans le [modèle Dispose](../../../docs/standard/design-guidelines/dispose-pattern.md) section.

> [!NOTE]
> Pour les instructions et informations supplémentaires sur les autres commun, les types intégrés .NET Framework, consultez les rubriques de référence pour les éléments suivants : <xref:System.DateTime?displayProperty=nameWithType>, <xref:System.DateTimeOffset?displayProperty=nameWithType>, <xref:System.ICloneable?displayProperty=nameWithType>, <xref:System.IComparable%601?displayProperty=nameWithType>, <xref:System.IEquatable%601?displayProperty=nameWithType>, <xref:System.Nullable%601?displayProperty=nameWithType>, <xref:System.Object?displayProperty=nameWithType> , <xref:System.Uri?displayProperty=nameWithType>.

## <a name="in-this-section"></a>Dans cette section

[Tableaux](arrays.md)  
[Attributs](attributes.md)  
[Collections](guidelines-for-collections.md)  
[Sérialisation](serialization.md)  
[System.Xml, utilisation](system-xml-usage.md)  
[Opérateurs d’égalité](equality-operators.md)  

*Portions © 2005, 2009 Microsoft Corporation. Tous droits réservés.*

*Réimprimé avec l’autorisation de Pearson Education, Inc. et extrait de [Framework Design Guidelines: Conventions, Idioms, and Patterns for Reusable .NET Libraries, 2nd Edition](https://www.informit.com/store/framework-design-guidelines-conventions-idioms-and-9780321545619) par Krzysztof Cwalina et Brad Abrams, publié le 22 octobre 2008 par Addison-Wesley Professional dans le cadre de la série sur le développement Microsoft Windows.*
  
## <a name="see-also"></a>Voir aussi

- [Règles de conception de .NET Framework](../../../docs/standard/design-guidelines/index.md)
