---
title: Architecture d'entrée pour l'interopérabilité entre Windows Forms et WPF
ms.date: 03/30/2017
helpviewer_keywords:
- input architecture [WPF interoperability]
- messages [WPF]
- Windows Forms [WPF], interoperability with
- Windows Forms [WPF], WPF interoperation
- interoperability [WPF], Windows Forms
- modeless forms [WPF]
- ElementHost keyboard and messages [WPF]
- keyboard interoperation [WPF]
- WindowsFormsHost keyboard and messages [WPF]
- modeless dialog boxes [WPF]
ms.assetid: 0eb6f137-f088-4c5e-9e37-f96afd28f235
ms.openlocfilehash: 2df754c0c47ea99c0892e0b9365da5589f2eab76
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62007095"
---
# <a name="windows-forms-and-wpf-interoperability-input-architecture"></a>Architecture d'entrée pour l'interopérabilité entre Windows Forms et WPF
Interopérabilité entre le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] et [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] nécessite que les deux technologies disposent du traitement d’entrée au clavier approprié. Cette rubrique décrit comment ces technologies implémentent le clavier et traitement pour permettre l’interopérabilité régulière dans des applications hybrides du message.  
  
 Cette rubrique contient les sous-sections suivantes :  
  
- Formulaires sans mode et les boîtes de dialogue  
  
- Clavier WindowsFormsHost et traitement des messages  
  
- Clavier ElementHost et traitement des messages  
  
## <a name="modeless-forms-and-dialog-boxes"></a>Formulaires sans mode et les boîtes de dialogue  
 Appeler le <xref:System.Windows.Forms.Integration.WindowsFormsHost.EnableWindowsFormsInterop%2A> méthode sur le <xref:System.Windows.Forms.Integration.WindowsFormsHost> élément pour ouvrir une zone de formulaire ou de la boîte de dialogue non modale à partir d’un [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]-application basée sur.  
  
 Appelez le <xref:System.Windows.Forms.Integration.ElementHost.EnableModelessKeyboardInterop%2A> méthode sur le <xref:System.Windows.Forms.Integration.ElementHost> contrôle pour ouvrir un non modal [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] page dans un [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)]-application basée sur.  
  
## <a name="windowsformshost-keyboard-and-message-processing"></a>Clavier WindowsFormsHost et traitement des messages  
 Quand ils sont hébergés par un [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]-application, basée sur [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] clavier et le message de traitement se compose des éléments suivants :  
  
- Le <xref:System.Windows.Forms.Integration.WindowsFormsHost> classe acquiert des messages à partir de la [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] boucle de message, qui est implémentée par le <xref:System.Windows.Interop.ComponentDispatcher> classe.  
  
- Le <xref:System.Windows.Forms.Integration.WindowsFormsHost> classe crée un substitut [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] boucle de message afin de garantir qu’ordinaire [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] clavier traitement se produit.  
  
- Le <xref:System.Windows.Forms.Integration.WindowsFormsHost> la classe implémente le <xref:System.Windows.Interop.IKeyboardInputSink> interface pour coordonner la gestion du focus avec [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)].  
  
- Le <xref:System.Windows.Forms.Integration.WindowsFormsHost> contrôles s’inscrivent et démarrent leurs boucles de messages.  
  
 Les sections suivantes décrivent ces parties du processus plus en détail.  
  
### <a name="acquiring-messages-from-the-wpf-message-loop"></a>Acquisition de Messages à partir de la boucle de messages WPF  
 Le <xref:System.Windows.Interop.ComponentDispatcher> classe implémente le Gestionnaire de boucle de message pour [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)]. Le <xref:System.Windows.Interop.ComponentDispatcher> classe fournit des hooks pour que les clients externes pour filtrer les messages avant [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] les traite.  
  
 L’implémentation d’interopérabilité gère le <xref:System.Windows.Interop.ComponentDispatcher.ThreadFilterMessage?displayProperty=nameWithType> événement, ce qui permet de [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôles pour traiter les messages avant [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] contrôles.  
  
### <a name="surrogate-windows-forms-message-loop"></a>Boucle de Message de remplacement Windows Forms  
 Par défaut, le <xref:System.Windows.Forms.Application?displayProperty=nameWithType> classe contient la boucle de message principale pour [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] applications. Lors de l’interopérabilité, la [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] message boucle ne traite pas les messages. Par conséquent, cette logique doit être reproduite. Le gestionnaire pour le <xref:System.Windows.Interop.ComponentDispatcher.ThreadFilterMessage?displayProperty=nameWithType> événement effectue les étapes suivantes :  
  
1. Filtre le message à l’aide de la <xref:System.Windows.Forms.IMessageFilter> interface.  
  
2. Appelle le <xref:System.Windows.Forms.Control.PreProcessMessage%2A?displayProperty=nameWithType> (méthode).  
  
3. Traduit et distribue le message, si nécessaire.  
  
4. Transmet le message au contrôle d’hébergement, si aucun des autres contrôles ne traitement le message.  
  
### <a name="ikeyboardinputsink-implementation"></a>Implémentation IKeyboardInputSink  
 La boucle de message de substitut gère la gestion du clavier. Par conséquent, le <xref:System.Windows.Interop.IKeyboardInputSink.TabInto%2A?displayProperty=nameWithType> méthode est le seul <xref:System.Windows.Interop.IKeyboardInputSink> membre qui nécessite une implémentation dans la <xref:System.Windows.Forms.Integration.WindowsFormsHost> classe.  
  
 Par défaut, le <xref:System.Windows.Interop.HwndHost> classe retourne `false` pour son <xref:System.Windows.Interop.HwndHost.System%23Windows%23Interop%23IKeyboardInputSink%23TabInto%2A> implémentation. Cela empêche la tabulation à partir d’un [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] le contrôle à un [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôle.  
  
 Le <xref:System.Windows.Forms.Integration.WindowsFormsHost> implémentation de la <xref:System.Windows.Interop.IKeyboardInputSink.TabInto%2A?displayProperty=nameWithType> méthode effectue les étapes suivantes :  
  
1. Recherche le premier ou dernier [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] contrôle contenu par le <xref:System.Windows.Forms.Integration.WindowsFormsHost> contrôle et qui peut recevoir le focus. Le choix de contrôle dépend des informations de parcours.  
  
2. Définit le focus au contrôle et retourne `true`.  
  
3. Si aucun contrôle ne peut recevoir le focus, retourne `false`.  
  
### <a name="windowsformshost-registration"></a>WindowsFormsHost Registration  
 Lorsque le handle de fenêtre pour un <xref:System.Windows.Forms.Integration.WindowsFormsHost> contrôle est créé, le <xref:System.Windows.Forms.Integration.WindowsFormsHost> contrôle appelle une méthode statique interne qui enregistre sa présence pour la boucle de message.  
  
 Pendant l’inscription, le <xref:System.Windows.Forms.Integration.WindowsFormsHost> contrôle examine la boucle de message. Si la boucle de message n’a pas été démarrée, le <xref:System.Windows.Interop.ComponentDispatcher.ThreadFilterMessage?displayProperty=nameWithType> Gestionnaire d’événements est créé. La boucle de message est considéré comme à s’exécuter quand le <xref:System.Windows.Interop.ComponentDispatcher.ThreadFilterMessage?displayProperty=nameWithType> Gestionnaire d’événements est attaché.  
  
 Quand le handle de fenêtre est détruit, le <xref:System.Windows.Forms.Integration.WindowsFormsHost> contrôle lui-même supprime l’inscription.  
  
## <a name="elementhost-keyboard-and-message-processing"></a>Clavier ElementHost et traitement des messages  
 Quand ils sont hébergés par un [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] application, [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] clavier et le message de traitement se compose des éléments suivants :  
  
- <xref:System.Windows.Interop.HwndSource>, <xref:System.Windows.Interop.IKeyboardInputSink>, et <xref:System.Windows.Interop.IKeyboardInputSite> implémentations d’interface.  
  
- Touches de direction et de tabulation.  
  
- Touches de commande et les clés de boîte de dialogue.  
  
- [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] traitement de l’accélérateur.  
  
 Les sections suivantes décrivent ces parties plus en détail.  
  
### <a name="interface-implementations"></a>Implémentations d’interface  
 Dans [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)], les messages de clavier sont routés vers le handle de fenêtre du contrôle qui a le focus. Dans la <xref:System.Windows.Forms.Integration.ElementHost> contrôle, ces messages sont routés vers l’élément hébergé. Pour ce faire, le <xref:System.Windows.Forms.Integration.ElementHost> contrôle fournit une <xref:System.Windows.Interop.HwndSource> instance. Si le <xref:System.Windows.Forms.Integration.ElementHost> contrôle a le focus, le <xref:System.Windows.Interop.HwndSource> instance achemine la plupart des entrées au clavier afin qu’il puisse être traité par le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Input.InputManager> classe.  
  
 Le <xref:System.Windows.Interop.HwndSource> la classe implémente le <xref:System.Windows.Interop.IKeyboardInputSink> et <xref:System.Windows.Interop.IKeyboardInputSite> interfaces.  
  
 Interopérabilité du clavier s’appuie sur l’implémentation de la <xref:System.Windows.Interop.IKeyboardInputSite.OnNoMoreTabStops%2A> méthode pour gérer la touche TAB et flèche de clé d’entrée qui déplace le focus en dehors des éléments hébergés.  
  
### <a name="tabbing-and-arrow-keys"></a>TAB et les touches de direction  
 Le [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] logique de sélection est mappée à la <xref:System.Windows.Interop.HwndSource.System%23Windows%23Interop%23IKeyboardInputSink%23TabInto%2A> et <xref:System.Windows.Interop.IKeyboardInputSite.OnNoMoreTabStops%2A> méthodes à implémenter la tabulation et la flèche de navigation de clé. Substitution de la <xref:System.Windows.Forms.Integration.ElementHost.Select%2A> méthode accomplit ce mappage.  
  
### <a name="command-keys-and-dialog-box-keys"></a>Touches de commande et les clés de boîte de dialogue  
 Pour donner [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] la première occasion pour traiter les touches de commande et les clés de la boîte de dialogue, [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] prétraitement de la commande est connecté à la <xref:System.Windows.Interop.IKeyboardInputSink.TranslateAccelerator%2A> (méthode). Substitution de la <xref:System.Windows.Forms.Control.ProcessCmdKey%2A?displayProperty=nameWithType> méthode connecte les deux technologies.  
  
 Avec le <xref:System.Windows.Interop.IKeyboardInputSink.TranslateAccelerator%2A> (méthode), les éléments hébergés peuvent gérer tout message clé, tel que WM_KEYDOWN, WM_KEYUP, WM_SYSKEYDOWN ou WM_SYSKEYUP, y compris des touches de commande, telles que les touches de tabulation, entrée, ÉCHAP et flèche. Si un message de touche n’est pas géré, il est envoyé le [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] hiérarchie ancêtre pour la gestion.  
  
### <a name="accelerator-processing"></a>Traitement d’accélérateur  
 Pour traiter correctement, les accélérateurs [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] traitement d’accélérateur doit être connecté à la [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Input.AccessKeyManager> classe. En outre, tous les messages WM_CHAR doivent être routés correctement aux éléments hébergés.  
  
 Étant donné que la valeur par défaut <xref:System.Windows.Interop.HwndSource> implémentation de la <xref:System.Windows.Interop.IKeyboardInputSink.TranslateChar%2A> méthode retourne `false`, les messages WM_CHAR sont traités à l’aide de la logique suivante :  
  
- Le <xref:System.Windows.Forms.Control.IsInputChar%2A?displayProperty=nameWithType> méthode est substituée pour garantir que tous les messages WM_CHAR sont envoyés aux éléments hébergés.  
  
- Si la touche ALT est enfoncée, le message est WM_SYSCHAR. [!INCLUDE[TLA#tla_winforms](../../../../includes/tlasharptla-winforms-md.md)] n’effectue aucun prétraitement ce message via le <xref:System.Windows.Forms.Control.IsInputChar%2A> (méthode). Par conséquent, le <xref:System.Windows.Forms.Control.ProcessMnemonic%2A> méthode est substituée pour interroger le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Input.AccessKeyManager> pour un accélérateur enregistré. Si un accélérateur enregistré est trouvé, <xref:System.Windows.Input.AccessKeyManager> traite.  
  
- Si la touche ALT n’est pas activée, le [!INCLUDE[TLA2#tla_winclient](../../../../includes/tla2sharptla-winclient-md.md)] <xref:System.Windows.Input.InputManager> classe traite l’entrée non prise en charge. Si l’entrée est un accélérateur, le <xref:System.Windows.Input.AccessKeyManager> traite. Le <xref:System.Windows.Input.InputManager.PostProcessInput> événement est géré pour les messages WM_CHAR qui n’ont pas été traités.  
  
 Lorsque l’utilisateur appuie sur la touche ALT, les signaux visuels accélérateur sont affichent sur la totalité du formulaire. Pour prendre en charge ce comportement, tous les <xref:System.Windows.Forms.Integration.ElementHost> contrôles sur le formulaire actif reçoivent des messages WM_SYSKEYDOWN, quel que soit le contrôle a le focus.  
  
 Les messages sont envoyés uniquement à <xref:System.Windows.Forms.Integration.ElementHost> contrôles dans le formulaire actif.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.Integration.WindowsFormsHost.EnableWindowsFormsInterop%2A>
- <xref:System.Windows.Forms.Integration.ElementHost.EnableModelessKeyboardInterop%2A>
- <xref:System.Windows.Forms.Integration.ElementHost>
- <xref:System.Windows.Forms.Integration.WindowsFormsHost>
- [Procédure pas à pas : Hébergement d’un contrôle Composite de formulaires Windows dans WPF](walkthrough-hosting-a-windows-forms-composite-control-in-wpf.md)
- [Procédure pas à pas : Hébergement d’un contrôle Composite WPF dans les Windows Forms](walkthrough-hosting-a-wpf-composite-control-in-windows-forms.md)
- [Interopérabilité WPF et Win32](wpf-and-win32-interoperation.md)
