---
title: Considérations sur les performances de l'interopérabilité entre Direct3D9 et WPF
ms.date: 03/30/2017
helpviewer_keywords:
- WPF [WPF], Direct3D9 interop performance
- Direct3D9 [WPF interoperability], performance
ms.assetid: ea8baf91-12fe-4b44-ac4d-477110ab14dd
ms.openlocfilehash: 1371fa901bebc503a0091f3229a8fd7e6ccc2c86
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61772851"
---
# <a name="performance-considerations-for-direct3d9-and-wpf-interoperability"></a>Considérations sur les performances de l'interopérabilité entre Direct3D9 et WPF
Vous pouvez héberger les contenu Direct3D9 à l’aide de la <xref:System.Windows.Interop.D3DImage> classe. Hébergement de contenu de Direct3D9 peut affecter les performances de votre application. Cette rubrique décrit les meilleures pratiques pour optimiser les performances lors de l’hébergement de contenu Direct3D9 dans une application Windows Presentation Foundation (WPF). Ces meilleures pratiques incluent l’utilisation de <xref:System.Windows.Interop.D3DImage> et meilleures pratiques lorsque vous utilisez Windows Vista, Windows XP, et affiche des écrans multiples.  
  
> [!NOTE]
>  Pour obtenir des exemples de code qui illustrent ces meilleures pratiques, consultez [interopérabilité WPF et Direct3D9](wpf-and-direct3d9-interoperation.md).  
  
## <a name="use-d3dimage-sparingly"></a>Utilisez D3DImage avec parcimonie  
 Direct3D9 contenu hébergé dans un <xref:System.Windows.Interop.D3DImage> instance ne rend pas aussi rapide que dans une application Direct3D pure. Copie de la surface et de vider le tampon de commande peuvent être des opérations coûteuses. Comme le nombre de <xref:System.Windows.Interop.D3DImage> augmente d’instances, de consommation plus se produit et dégradent les performances. Par conséquent, vous devez utiliser <xref:System.Windows.Interop.D3DImage> avec parcimonie.  
  
## <a name="best-practices-on-windows-vista"></a>Meilleures pratiques sur Windows Vista  
 Pour de meilleures performances sur Windows Vista avec un affichage qui est configuré pour utiliser le modèle de pilote d’affichage de Windows (WDDM), créez votre surface Direct3D9 sur un `IDirect3DDevice9Ex` appareil. Cela permet le partage de surface. La carte vidéo doit prendre en charge la `D3DDEVCAPS2_CAN_STRETCHRECT_FROM_TEXTURES` et `D3DCAPS2_CANSHARERESOURCE` fonctionnalités du pilote sur Windows Vista. Tous les autres paramètres entraînent la surface à être copiée via le logiciel, ce qui réduit considérablement les performances.  
  
> [!NOTE]
>  Si Windows Vista a un affichage qui est configuré pour utiliser le modèle de pilote d’affichage de Windows XP (XDDM), la surface est toujours copiée via le logiciel, indépendamment des paramètres. Avec la carte vidéo et les paramètres appropriés, vous verrez meilleures performances sur Windows Vista lorsque vous utilisez le modèle WDDM, car la copie de la surface est effectuées dans le matériel.  
  
## <a name="best-practices-on-windows-xp"></a>Meilleures pratiques sur Windows XP  
 Pour de meilleures performances sur Windows XP, qui utilise le modèle de pilote d’affichage (XDDM) Windows XP, créez une surface verrouillable qui se comporte correctement lors de la `IDirect3DSurface9::GetDC` méthode est appelée. En interne, le `BitBlt` méthode transfère la surface sur périphériques de matériel. Le `GetDC` méthode fonctionne toujours sur les surfaces XRGB. Toutefois, si l’ordinateur client exécute Windows XP avec SP3 ou SP2, et si le client possède également le correctif logiciel pour la fonctionnalité de superposition des fenêtres, cette méthode fonctionne uniquement sur les surfaces ARGB. La carte vidéo doit prendre en charge la `D3DDEVCAPS2_CAN_STRETCHRECT_FROM_TEXTURES` fonctionnalité de pilote.  
  
 Une profondeur de l’affichage du bureau 16 bits peut réduire considérablement les performances. Un poste de travail 32 bits est recommandé.  
  
 Si vous développez pour Windows Vista et Windows XP, testez les performances sur Windows XP. Insuffisance de mémoire vidéo sur Windows XP est une préoccupation. En outre, <xref:System.Windows.Interop.D3DImage> sur Windows XP utilise davantage de mémoire vidéo et de bande passante que Windows Vista WDDM, en raison d’une copie de mémoire vidéo supplémentaire nécessaire. Par conséquent, vous pouvez obtenir des performances soient moins bonnes sur XP de Windows que sur Windows Vista pour le même matériel vidéo.  
  
> [!NOTE]
>  XDDM est disponible sur Windows XP et Windows Vista ; Toutefois, le modèle WDDM est disponible uniquement sous Windows Vista.  
  
## <a name="general-best-practices"></a>Meilleures pratiques générales  
 Lorsque vous créez l’appareil, utilisez le `D3DCREATE_MULTITHREADED` indicateur de création. Cela réduit les performances, mais le système de rendu WPF appelle des méthodes sur cet appareil à partir d’un autre thread. Veillez à suivre le protocole de verrouillage correctement, afin qu’aucun des deux threads accéder à l’appareil en même temps.  
  
 Si votre rendu est exécuté sur un thread managé WPF, il est fortement recommandé de créer l’appareil avec le `D3DCREATE_FPU_PRESERVE` indicateur de création. Sans ce paramètre, le rendu D3D peut réduire la précision des opérations de double précision WPF et introduire des problèmes de rendu.  
  
 Mosaïque un <xref:System.Windows.Interop.D3DImage> est rapide, sauf si vous disposer en mosaïque une surface non pow2 sans prise en charge matérielle, ou si vous disposer en mosaïque un <xref:System.Windows.Media.DrawingBrush> ou <xref:System.Windows.Media.VisualBrush> qui contient un <xref:System.Windows.Interop.D3DImage>.  
  
## <a name="best-practices-for-multi-monitor-displays"></a>Meilleures pratiques pour l’affichage sur plusieurs écrans  
 Si vous utilisez un ordinateur qui dispose de plusieurs moniteurs, vous devez suivre les meilleures pratiques décrites précédemment. Il existe également certaines considérations de performances supplémentaires pour une configuration de plusieurs écran.  
  
 Lorsque vous créez la mémoire tampon d’arrière-plan, il est créé sur un appareil spécifique et l’adaptateur, mais WPF peut afficher le tampon d’affichage sur n’importe quelle carte. Copie pour des adaptateurs pour mettre à jour le tampon d’affichage peut être très coûteux. Sur Windows Vista est configuré pour utiliser le WDDM avec plusieurs cartes vidéo et un `IDirect3DDevice9Ex` appareil, si le tampon d’affichage est sur un autre adaptateur mais toujours sur la même carte vidéo, il n’y a aucune altération des performances. Toutefois, sur Windows XP et le XDDM avec plusieurs cartes vidéo, il est sensiblement les performances lorsque le tampon d’affichage est affiché sur un autre adaptateur que la mémoire tampon d’arrière-plan. Pour plus d’informations, consultez [interopérabilité WPF et Direct3D9](wpf-and-direct3d9-interoperation.md).  
  
## <a name="performance-summary"></a>Résumé des performances  
 Le tableau suivant montre les performances de la mise à jour du tampon d’affichage en fonction du système d’exploitation, le format de pixel et verrouillabilité de la surface. Le tampon d’affichage et de la mémoire tampon d’arrière-plan sont supposées pour être sur la même carte. Selon la configuration de l’adaptateur, les mises à jour matérielles sont généralement beaucoup plus rapides que les mises à jour logicielles.  
  
|Format de pixel de la surface|9Ex, WDDM et Windows Vista|Autres configurations de Windows Vista|Windows XP SP3 ou SP2 avec correctif logiciel|Windows XP SP2|  
|--------------------------|---------------------------------|----------------------------------------|--------------------------------------|--------------------|  
|D3DFMT_X8R8G8B8 (non verrouillable)|**Mise à jour du matériel**|Mise à jour logicielle|Mise à jour logicielle|Mise à jour logicielle|  
|D3DFMT_X8R8G8B8 (lockable)|**Mise à jour du matériel**|Mise à jour logicielle|**Mise à jour du matériel**|**Mise à jour du matériel**|  
|D3DFMT_A8R8G8B8 (non verrouillable)|**Mise à jour du matériel**|Mise à jour logicielle|Mise à jour logicielle|Mise à jour logicielle|  
|D3DFMT_A8R8G8B8 (lockable)|**Mise à jour du matériel**|Mise à jour logicielle|**Mise à jour du matériel**|Mise à jour logicielle|  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Interop.D3DImage>
- [Interopérabilité WPF et Direct3D9](wpf-and-direct3d9-interoperation.md)
- [Procédure pas à pas : Création de contenu Direct3D9 à héberger dans WPF](walkthrough-creating-direct3d9-content-for-hosting-in-wpf.md)
- [Procédure pas à pas : Hébergement de contenu Direct3D9 dans WPF](walkthrough-hosting-direct3d9-content-in-wpf.md)
