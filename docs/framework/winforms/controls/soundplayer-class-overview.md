---
title: Vue d'ensemble de la classe SoundPlayer
ms.date: 03/30/2017
helpviewer_keywords:
- playing sounds [Windows Forms], SoundPlayer class
- SoundPlayer class [Windows Forms], about SoundPlayer class
- sounds [Windows Forms], playing
ms.assetid: fcebb938-62b9-4677-9cbe-6465bc863e22
ms.openlocfilehash: 3ff23cbfa78b803d4526e7a7c389fd5d458a967c
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59195005"
---
# <a name="soundplayer-class-overview"></a><span data-ttu-id="0115d-102">Vue d'ensemble de la classe SoundPlayer</span><span class="sxs-lookup"><span data-stu-id="0115d-102">SoundPlayer Class Overview</span></span>
<span data-ttu-id="0115d-103">La classe <xref:System.Media.SoundPlayer> vous permet d'inclure facilement des sons dans vos applications.</span><span class="sxs-lookup"><span data-stu-id="0115d-103">The <xref:System.Media.SoundPlayer> class enables you to easily include sounds in your applications.</span></span>  
  
 <span data-ttu-id="0115d-104">Le <xref:System.Media.SoundPlayer> classe peut lire des fichiers audio au format .wav, à partir d’une ressource ou à partir d’emplacements UNC ou HTTP.</span><span class="sxs-lookup"><span data-stu-id="0115d-104">The <xref:System.Media.SoundPlayer> class can play sound files in the .wav format, either from a resource or from UNC or HTTP locations.</span></span> <span data-ttu-id="0115d-105">En outre, la <xref:System.Media.SoundPlayer> classe vous permet de charger ou lire des sons de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="0115d-105">Additionally, the <xref:System.Media.SoundPlayer> class enables you to load or play sounds asynchronously.</span></span>  
  
 <span data-ttu-id="0115d-106">Vous pouvez également utiliser la classe <xref:System.Media.SystemSounds> pour jouer l'un des sons système courants, tel qu'un signal sonore.</span><span class="sxs-lookup"><span data-stu-id="0115d-106">You can also use the <xref:System.Media.SystemSounds> class to play common system sounds, including a beep.</span></span>  
  
## <a name="commonly-used-properties-methods-and-events"></a><span data-ttu-id="0115d-107">Propriétés, méthodes et événements couramment utilisés</span><span class="sxs-lookup"><span data-stu-id="0115d-107">Commonly Used Properties, Methods, and Events</span></span>  
  
|<span data-ttu-id="0115d-108">Nom</span><span class="sxs-lookup"><span data-stu-id="0115d-108">Name</span></span>|<span data-ttu-id="0115d-109">Description</span><span class="sxs-lookup"><span data-stu-id="0115d-109">Description</span></span>|  
|----------|-----------------|  
|<xref:System.Media.SoundPlayer.SoundLocation%2A> <span data-ttu-id="0115d-110">propriété</span><span class="sxs-lookup"><span data-stu-id="0115d-110">property</span></span>|<span data-ttu-id="0115d-111">Chemin du fichier ou adresse web du son.</span><span class="sxs-lookup"><span data-stu-id="0115d-111">The file path or Web address of the sound.</span></span> <span data-ttu-id="0115d-112">Les valeurs acceptables peuvent être UNC ou HTTP.</span><span class="sxs-lookup"><span data-stu-id="0115d-112">Acceptable values can be UNC or HTTP.</span></span>|  
|<xref:System.Media.SoundPlayer.LoadTimeout%2A> <span data-ttu-id="0115d-113">propriété</span><span class="sxs-lookup"><span data-stu-id="0115d-113">property</span></span>|<span data-ttu-id="0115d-114">Nombre de millisecondes que votre programme attend pour charger un son avant de lever une exception.</span><span class="sxs-lookup"><span data-stu-id="0115d-114">The number of milliseconds your program will wait to load a sound before it throws an exception.</span></span> <span data-ttu-id="0115d-115">La valeur par défaut est 10 secondes.</span><span class="sxs-lookup"><span data-stu-id="0115d-115">The default is 10 seconds.</span></span>|  
|<xref:System.Media.SoundPlayer.IsLoadCompleted%2A> <span data-ttu-id="0115d-116">propriété</span><span class="sxs-lookup"><span data-stu-id="0115d-116">property</span></span>|<span data-ttu-id="0115d-117">Valeur booléenne indiquant si le chargement du son est terminé.</span><span class="sxs-lookup"><span data-stu-id="0115d-117">A Boolean value indicating whether the sound has finished loading.</span></span>|  
|<xref:System.Media.SoundPlayer.Load%2A> <span data-ttu-id="0115d-118">méthode</span><span class="sxs-lookup"><span data-stu-id="0115d-118">method</span></span>|<span data-ttu-id="0115d-119">Charge un son de façon synchrone.</span><span class="sxs-lookup"><span data-stu-id="0115d-119">Loads a sound synchronously.</span></span>|  
|<xref:System.Media.SoundPlayer.LoadAsync%2A> <span data-ttu-id="0115d-120">méthode</span><span class="sxs-lookup"><span data-stu-id="0115d-120">method</span></span>|<span data-ttu-id="0115d-121">Commence à charger un son de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="0115d-121">Begins to load a sound asynchronously.</span></span> <span data-ttu-id="0115d-122">Lorsque le chargement est terminé, il déclenche le <xref:System.Media.SoundPlayer.OnLoadCompleted%2A> événement.</span><span class="sxs-lookup"><span data-stu-id="0115d-122">When loading is complete, it raises the <xref:System.Media.SoundPlayer.OnLoadCompleted%2A> event.</span></span>|  
|<xref:System.Media.SoundPlayer.Play%2A> <span data-ttu-id="0115d-123">méthode</span><span class="sxs-lookup"><span data-stu-id="0115d-123">method</span></span>|<span data-ttu-id="0115d-124">Lit le son spécifié dans le <xref:System.Media.SoundPlayer.SoundLocation%2A> ou <xref:System.Media.SoundPlayer.Stream%2A> propriété dans un nouveau thread.</span><span class="sxs-lookup"><span data-stu-id="0115d-124">Plays the sound specified in the <xref:System.Media.SoundPlayer.SoundLocation%2A> or <xref:System.Media.SoundPlayer.Stream%2A> property in a new thread.</span></span>|  
|<xref:System.Media.SoundPlayer.PlaySync%2A> <span data-ttu-id="0115d-125">méthode</span><span class="sxs-lookup"><span data-stu-id="0115d-125">method</span></span>|<span data-ttu-id="0115d-126">Lit le son spécifié dans le <xref:System.Media.SoundPlayer.SoundLocation%2A> ou <xref:System.Media.SoundPlayer.Stream%2A> propriété dans le thread actuel.</span><span class="sxs-lookup"><span data-stu-id="0115d-126">Plays the sound specified in the <xref:System.Media.SoundPlayer.SoundLocation%2A> or <xref:System.Media.SoundPlayer.Stream%2A> property in the current thread.</span></span>|  
|<xref:System.Media.SoundPlayer.Stop%2A> <span data-ttu-id="0115d-127">méthode</span><span class="sxs-lookup"><span data-stu-id="0115d-127">method</span></span>|<span data-ttu-id="0115d-128">Arrête le son actuellement émis.</span><span class="sxs-lookup"><span data-stu-id="0115d-128">Stops any sound currently playing.</span></span>|  
|<xref:System.Media.SoundPlayer.LoadCompleted> <span data-ttu-id="0115d-129">événement</span><span class="sxs-lookup"><span data-stu-id="0115d-129">event</span></span>|<span data-ttu-id="0115d-130">Déclenché après une tentative de chargement d’un son.</span><span class="sxs-lookup"><span data-stu-id="0115d-130">Raised after the load of a sound is attempted.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="0115d-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0115d-131">See also</span></span>

- <xref:System.Media.SoundPlayer>
- <xref:System.Media.SystemSounds>
