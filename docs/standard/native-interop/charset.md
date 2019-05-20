---
title: Charsets et marshaling - .NET
description: Découvrez l’impact des différentes valeurs du charset sur la façon dont .NET marshale les données en code natif.
author: jkoritzinsky
ms.author: jekoritz
ms.date: 01/18/2019
ms.openlocfilehash: c50c58ad639b1efb29c13e5124fe3c32e8af96fc
ms.sourcegitcommit: ca2ca60e6f5ea327f164be7ce26d9599e0f85fe4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/06/2019
ms.locfileid: "65063339"
---
# <a name="charsets-and-marshaling"></a>Charsets et marshaling

La façon dont les valeurs `char` et les objets `string` et `System.Text.StringBuilder` sont marshalés dépend de la valeur du champ `CharSet` sur P/Invoke ou la structure. Pour définir le `CharSet` d’un P/Invoke, définissez le champ <xref:System.Runtime.InteropServices.DllImportAttribute.CharSet?displayProperty=nameWithType> lorsque vous déclarez votre P/Invoke. Pour définir le `CharSet` d’une structure, définissez le champ <xref:System.Runtime.InteropServices.StructLayoutAttribute.CharSet?displayProperty=nameWithType> sur votre déclaration struct. Lorsque ces champs d’attribut ne sont pas définis, c’est au compilateur du langage de déterminer quel `CharSet` utiliser. C# et VB utilisent par défaut le charset <xref:System.Runtime.InteropServices.CharSet.Ansi>.

Le tableau suivant présente la correspondance entre chaque charset et la représentation d’un caractère ou d’une chaîne après marshaling avec ce charset :

| Valeur`CharSet`  | Windows            | .NET Core 2.2 et antérieur sur Unix | .NET Core 3.0 et ultérieur et Mono sur Unix |
|-----------------|--------------------|-----------------------------------|------------------------------------------|
| Ansi            | `char` (ANSI)      | `char` (UTF-8)                    | `char` (UTF-8)                           |
| Unicode         | `wchar_t` (UTF-16) | `char16_t` (UTF-16)               | `char16_t` (UTF-16)                      |
| Auto            | `wchar_t` (UTF-16) | `char16_t` (UTF-16)               | `char` (UTF-8)                           |

Lorsque vous choisissez votre charset, renseignez-vous sur la représentation native attendue.
