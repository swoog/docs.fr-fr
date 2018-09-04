---
title: Outils .NET Core supplémentaires
description: Vue d’ensemble des outils supplémentaires qui prennent en charge et étendent les fonctionnalités de .NET Core.
author: mlacouture
ms.author: johalex
ms.date: 01/19/2018
ms.custom: mvc
ms.openlocfilehash: ba63ef6cdc092d06e267637112070e7cd5133a45
ms.sourcegitcommit: 2eceb05f1a5bb261291a1f6a91c5153727ac1c19
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/04/2018
ms.locfileid: "43511752"
---
# <a name="net-core-additional-tools"></a>Outils .NET Core supplémentaires

Cette section dresse une liste des outils qui prennent en charge et étendent les fonctionnalités de .NET Core, en plus des outils d’[interface de ligne de commande (CLI) .NET Core](..\tools\index.md).

## <a name="wcf-web-service-reference-toolwcf-web-service-reference-guidemd"></a>[Outil WCF Web Service Reference](wcf-web-service-reference-guide.md)

WCF (Windows Communication Foundation) Web Service Reference est un fournisseur de services connectés Visual Studio qui a fait son apparition dans [Visual Studio 2017 version 15.5](https://visualstudio.microsoft.com/news/releasenotes/vs2017-relnotes#WCFTools). Cet outil récupère les métadonnées d’un service web dans la solution actuelle sur un emplacement réseau ou dans un fichier WSDL, puis génère un fichier source compatible avec .NET Core, en définissant une classe proxy WCF avec des méthodes que vous pouvez utiliser pour accéder aux opérations du service web.

## <a name="wcf-dotnet-svcutil-tooldotnet-svcutil-guidemd"></a>[Outil dotnet-svcutil WCF](dotnet-svcutil-guide.md)

L’outil dotnet-svcutil WCF (Windows Communication Foundation) est un outil CLI .NET Core qui récupère les métadonnées d’un service web sur un emplacement réseau ou dans un fichier WSDL, puis génère un fichier source compatible avec .NET Core, en définissant une classe proxy WCF avec des méthodes que vous pouvez utiliser pour accéder aux opérations du service web. L’outil **dotnet-svcutil** est une option alternative au fournisseur de services connectés Visual Studio [**WCF Web Service Reference**](wcf-web-service-reference-guide.md) inclus dans Visual Studio 2017 v15.5. L’outil **dotnet-svcutil**, en tant qu’outil CLI .NET Core, est disponible sur les plateformes Linux, macOS et Windows.

## <a name="xml-serializer-generatorxml-serializer-generatormd"></a>[Générateur de sérialiseur XML](xml-serializer-generator.md)

Comme le [Générateur de sérialiseur XML (sgen.exe)](../../standard/serialization/xml-serializer-generator-tool-sgen-exe.md) pour le .NET Framework, le [package NuGet Microsoft.XmlSerializer.Generator](https://www.nuget.org/packages/Microsoft.XmlSerializer.Generator) est la solution pour les bibliothèques .NET Core et .NET Standard. Il crée un assembly de sérialisation XML pour les types contenus dans un assembly afin d’améliorer les performances de démarrage de la sérialisation XML pendant la sérialisation ou la désérialisation des objets de ces types avec <xref:System.Xml.Serialization.XmlSerializer>.