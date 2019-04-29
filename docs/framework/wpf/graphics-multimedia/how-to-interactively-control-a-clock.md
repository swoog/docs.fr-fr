---
title: 'Procédure : Contrôler une horloge de façon interactive'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- controlling clocks interactively [WPF]
- clocks [WPF], controlling interactively
ms.assetid: d0b520e0-2f18-4cef-977f-2909e709548a
ms.openlocfilehash: 05989b6a03e03fb5723a70c9c36d5e32f9117049
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61947236"
---
# <a name="how-to-interactively-control-a-clock"></a>Procédure : Contrôler une horloge de façon interactive
Un <xref:System.Windows.Media.Animation.Clock> l’objet <xref:System.Windows.Media.Animation.ClockController> propriété vous permet de manière interactive Démarrer, suspendre, reprendre, rechercher, avancer l’horloge à sa période de remplissage et arrêter l’horloge. Que l’horloge racine d’arborescence de minutage peut être contrôlée de manière interactive.  
  
> [!NOTE]
>  Il existe d’autres façons de manière interactive des animations de contrôle qui ne nécessitent pas de travailler directement avec les horloges : vous pouvez également utiliser des tables de montage séquentiel. Les storyboards sont pris en charge dans le balisage et code. Pour obtenir un exemple, consultez [animer une propriété à l’aide d’un Storyboard](how-to-animate-a-property-by-using-a-storyboard.md) ou [vue d’ensemble de l’Animation](animation-overview.md).  
  
 Dans l’exemple suivant, plusieurs boutons sont utilisés pour contrôler une horloge d’animation de manière interactive.  
  
## <a name="example"></a>Exemple  
 [!code-csharp[timingbehaviors_procedural_snip#GraphicsMMClockControllerExample](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_procedural_snip/CSharp/ClockControllerExample.cs#graphicsmmclockcontrollerexample)]
 [!code-vb[timingbehaviors_procedural_snip#GraphicsMMClockControllerExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/timingbehaviors_procedural_snip/visualbasic/clockcontrollerexample.vb#graphicsmmclockcontrollerexample)]  
  
## <a name="see-also"></a>Voir aussi

- [Animer une propriété à l’aide d’une table de montage séquentiel](how-to-animate-a-property-by-using-a-storyboard.md)
- [Vue d’ensemble de l’animation](animation-overview.md)
