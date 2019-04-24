---
title: Charsets et marshaling – .NET
description: Découvrez l’impact des différentes valeurs du charset sur la façon dont .NET marshale les données en code natif.
author: jkoritzinsky
ms.author: jekoritz
ms.date: 01/18/2019
ms.openlocfilehash: f436bbbf435df07d242f9bf295b0264c4cfd5b3b
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59480844"
---
# <a name="charsets-and-marshalling"></a>Charsets et marshaling

La façon dont les valeurs `char` et les objets `string` et `System.Text.StringBuilder` sont marshalés dépend de la valeur du champ `CharSet` sur P/Invoke ou la structure. Pour définir le `CharSet` d’un P/Invoke, définissez le champ <xref:System.Runtime.InteropServices.DllImportAttribute.CharSet?displayProperty=nameWithType> lorsque vous déclarez votre P/Invoke. Pour définir le `CharSet` d’une structure, définissez le champ <xref:System.Runtime.InteropServices.StructLayoutAttribute.CharSet?displayProperty=nameWithType> sur votre déclaration struct. Lorsque ces champs d’attribut ne sont pas définis, c’est au compilateur du langage de déterminer quel `CharSet` utiliser. C# et VB utilisent par défaut le charset <xref:System.Runtime.InteropServices.CharSet.Ansi>.

Le tableau suivant présente la correspondance entre chaque charset et la représentation d’un caractère ou d’une chaîne après marshaling avec ce charset :

| CharSet | Windows            | Unix sur .NET Core 2.2 et les versions antérieures | Mono et Unix sur .NET Core 3.0 et les versions ultérieures |
|---------|--------------------|-----------------------------|------------------------------------------|
| Ansi    | `char` (ANSI)      | `char` (UTF-8)              | `char` (UTF-8)                           |
| Unicode | `wchar_t` (UTF-16) | `char16_t` (UTF-16)         | `char16_t` (UTF-16)                      |
| Auto    | `wchar_t` (UTF-16) | `char16_t` (UTF-16)         | `char` (UTF-8)                           |

Lorsque vous choisissez votre charset, renseignez-vous sur la représentation native attendue.
