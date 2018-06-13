---
title: Informations de référence sur global.json
description: Consultez le schéma du fichier global.json, qui permet de définir la version des outils .NET Core.
author: blackdwarf
ms.author: mairaw
ms.date: 04/05/2017
ms.openlocfilehash: 7479774c7b9cdda233cf32d791c16e7fc6d733a8
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33209968"
---
# <a name="globaljson-reference"></a>Informations de référence sur global.json

Le fichier *global.json* permet de sélectionner la version des outils .NET Core utilisée par le biais de la propriété `sdk`.

Les outils CLI .NET Core recherchent ce fichier dans le répertoire de travail actif (qui n’est pas forcément le même que le répertoire du projet) ou dans l’un de ses répertoires parents.

## <a name="sdk"></a>sdk
Type : object

Spécifie des informations sur le SDK.

### <a name="version"></a>version
Type : chaîne

Version du SDK à utiliser.

Exemple :

```json
{
  "sdk": {
    "version": "1.0.0-preview2-003121"
  }
}
```
