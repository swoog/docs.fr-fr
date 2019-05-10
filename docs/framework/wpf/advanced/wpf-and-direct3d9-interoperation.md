---
title: Interopérabilité WPF et Direct3D9
ms.date: 03/30/2017
dev_langs:
- cpp
helpviewer_keywords:
- WPF [WPF], creating Direct3D9 content
- Direct3D9 [WPF interoperability], creating Direct3D9 content
ms.assetid: 1b14b823-69c4-4e8d-99e4-f6dade58f89a
ms.openlocfilehash: d04278cd2814106dacad53f268ef03227083274e
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64650807"
---
# <a name="wpf-and-direct3d9-interoperation"></a>Interopérabilité WPF et Direct3D9
Vous pouvez inclure les contenu Direct3D9 dans une application Windows Presentation Foundation (WPF). Cette rubrique décrit la procédure créer un contenu Direct3D9 afin qu’il interagit efficacement avec WPF.  
  
> [!NOTE]
>  Lorsque vous utilisez les contenu Direct3D9 dans WPF, vous devez également réfléchir aux performances. Pour plus d’informations sur comment optimiser les performances, consultez [Performance Considerations for Direct3D9 et WPF interopérabilité](performance-considerations-for-direct3d9-and-wpf-interoperability.md).  
  
## <a name="display-buffers"></a>Mémoires tampons d’affichage  
 Le <xref:System.Windows.Interop.D3DImage> classe gère deux mémoires tampons d’affichage, qui sont appelées les *mémoire tampon d’arrière-plan* et *tampon d’affichage*. La mémoire tampon d’arrière-plan est votre surface Direct3D9. Modifications apportées à la mémoire tampon d’arrière-plan sont copiées en avant dans le tampon d’affichage lorsque vous appelez le <xref:System.Windows.Interop.D3DImage.Unlock%2A> (méthode).  
  
 L’illustration suivante montre la relation entre la mémoire tampon d’arrière-plan et le tampon d’affichage.  
  
 ![Mémoires tampons d’affichage D3DImage](./media/d3dimage-buffers.png "D3DImage_buffers")  
  
## <a name="direct3d9-device-creation"></a>Création d’un appareil Direct3D9  
 Pour restituer le contenu Direct3D9, vous devez créer un périphérique Direct3D9. Il existe deux objets Direct3D9 que vous pouvez utiliser pour créer un appareil, `IDirect3D9` et `IDirect3D9Ex`. Permet de créer ces objets `IDirect3DDevice9` et `IDirect3DDevice9Ex` appareils, respectivement.  
  
 Créer un appareil en appelant une des méthodes suivantes.  
  
- `IDirect3D9 * Direct3DCreate9(UINT SDKVersion);`  
  
- `HRESULT Direct3DCreate9Ex(UINT SDKVersion, IDirect3D9Ex **ppD3D);`  
  
 Sur Windows Vista ou version ultérieure du système d’exploitation, utilisez la `Direct3DCreate9Ex` méthode avec un affichage qui est configuré pour utiliser le modèle de pilote d’affichage de Windows (WDDM). Utilisez le `Direct3DCreate9` méthode sur n’importe quelle autre plateforme.  
  
### <a name="availability-of-the-direct3dcreate9ex-method"></a>Disponibilité de la méthode Direct3DCreate9Ex  
 Le fichier d3d9.dll a la `Direct3DCreate9Ex` méthode uniquement sur Windows Vista ou version ultérieure du système d’exploitation. Si vous liez directement la fonction sur Windows XP, votre application ne parvient pas à charger. Pour déterminer si le `Direct3DCreate9Ex` méthode est prise en charge, de charger la DLL et recherchez l’adresse proc. Le code suivant montre comment tester la `Direct3DCreate9Ex` (méthode). Pour obtenir un exemple de code complet, consultez [procédure pas à pas : Création de contenu de Direct3D9 à héberger dans WPF](walkthrough-creating-direct3d9-content-for-hosting-in-wpf.md).  
  
 [!code-cpp[System.Windows.Interop.D3DImage#RendererManager_EnsureD3DObjects](~/samples/snippets/cpp/VS_Snippets_Wpf/System.Windows.Interop.D3DImage/cpp/renderermanager.cpp#renderermanager_ensured3dobjects)]  
  
### <a name="hwnd-creation"></a>Création de HWND  
 Création d’un appareil nécessite un HWND. En règle générale, vous créez un HWND factice pour Direct3D9 à utiliser. L’exemple de code suivant montre comment créer un HWND factice.  
  
 [!code-cpp[System.Windows.Interop.D3DImage#RendererManager_EnsureHWND](~/samples/snippets/cpp/VS_Snippets_Wpf/System.Windows.Interop.D3DImage/cpp/renderermanager.cpp#renderermanager_ensurehwnd)]  
  
### <a name="present-parameters"></a>Paramètres présents  
 Création d’un appareil nécessite également un `D3DPRESENT_PARAMETERS` struct, mais seuls quelques paramètres sont importants. Ces paramètres sont choisis pour minimiser l’encombrement mémoire.  
  
 Définir le `BackBufferHeight` et `BackBufferWidth` champs à 1. Les définissant sur 0 entraîne leur être définie sur les dimensions du HWND.  
  
 Toujours défini le `D3DCREATE_MULTITHREADED` et `D3DCREATE_FPU_PRESERVE` indicateurs pour empêcher endommager la mémoire utilisée par Direct3D9 et empêcher Direct3D9 de modifier les paramètres FPU.  
  
 Le code suivant montre comment initialiser le `D3DPRESENT_PARAMETERS` struct.  
  
 [!code-cpp[System.Windows.Interop.D3DImage#Renderer_Init](~/samples/snippets/cpp/VS_Snippets_Wpf/System.Windows.Interop.D3DImage/cpp/renderer.cpp#renderer_init)]  
  
## <a name="creating-the-back-buffer-render-target"></a>Création de la cible de rendu de mémoire tampon d’arrière-plan  
 Pour afficher le contenu Direct3D9 dans un <xref:System.Windows.Interop.D3DImage>, vous créez une surface Direct3D9 et affectez-le en appelant le <xref:System.Windows.Interop.D3DImage.SetBackBuffer%2A> (méthode).  
  
### <a name="verifying-adapter-support"></a>Vérification de la prise en charge de l’adaptateur  
 Avant de créer une surface, vérifiez que toutes les cartes prennent en charge les propriétés de surface que vous avez besoin. Même si vous effectuez le rendu qu’une seule carte, la fenêtre WPF peut s’afficher sur n’importe quelle carte dans le système. Vous devez toujours écrire du code Direct3D9 qui gère les configurations de carte multi, et vous devez vérifier tous les adaptateurs pour la prise en charge, étant donné que WPF peut déplacer la surface parmi les adaptateurs disponibles.  
  
 L’exemple de code suivant montre comment vérifier toutes les cartes sur le système pour Direct3D9 prennent en charge.  
  
 [!code-cpp[System.Windows.Interop.D3DImage#RendererManager_TestSurfaceSettings](~/samples/snippets/cpp/VS_Snippets_Wpf/System.Windows.Interop.D3DImage/cpp/renderermanager.cpp#renderermanager_testsurfacesettings)]  
  
### <a name="creating-the-surface"></a>Création de la Surface  
 Avant de créer une surface, vérifiez que les fonctionnalités des appareils prennent en charge les bonnes performances sur le système d’exploitation cible. Pour plus d’informations, consultez [Performance Considerations for Direct3D9 et WPF interopérabilité](performance-considerations-for-direct3d9-and-wpf-interoperability.md).  
  
 Lorsque vous avez vérifié les fonctionnalités des appareils, vous pouvez créer la surface. L’exemple de code suivant montre comment créer la cible de rendu.  
  
 [!code-cpp[System.Windows.Interop.D3DImage#Renderer_CreateSurface](~/samples/snippets/cpp/VS_Snippets_Wpf/System.Windows.Interop.D3DImage/cpp/renderer.cpp#renderer_createsurface)]  
  
### <a name="wddm"></a>WDDM  
 Sur Windows Vista et versions ultérieures, qui sont configurés pour utiliser le WDDM, vous pouvez créer une texture de cible de rendu et passer la surface de niveau 0 pour le <xref:System.Windows.Interop.D3DImage.SetBackBuffer%2A> (méthode). Cette approche n’est pas recommandée sur Windows XP, car vous ne pouvez pas créer une texture de cible de rendu verrouillable et performances seront réduit.  
  
## <a name="handling-device-state"></a>État de gestion des appareils  
 Le <xref:System.Windows.Interop.D3DImage> classe gère deux mémoires tampons d’affichage, qui sont appelées les *mémoire tampon d’arrière-plan* et *tampon d’affichage*. La mémoire tampon d’arrière-plan est votre surface Direct3D.  Modifications apportées à la mémoire tampon d’arrière-plan sont copiées en avant dans le tampon d’affichage lorsque vous appelez le <xref:System.Windows.Interop.D3DImage.Unlock%2A> méthode, où il est affiché sur le matériel. Parfois, le tampon d’affichage n’est plus disponible. Ce manque de disponibilité peut être dû de verrouillage de l’écran, les applications Direct3D exclusives plein écran, changement d’utilisateur ou autres activités du système. Lorsque cela se produit, votre application WPF est notifiée en gérant la <xref:System.Windows.Interop.D3DImage.IsFrontBufferAvailableChanged> événement.  Comment votre application répond à la mémoire tampon avant d’indisponible dépend de Si WPF est activé à revenir au rendu logiciel. Le <xref:System.Windows.Interop.D3DImage.SetBackBuffer%2A> méthode a une surcharge qui accepte un paramètre qui spécifie si WPF revient au rendu logiciel.  
  
 Lorsque vous appelez le <xref:System.Windows.Interop.D3DImage.SetBackBuffer%28System.Windows.Interop.D3DResourceType%2CSystem.IntPtr%29> surcharger ou appeler le <xref:System.Windows.Interop.D3DImage.SetBackBuffer%28System.Windows.Interop.D3DResourceType%2CSystem.IntPtr%2CSystem.Boolean%29> surcharge avec le `enableSoftwareFallback` paramètre défini sur `false`, le système de rendu libère sa référence à la mémoire tampon d’arrière-plan lorsque le tampon d’affichage n’est plus disponible et que rien n’est affiché. Lorsque le tampon d’affichage est à nouveau disponible, le système de rendu déclenche le <xref:System.Windows.Interop.D3DImage.IsFrontBufferAvailableChanged> événement pour avertir votre application WPF.  Vous pouvez créer un gestionnaire d’événements pour le <xref:System.Windows.Interop.D3DImage.IsFrontBufferAvailableChanged> événement pour redémarrer le rendu avec une surface Direct3D valide. Pour redémarrer le rendu, vous devez appeler <xref:System.Windows.Interop.D3DImage.SetBackBuffer%2A>.  
  
 Lorsque vous appelez le <xref:System.Windows.Interop.D3DImage.SetBackBuffer%28System.Windows.Interop.D3DResourceType%2CSystem.IntPtr%2CSystem.Boolean%29> surcharge avec le `enableSoftwareFallback` paramètre défini sur `true`, le système de rendu conserve sa référence à la mémoire tampon d’arrière-plan lorsque le tampon d’affichage n’est plus disponible, il est donc inutile d’appeler <xref:System.Windows.Interop.D3DImage.SetBackBuffer%2A> lors de l’avant mémoire tampon est à nouveau disponible.  
  
 Lorsque le rendu logiciel est activé, il peut arriver dans lequel le périphérique l’utilisateur n’est plus disponible, mais le système de rendu conserve une référence à la surface Direct3D. Pour vérifier si un appareil Direct3D9 n’est pas disponible, appelez le `TestCooperativeLevel` (méthode). Pour vérifier un appel de périphériques Direct3D9Ex le `CheckDeviceState` (méthode), car le `TestCooperativeLevel` méthode est déconseillée et renvoie toujours success. Si l’appareil de l’utilisateur n’est plus disponible, appelez <xref:System.Windows.Interop.D3DImage.SetBackBuffer%2A> pour libérer la référence de WPF à la mémoire tampon d’arrière-plan.  Si vous devez réinitialiser votre appareil, appelez <xref:System.Windows.Interop.D3DImage.SetBackBuffer%2A> avec la `backBuffer` paramètre défini sur `null`, puis appelez <xref:System.Windows.Interop.D3DImage.SetBackBuffer%2A> avec `backBuffer` défini sur une surface Direct3D valide.  
  
 Appelez le `Reset` pour récupérer à partir d’un appareil non valide uniquement si vous implémentez la prise en charge de l’adaptateur multi. Sinon, libérer toutes les interfaces Direct3D9 et recréez-les complètement. Si la disposition de l’adaptateur a changé, les objets Direct3D9 créés avant la modification ne sont pas mis à jour.  
  
## <a name="handling-resizing"></a>Gestion du redimensionnement  
 Si un <xref:System.Windows.Interop.D3DImage> s’affiche avec une résolution autre que sa taille d’origine, il est mis à l’échelle en fonction de l’actuel <xref:System.Windows.Media.RenderOptions.BitmapScalingMode%2A>, sauf que <xref:System.Windows.Media.Effects.SamplingMode.Bilinear> est remplacé par <xref:System.Windows.Media.BitmapScalingMode.Fant>.  
  
 Si vous avez besoin d’une meilleure fidélité, vous devez créer un nouveau surface lorsque le conteneur de la <xref:System.Windows.Interop.D3DImage> change de taille.  
  
 Il existe trois approches possibles pour gérer le redimensionnement.  
  
- Participer au système de disposition et créer une surface lorsque la taille change. Ne créez pas trop de surfaces, étant donné que vous pouvez épuiser ou fragmenter la mémoire vidéo.  
  
- Patientez jusqu'à ce qu’un événement de redimensionnement n’a pas eu lieu pour une période fixe pour créer la nouvelle surface.  
  
- Créer un <xref:System.Windows.Threading.DispatcherTimer> qui vérifie les dimensions de conteneur plusieurs fois par seconde.  
  
## <a name="multi-monitor-optimization"></a>Optimisation de plusieurs écran  
 Considérablement les performances peuvent entraîner lorsque le système de rendu déplace un <xref:System.Windows.Interop.D3DImage> vers un autre moniteur.  
  
 Sur le modèle WDDM, tant que les moniteurs sont sur le même vidéo carte et que vous utilisez `Direct3DCreate9Ex`, il n’existe aucune diminution des performances. Si les moniteurs sont sur des cartes vidéo séparées, les performances sont réduites. Sur Windows XP, les performances sont toujours altérées.  
  
 Lorsque le <xref:System.Windows.Interop.D3DImage> se déplace vers un autre moniteur, vous pouvez créer une surface sur l’adaptateur correspondant pour restaurer de bonnes performances.  
  
 Pour éviter la baisse des performances, écrivez du code spécifiquement pour le cas de plusieurs écran. La liste suivante montre une façon d’écrire du code de plusieurs écran.  
  
1. Rechercher un point de la <xref:System.Windows.Interop.D3DImage> dans l’espace d’écran avec la `Visual.ProjectToScreen` (méthode).  
  
2. Utilisez le `MonitorFromPoint` méthode GDI pour rechercher le moniteur qui affiche le point.  
  
3. Utilisez le `IDirect3D9::GetAdapterMonitor` méthode pour déterminer quelle carte Direct3D9 le moniteur se trouve sur.  
  
4. Si l’adaptateur n’est pas le même que l’adaptateur avec la mémoire tampon d’arrière-plan, créez une nouvelle mémoire tampon d’arrière-plan sur le nouveau moniteur et assignez-la à la <xref:System.Windows.Interop.D3DImage> mémoire tampon d’arrière-plan.  
  
> [!NOTE]
>  Si le <xref:System.Windows.Interop.D3DImage> chevauche moniteurs, les performances seront lentes, sauf dans le cas du WDDM et `IDirect3D9Ex` sur la même carte. Il n’existe aucun moyen pour améliorer les performances dans ce cas.  
  
 L’exemple de code suivant montre comment rechercher le moniteur actuel.  
  
 [!code-cpp[System.Windows.Interop.D3DImage#RendererManager_SetAdapter](~/samples/snippets/cpp/VS_Snippets_Wpf/System.Windows.Interop.D3DImage/cpp/renderermanager.cpp#renderermanager_setadapter)]  
  
 Mettre à jour le moniteur lorsque les <xref:System.Windows.Interop.D3DImage> les modifications de taille ou la position du conteneur, ou la mise à jour le moniteur à l’aide un `DispatcherTimer` qui met à jour plusieurs fois par seconde.  
  
## <a name="wpf-software-rendering"></a>Rendu logiciel WPF  
 WPF restitue de façon synchrone le thread d’interface utilisateur dans le logiciel dans les situations suivantes.  
  
- Impression  
  
- <xref:System.Windows.Media.Effects.BitmapEffect>  
  
- <xref:System.Windows.Media.Imaging.RenderTargetBitmap>  
  
 Lorsqu’une de ces situations se produit, le système de rendu appelle le <xref:System.Windows.Interop.D3DImage.CopyBackBuffer%2A> méthode pour copier le tampon matériel au logiciel. L’implémentation par défaut appelle la `GetRenderTargetData` méthode avec la surface. Étant donné que cet appel se produit en dehors du modèle de verrouillage/déverrouillage, elle risque d’échouer. Dans ce cas, le `CopyBackBuffer` retourne de la méthode `null` et aucune image n’est affichée.  
  
 Vous pouvez remplacer le <xref:System.Windows.Interop.D3DImage.CopyBackBuffer%2A> méthode, appelez l’implémentation de base, et si elle retourne `null`, vous pouvez retourner un espace réservé <xref:System.Windows.Media.Imaging.BitmapSource>.  
  
 Vous pouvez également implémenter votre propre rendu logiciel au lieu d’appeler l’implémentation de base.  
  
> [!NOTE]
>  Si WPF est rendu complètement dans le logiciel, <xref:System.Windows.Interop.D3DImage> n’est pas affiché car WPF ne dispose pas d’un tampon d’affichage.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Interop.D3DImage>
- [Considérations sur les performances de l'interopérabilité entre Direct3D9 et WPF](performance-considerations-for-direct3d9-and-wpf-interoperability.md)
- [Procédure pas à pas : Création de contenu Direct3D9 à héberger dans WPF](walkthrough-creating-direct3d9-content-for-hosting-in-wpf.md)
- [Procédure pas à pas : Hébergement de contenu Direct3D9 dans WPF](walkthrough-hosting-direct3d9-content-in-wpf.md)
