---
title: 'Optimisation des performances : Ressources d’application'
ms.date: 03/30/2017
helpviewer_keywords:
- application resources [WPF], performance
- resources [WPF], performance
- static resources [WPF]
- sharing resources [WPF]
- brushes [WPF], performance
- sharing brushes without copying [WPF]
ms.assetid: 62b88488-c08e-4804-b7de-a1c34fbe929c
ms.openlocfilehash: 362d0f0fd3282365e5e05dcd43c49a9fd2ddc9a7
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59139423"
---
# <a name="optimizing-performance-application-resources"></a>Optimisation des performances : Ressources d’application
[!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] vous permet de partager des ressources d’application afin que vous pouvez prendre en charge une apparence cohérente ou un comportement à travers des éléments similaires type. Cette rubrique fournit quelques recommandations dans ce domaine qui peut vous aider à améliorent les performances de vos applications.  
  
 Pour plus d’informations sur les ressources, consultez la page [Ressources XAML](xaml-resources.md).  
  
## <a name="sharing-resources"></a>Partage de ressources  
 Si votre application utilise des contrôles personnalisés et définit des ressources dans un <xref:System.Windows.ResourceDictionary> (ou nœud de ressources de XAML), il est recommandé que vous définissiez les ressources sur le <xref:System.Windows.Application> ou <xref:System.Windows.Window> au niveau de l’objet, ou les définir dans le thème par défaut pour le contrôles personnalisés. Définition des ressources dans un contrôle personnalisé <xref:System.Windows.ResourceDictionary> impose un impact sur les performances pour chaque instance de ce contrôle. Par exemple, si vous avez des opérations exigeantes en performances pinceau définies en tant que partie de la définition de ressource d’un contrôle personnalisé et le nombre d’instances du contrôle personnalisé, plage de travail de l’application augmente considérablement.  
  
 Pour illustrer ce point, considérez les points suivants. Supposons que vous développez un jeu de carte à l’aide [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]. Pour la plupart des jeux de cartes, vous avez besoin de 52 cartes avec 52 faces différentes. Vous décidez d’implémenter un contrôle personnalisé de carte et vous définissez 52 pinceaux (chacun représentant une face de carte) dans les ressources de votre carte de contrôle personnalisé. Dans votre application principale, vous créez initialement 52 instances de ce contrôle personnalisé de carte. Chaque instance de la carte de contrôle personnalisé génère 52 instances de <xref:System.Windows.Media.Brush> objets, ce qui vous donne un total de 52 * 52 <xref:System.Windows.Media.Brush> objets dans votre application. En déplaçant les pinceaux hors les ressources de contrôle personnalisé de carte à la <xref:System.Windows.Application> ou <xref:System.Windows.Window> au niveau objet, ou en les définissant dans le thème par défaut pour le contrôle personnalisé, vous réduisez la plage de travail de l’application, puisque vous partagez maintenant les 52 pinceaux parmi 52 d’instances de la carte de contrôle.  
  
## <a name="sharing-a-brush-without-copying"></a>Partage d’un pinceau sans copier  
 Si vous avez plusieurs éléments en utilisant le même <xref:System.Windows.Media.Brush> de l’objet, définissez le pinceau en tant que ressource et référencer, plutôt que de définir le pinceau inline dans [!INCLUDE[TLA#tla_titlexaml](../../../../includes/tlasharptla-titlexaml-md.md)]. Cette méthode crée une instance et la réutiliser, tandis que la définition de pinceaux inline dans [!INCLUDE[TLA#tla_titlexaml](../../../../includes/tlasharptla-titlexaml-md.md)] crée une nouvelle instance pour chaque élément.  
  
 L’exemple de balisage suivant illustre ce point :  
  
 [!code-xaml[Performance#PerformanceSnippet7](~/samples/snippets/csharp/VS_Snippets_Wpf/Performance/CSharp/BrushResource.xaml#performancesnippet7)]  
  
## <a name="use-static-resources-when-possible"></a>Utiliser des ressources statiques lorsque cela est Possible  
 Une ressource statique fournit une valeur pour n’importe quel attribut de propriété XAML en recherchant une référence à une ressource déjà définie. Le comportement de recherche pour cette ressource est analogue à la recherche au moment de la compilation.  
  
 Une ressource dynamique, quant à eux, crée une expression temporaire pendant la compilation initiale et donc diffèrera la recherche des ressources jusqu'à ce que la valeur de la ressource demandée est réellement nécessaire pour construire un objet. Le comportement de recherche pour cette ressource est analogue à la recherche au moment de l’exécution, qui impose un impact sur les performances. Utilisez les ressources statiques dès que possible dans votre application, à l’aide de ressources dynamiques uniquement lorsque cela est nécessaire.  
  
 L’exemple de balisage suivant illustre l’utilisation de ces deux types de ressources :  
  
 [!code-xaml[Performance#PerformanceSnippet8](~/samples/snippets/csharp/VS_Snippets_Wpf/Performance/CSharp/DynamicResource.xaml#performancesnippet8)]  
  
## <a name="see-also"></a>Voir aussi

- [Optimisation des performances des applications WPF](optimizing-wpf-application-performance.md)
- [Planification des performances des applications](planning-for-application-performance.md)
- [Tirer parti du matériel](optimizing-performance-taking-advantage-of-hardware.md)
- [Disposition et conception](optimizing-performance-layout-and-design.md)
- [Graphisme 2D et acquisition d’images](optimizing-performance-2d-graphics-and-imaging.md)
- [Comportement de l’objet](optimizing-performance-object-behavior.md)
- [Texte](optimizing-performance-text.md)
- [Liaison de données](optimizing-performance-data-binding.md)
- [Autres recommandations relatives aux performances](optimizing-performance-other-recommendations.md)
