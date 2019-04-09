---
title: Planification des performances des applications
ms.date: 03/30/2017
helpviewer_keywords:
- applications [WPF], optimizing
- WPF application [WPF], optimizing
ms.assetid: c91bd0c5-a193-46ff-9da1-eb7a3a76a3b3
ms.openlocfilehash: 70dda68112d47d3e5a0609a5df7696920477c698
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59210202"
---
# <a name="planning-for-application-performance"></a>Planification des performances des applications
La réussite de vos objectifs de performances dépend du degré de l’élaboration de votre stratégie de performances. La planification est la première étape dans le développement de tous les produits. Cette rubrique décrit quelques règles très simples pour le développement d’une stratégie de bonnes performances.  
  
## <a name="think-in-terms-of-scenarios"></a>Pensez en termes de scénarios  
 Scénarios peuvent vous aider à vous concentrer sur les composants critiques de votre application. Scénarios sont généralement dérivées de vos clients, ainsi que les produits concurrents. Toujours étudier vos clients et découvrez ce qui a réellement attirés sur votre produit et vos concurrents. Commentaires de vos clients peuvent vous aider à déterminer le scénario principal de votre application. Par exemple, si vous concevez un composant qui sera utilisé au démarrage, il est probable que le composant sera appelé qu’une seule fois, au démarrage de l’application. Temps de démarrage devient votre scénario clé. Autres exemples de scénarios clés peut être de la fréquence d’images souhaitée pour les séquences d’animation, ou à la valeur maximale autorisée pour l’application de jeu de travail.  
  
## <a name="define-goals"></a>Définir des objectifs  
 Objectifs de vous aident à déterminer si une application s’exécute plus rapidement ou plus lentement. Vous devez définir des objectifs pour tous vos scénarios. Tous les objectifs de performances que vous définissez doivent être basées sur les attentes de vos clients. Il peut être difficile de performances de jeu cycle des objectifs très tôt dans le développement d’applications, lorsqu’il existe toujours des nombreux problèmes non résolus. Toutefois, il est préférable de définir un objectif initial et réviser ensuite que ne pas avoir un objectif du tout.  
  
## <a name="understand-your-platform"></a>Comprendre votre plateforme  
 Toujours conserver le cycle de mesure, investigation et ajustement/correction pendant le cycle de développement de votre application. À partir du début à la fin du cycle de développement, vous devez mesurer les performances de votre application dans un environnement fiable et stable. Vous devez éviter les variations provoquées par des facteurs externes. Par exemple, lorsque vous testez les performances, vous devez désactiver la protection antivirus ou une mise à jour automatique, telles que SMS, pour ne pas affecter les performances des résultats de test. Une fois que vous avez mesuré les performances de votre application, vous devez identifier les modifications qui entraîneront des améliorations plus importantes. Une fois que vous avez modifié votre application, puis recommencez le cycle.  
  
## <a name="make-performance-tuning-an-iterative-process"></a>Un processus itératif de réglage des performances  
 Vous devez connaître le coût relatif de chaque fonctionnalité, que vous allez utiliser. Par exemple, l’utilisation de la réflexion dans Microsoft .NET Framework est généralement gourmande en ressources informatiques, de performances et vous devez utiliser judicieusement. Cela ne signifie pas éviter l’utilisation de la réflexion, uniquement que vous devez être prudent afin d’équilibrer les exigences de performances de votre application avec les exigences de performance des fonctionnalités que vous utilisez.  
  
## <a name="build-towards-graphical-richness"></a>Richesse graphique  
 Une technique clé pour la création d’une approche évolutive vers la réalisation des [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] des performances des applications consiste à créer richesse graphique et la complexité. Toujours commencer par en utilisant les ressources d’intensif de performances moindres pour atteindre vos objectifs de scénario. Une fois que vous atteindre ces objectifs, richesse graphique à l’aide de plus de fonctionnalités exigeantes, toujours vos objectifs en n’oubliant pas. N’oubliez pas, [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] est une plateforme riche et fournit de puissantes fonctionnalités graphiques. À l’aide de fonctionnalités exigeantes sans prendre en considération peut avoir un impact négatif sur les performances de votre application globale.  
  
 [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] les contrôles sont par nature extensibles en permettant la personnalisation de la poussée de leur apparence, sans modification de leur comportement de contrôle. En tirant parti des styles, des modèles de données et des modèles de contrôle, vous pouvez créer et évoluer un personnalisable [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] qui s’adapte à vos exigences de performances.  
  
## <a name="see-also"></a>Voir aussi

- [Optimisation des performances des applications WPF](optimizing-wpf-application-performance.md)
- [Tirer parti du matériel](optimizing-performance-taking-advantage-of-hardware.md)
- [Disposition et conception](optimizing-performance-layout-and-design.md)
- [Graphisme 2D et acquisition d’images](optimizing-performance-2d-graphics-and-imaging.md)
- [Comportement de l’objet](optimizing-performance-object-behavior.md)
- [Ressources d’application](optimizing-performance-application-resources.md)
- [Texte](optimizing-performance-text.md)
- [Liaison de données](optimizing-performance-data-binding.md)
- [Autres recommandations relatives aux performances](optimizing-performance-other-recommendations.md)
