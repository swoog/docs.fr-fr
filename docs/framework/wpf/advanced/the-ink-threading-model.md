---
title: Modèle de thread de l'encre
ms.date: 03/30/2017
helpviewer_keywords:
- application user interface thread [WPF]
- stylus plug-in
- ink threading model [WPF]
- ink [WPF], rendering
- pen thread [WPF]
- threading model [WPF]
- rendering ink [WPF]
- dynamic rendering thread [WPF]
- ink collection plug-in
- plug-ins [WPF], for ink
ms.assetid: c85fcad1-cb50-4431-847c-ac4145a35c89
ms.openlocfilehash: 80e7ef202c46a23069766512cf4e67bb21a49564
ms.sourcegitcommit: 0be8a279af6d8a43e03141e349d3efd5d35f8767
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/18/2019
ms.locfileid: "59335314"
---
# <a name="the-ink-threading-model"></a>Modèle de thread de l'encre
Un des avantages de l’encre sur un Tablet PC est qu’il la sensation écriture avec un crayon régulière et du papier.  Pour ce faire, le stylet collecte les données d’entrée à un rythme beaucoup plus élevée que la souris et restitue l’encre lorsque l’utilisateur écrit.  Thread d’interface (UI) de l’application utilisateur n’est pas suffisant pour collecter les données de stylet et encre de rendu, car il peut se bloquer.  Pour y remédier, un [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] application utilise deux threads supplémentaires lorsqu’un utilisateur écrit l’encre.  
  
 La liste suivante décrit les threads qui participent à la collecte et le rendu de l’encre numérique :  
  
-   Thread de stylet - le thread qui accepte une entrée à partir du stylet.  (En réalité, il s’agit d’un pool de threads, mais cette rubrique fait référence à ce dernier en tant qu’un thread de stylet.)  
  
-   Thread d’interface utilisateur application - le thread qui contrôle l’interface utilisateur de l’application.  
  
-   Thread de rendu dynamique - le thread qui restitue l’encre lorsque l’utilisateur dessine un trait. Le thread de rendu dynamique est différent du thread qui restitue des autres éléments d’interface utilisateur pour l’application, comme indiqué dans la fenêtre Presentation Foundation [modèle de thread](threading-model.md).  
  
 Le modèle d’encrage est le même si l’application utilise le <xref:System.Windows.Controls.InkCanvas> ou un contrôle personnalisé similaire à celui de [création d’un contrôle d’entrée d’encre](creating-an-ink-input-control.md).  Bien que cette rubrique étudie les threads en termes de la <xref:System.Windows.Controls.InkCanvas>, les mêmes concepts s’appliquent lorsque vous créez un contrôle personnalisé.  
  
## <a name="threading-overview"></a>Vue d’ensemble de Threading  
 Le diagramme suivant illustre le modèle de thread lorsqu’un utilisateur dessine un trait :  
  
 ![Modèle de thread lors du dessin d’un trait. ](./media/inkthreading-drawingink.png "InkThreading_DrawingInk")  
  
1. Actions qui se produisent pendant que l’utilisateur dessine le trait  
  
    1.  Lorsque l’utilisateur dessine un trait, les points du stylet arrivent sur le thread de stylet.  Plug-ins du stylet, y compris le <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer>, acceptez les points du stylet sur le thread de stylet et ont la possibilité de les modifier avant du <xref:System.Windows.Controls.InkCanvas> les reçoit.  
  
    2.  Le <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> restitue les points du stylet sur le thread de rendu dynamique. Cela se produit en même temps que l’étape précédente.  
  
    3.  Le <xref:System.Windows.Controls.InkCanvas> reçoit les points du stylet sur le thread d’interface utilisateur.  
  
2. Actions qui se produisent une fois que l’utilisateur termine le trait  
  
    1.  Lorsque l’utilisateur termine le trait, la <xref:System.Windows.Controls.InkCanvas> crée un <xref:System.Windows.Ink.Stroke> de l’objet et l’ajoute à la <xref:System.Windows.Controls.InkPresenter>, qui le restitue de manière statique.  
  
    2.  Les alertes de thread d’interface utilisateur la <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> qui le trait est restitué de manière statique, par conséquent, le <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> supprime la représentation visuelle du trait.  
  
## <a name="ink-collection-and-stylus-plug-ins"></a>Collecte d’encre et de stylet Plug-ins  
 Chaque <xref:System.Windows.UIElement> a un <xref:System.Windows.Input.StylusPlugIns.StylusPlugInCollection>.  Le <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> des objets dans le <xref:System.Windows.Input.StylusPlugIns.StylusPlugInCollection> reçoivent et peuvent modifier les points du stylet sur le thread de stylet. Le <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> objets reçoivent les points du stylet selon leur ordre dans le <xref:System.Windows.Input.StylusPlugIns.StylusPlugInCollection>.  
  
 Le diagramme suivant illustre la situation hypothétique où la <xref:System.Windows.UIElement.StylusPlugIns%2A> collection d’un <xref:System.Windows.UIElement> contient `stylusPlugin1`, un <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer>, et `stylusPlugin2`, dans cet ordre.  
  
 ![Ordre des StylusPlugins affecte la sortie. ](./media/inkthreading-pluginorder.png "InkThreading_PluginOrder")  
  
 Dans le diagramme précédent, le comportement suivant se produit :  
  
1. `StylusPlugin1` Modifie les valeurs de x et y.  
  
2. <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> reçoit les points du stylet modifié et les affiche sur le thread de rendu dynamique.  
  
3. `StylusPlugin2` reçoit les points du stylet modifié, puis modifie les valeurs de x et y.  
  
4. L’application collecte les points du stylet et, lorsque l’utilisateur termine le trait, restitue le trait de manière statique.  
  
 Supposons que `stylusPlugin1` restreint les points du stylet à un rectangle et `stylusPlugin2` traduit les points du stylet vers la droite.  Dans le scénario précédent, le <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> reçoit les points du stylet restreints, mais pas les points du stylet traduits.  Lorsque l’utilisateur dessine le trait, le trait est affiché dans les limites du rectangle, mais le trait ne semble pas être traduit jusqu'à ce que l’utilisateur soulève le stylet.  
  
### <a name="performing-operations-with-a-stylus-plug-in-on-the-ui-thread"></a>Effectuer des opérations avec un plug-in sur le thread d’interface utilisateur du stylet  
 Étant donné que le test de positionnement précis ne peut pas être effectué sur le thread de stylet, certains éléments susceptibles de recevoir une entrée du stylet destinée aux autres éléments. Si vous devez vous assurer que l’entrée a été routée correctement avant d’effectuer une opération, vous abonner à et effectuer l’opération dans le <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn.OnStylusDownProcessed%2A>, <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn.OnStylusMoveProcessed%2A>, ou <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn.OnStylusUpProcessed%2A> (méthode). Ces méthodes sont appelées par le thread d’application après l’exécution du test de positionnement précis. Pour vous abonner à ces méthodes, appelez le <xref:System.Windows.Input.StylusPlugIns.RawStylusInput.NotifyWhenProcessed%2A> méthode dans la méthode qui se produit sur le thread de stylet.  
  
 Le diagramme suivant illustre la relation entre le thread de stylet et le thread d’interface utilisateur en ce qui concerne les événements du stylet d’un <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn>.  
  
 ![Modèles de thread de l’encre &#40;l’interface utilisateur et stylet&#41;](./media/inkthreading-plugincallbacks.png "InkThreading_PluginCallbacks")  
  
## <a name="rendering-ink"></a>Encre de rendu  
 Lorsque l’utilisateur trace un trait, <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> restitue l’encre sur un thread séparé pour que l’encre semble « couler » du stylet même lorsque le thread d’interface utilisateur est occupé.  Le <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> génère une arborescence visuelle sur le thread de rendu dynamique pendant qu’il collecte les points du stylet.  Lorsque l’utilisateur termine le trait, la <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> demande à être informé de la prochaine phase de rendu effectuée par l’application.  Une fois que l’application termine le prochain passe de rendu, le <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> nettoie son arborescence d’éléments visuels.  Le diagramme suivant illustre ce processus.  
  
 ![Diagramme des threads de l’encre](./media/inkthreading-visualtree.png "InkThreading_VisualTree")  
  
1. L’utilisateur commence le trait.  
  
    1.  Le <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> crée l’arborescence visuelle.  
  
2. L’utilisateur est le trait.  
  
    1.  Le <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> génère l’arborescence visuelle.  
  
3. L’utilisateur termine le trait.  
  
    1.  Le <xref:System.Windows.Controls.InkPresenter> ajoute le trait à son arborescence d’éléments visuels.  
  
    2.  La couche MIL (Media Integration) restitue les traits de manière statique.  
  
    3.  Le <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> nettoie les éléments visuels.
