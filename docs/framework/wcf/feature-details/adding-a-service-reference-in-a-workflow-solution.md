---
title: Ajout d'une référence de service dans une solution de workflow
ms.date: 03/30/2017
ms.assetid: 83574cf3-9803-49bc-837f-432936dc9c76
ms.openlocfilehash: 8f1fa4604f1a1873c7063ec3c9dccf08bd0aa0ee
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54549039"
---
# <a name="adding-a-service-reference-in-a-workflow-solution"></a>Ajout d'une référence de service dans une solution de workflow

L'ajout d'une référence de service dans une application de workflow fonctionne de façon légèrement différente que dans une application WCF normale. Lorsque vous sélectionnez **Ajouter > Service référence** et spécifiez l’URL pour le service, les métadonnées sont téléchargées et des activités personnalisées sont générées pour vous permettre d’appeler le service WCF ou le service de workflow WCF vous avez ajouté une référence à. Après l'ajout d'une référence de service, régénérez la solution pour que les activités générées soient construites. Celles-ci vont ensuite apparaître dans la boîte à outils du concepteur de workflow. Notez toutefois que cela ne fonctionne que si vous ajoutez une référence de service dans une solution de workflow. Le webcast suivant montre comment ajouter une référence de service dans d’autres types de projets : [Appel d’un Service WCF à partir d’un flux de travail dans un projet Web](https://go.microsoft.com/fwlink/?LinkId=207725).

L'ajout de deux ou plus références de service aux services qui contiennent le même nom d'opération entraîne un problème. Les activités générées vont appeler uniquement la première opération de service. Pour contourner ce problème, il faut renommer les opérations de service avec des noms différents ou modifier le nom de la configuration de point de terminaison dans chaque activité générée.

## <a name="see-also"></a>Voir aussi

- [Services de workflow](../../../../docs/framework/wcf/feature-details/workflow-services.md)
- [Appel d’un Service WCF à partir d’un flux de travail dans un projet Web](https://go.microsoft.com/fwlink/?LinkId=207725)
