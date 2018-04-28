---
title: Informations de référence sur global.json
description: Consultez le schéma du fichier global.json, qui permet de définir la version des outils .NET Core.
author: blackdwarf
ms.author: mairaw
ms.date: 04/05/2017
ms.topic: conceptual
ms.prod: dotnet-core
ms.technology: dotnet-cli
ms.devlang: dotnet
ms.workload:
- dotnetcore
ms.openlocfilehash: ac53a899e76c99527f2670d0a6bed3f8cc6ce31f
ms.sourcegitcommit: 03ee570f6f528a7d23a4221dcb26a9498edbdf8c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2018
---
# <a name="globaljson-reference"></a><span data-ttu-id="9962a-103">Informations de référence sur global.json</span><span class="sxs-lookup"><span data-stu-id="9962a-103">global.json reference</span></span>

<span data-ttu-id="9962a-104">Le fichier *global.json* permet de sélectionner la version des outils .NET Core utilisée par le biais de la propriété `sdk`.</span><span class="sxs-lookup"><span data-stu-id="9962a-104">The *global.json* file allows selection of the .NET Core tools version being used through the `sdk` property.</span></span>

<span data-ttu-id="9962a-105">Les outils CLI .NET Core recherchent ce fichier dans le répertoire de travail actif (qui n’est pas forcément le même que le répertoire du projet) ou dans l’un de ses répertoires parents.</span><span class="sxs-lookup"><span data-stu-id="9962a-105">.NET Core CLI tools look for this file in the current working directory (which isn't necessarily the same as the project directory) or one of its parent directories.</span></span>

## <a name="sdk"></a><span data-ttu-id="9962a-106">sdk</span><span class="sxs-lookup"><span data-stu-id="9962a-106">sdk</span></span>
<span data-ttu-id="9962a-107">Type : object</span><span class="sxs-lookup"><span data-stu-id="9962a-107">Type: Object</span></span>

<span data-ttu-id="9962a-108">Spécifie des informations sur le SDK.</span><span class="sxs-lookup"><span data-stu-id="9962a-108">Specifies information about the SDK.</span></span>

### <a name="version"></a><span data-ttu-id="9962a-109">version</span><span class="sxs-lookup"><span data-stu-id="9962a-109">version</span></span>
<span data-ttu-id="9962a-110">Type : chaîne</span><span class="sxs-lookup"><span data-stu-id="9962a-110">Type: String</span></span>

<span data-ttu-id="9962a-111">Version du SDK à utiliser.</span><span class="sxs-lookup"><span data-stu-id="9962a-111">The version of the SDK to use.</span></span>

<span data-ttu-id="9962a-112">Exemple :</span><span class="sxs-lookup"><span data-stu-id="9962a-112">For example:</span></span>

```json
{
  "sdk": {
    "version": "1.0.0-preview2-003121"
  }
}
```
