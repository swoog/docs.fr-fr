---
title: 'Procédure : ajouter des contrôles sans interface utilisateur à des Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
f1_keywords:
- NonVisualSelection
helpviewer_keywords:
- invisible controls [Windows Forms]
- Windows Forms controls, adding to form
- controls [Windows Forms], nonvisual
- Windows Forms controls, nonvisual
- nonvisual controls [Windows Forms]
ms.assetid: 52134d9c-cff6-4eed-8e2b-3d5eb3bd494e
ms.openlocfilehash: 49bf927085d29b60c1d9cf5d61df3894495349db
ms.sourcegitcommit: 0d0a6e96737dfe24d3257b7c94f25d9500f383ea
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/07/2019
ms.locfileid: "65210411"
---
# <a name="how-to-add-controls-without-a-user-interface-to-windows-forms"></a><span data-ttu-id="e692b-102">Procédure : ajouter des contrôles sans interface utilisateur à des Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e692b-102">How to: Add Controls Without a User Interface to Windows Forms</span></span>

<span data-ttu-id="e692b-103">Un contrôle non visuel (ou un composant) fournit des fonctionnalités à votre application.</span><span class="sxs-lookup"><span data-stu-id="e692b-103">A nonvisual control (or component) provides functionality to your application.</span></span> <span data-ttu-id="e692b-104">Contrairement à d’autres contrôles, composants ne fournissent pas d’une interface utilisateur à l’utilisateur et n’avez donc pas besoin doit être affiché sur l’aire du Concepteur de formulaires Windows.</span><span class="sxs-lookup"><span data-stu-id="e692b-104">Unlike other controls, components do not provide a user interface to the user and thus do not need to be displayed on the Windows Forms Designer surface.</span></span> <span data-ttu-id="e692b-105">Lorsqu’un composant est ajouté à un formulaire, le Concepteur de formulaires Windows affiche une barre d’état redimensionnable en bas de l’écran où tous les composants sont affichés.</span><span class="sxs-lookup"><span data-stu-id="e692b-105">When a component is added to a form, the Windows Forms Designer displays a resizable tray at the bottom of the form where all components are displayed.</span></span> <span data-ttu-id="e692b-106">Une fois qu’un contrôle a été ajouté à la barre d’état du composant, vous pouvez sélectionner le composant et définissez ses propriétés comme vous le feriez pour tout autre contrôle sur le formulaire.</span><span class="sxs-lookup"><span data-stu-id="e692b-106">Once a control has been added to the component tray, you can select the component and set its properties as you would any other control on the form.</span></span>

## <a name="add-a-component-to-a-windows-form"></a><span data-ttu-id="e692b-107">Ajouter un composant à un formulaire Windows</span><span class="sxs-lookup"><span data-stu-id="e692b-107">Add a component to a Windows Form</span></span>

1. <span data-ttu-id="e692b-108">Ouvrez le formulaire dans Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e692b-108">Open the form in Visual Studio.</span></span> <span data-ttu-id="e692b-109">Pour plus d’informations, consultez [Guide pratique pour Afficher des Windows Forms dans le concepteur](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/w5yd62ts(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="e692b-109">For details, see [How to: Display Windows Forms in the Designer](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2010/w5yd62ts(v=vs.100)).</span></span>

2. <span data-ttu-id="e692b-110">Dans le **boîte à outils**, cliquez sur un composant et faites-le glisser vers votre formulaire.</span><span class="sxs-lookup"><span data-stu-id="e692b-110">In the **Toolbox**, click a component and drag it to your form.</span></span>

     <span data-ttu-id="e692b-111">Votre composant s’affiche dans la barre d’état du composant.</span><span class="sxs-lookup"><span data-stu-id="e692b-111">Your component appears in the component tray.</span></span>

<span data-ttu-id="e692b-112">En outre, les composants peuvent être ajoutés à un formulaire au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="e692b-112">Furthermore, components can be added to a form at run time.</span></span> <span data-ttu-id="e692b-113">Il s’agit d’un scénario courant, notamment parce que les composants n’ont pas une expression visual, contrairement aux contrôles qui ont une interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e692b-113">This is a common scenario, especially because components do not have a visual expression, unlike controls that have a user interface.</span></span> <span data-ttu-id="e692b-114">Dans l’exemple ci-dessous, un <xref:System.Windows.Forms.Timer> composant est ajouté au moment de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="e692b-114">In the example below, a <xref:System.Windows.Forms.Timer> component is added at run time.</span></span> <span data-ttu-id="e692b-115">(Notez que Visual Studio contient un nombre de différents minuteurs ; dans ce cas, utiliser des formulaires Windows <xref:System.Windows.Forms.Timer> composant.</span><span class="sxs-lookup"><span data-stu-id="e692b-115">(Note that Visual Studio contains a number of different timers; in this case, use a Windows Forms <xref:System.Windows.Forms.Timer> component.</span></span> <span data-ttu-id="e692b-116">Pour plus d’informations sur les différents minuteurs dans Visual Studio, consultez [Introduction aux minuteurs serveur](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2008/tb9yt5e6(v=vs.90)).)</span><span class="sxs-lookup"><span data-stu-id="e692b-116">For more information about the different timers in Visual Studio, see [Introduction to Server-Based Timers](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2008/tb9yt5e6(v=vs.90)).)</span></span>

> [!CAUTION]
> <span data-ttu-id="e692b-117">Composants possèdent souvent des propriétés spécifiques au contrôle qui doivent être définies pour le composant de fonctionner efficacement.</span><span class="sxs-lookup"><span data-stu-id="e692b-117">Components often have control-specific properties that must be set for the component to function effectively.</span></span> <span data-ttu-id="e692b-118">Dans le cas de la <xref:System.Windows.Forms.Timer> composant ci-dessous, vous définissez le `Interval` propriété.</span><span class="sxs-lookup"><span data-stu-id="e692b-118">In the case of the <xref:System.Windows.Forms.Timer> component below, you set the `Interval` property.</span></span> <span data-ttu-id="e692b-119">Veillez, lorsque vous ajoutez des composants à votre projet, définissez les propriétés nécessaires pour ce composant.</span><span class="sxs-lookup"><span data-stu-id="e692b-119">Be sure, when adding components to your project, that you set the properties necessary for that component.</span></span>

## <a name="add-a-component-to-a-windows-form-programmatically"></a><span data-ttu-id="e692b-120">Ajouter un composant à un formulaire Windows par programmation</span><span class="sxs-lookup"><span data-stu-id="e692b-120">Add a component to a Windows Form programmatically</span></span>

1. <span data-ttu-id="e692b-121">Créez une instance de la <xref:System.Windows.Forms.Timer> classe dans le code.</span><span class="sxs-lookup"><span data-stu-id="e692b-121">Create an instance of the <xref:System.Windows.Forms.Timer> class in code.</span></span>

2. <span data-ttu-id="e692b-122">Définir le `Interval` propriété afin de déterminer la durée séparant les graduations de la minuterie.</span><span class="sxs-lookup"><span data-stu-id="e692b-122">Set the `Interval` property to determine the time between ticks of the timer.</span></span>

3. <span data-ttu-id="e692b-123">Configurer toutes les propriétés nécessaires pour votre composant.</span><span class="sxs-lookup"><span data-stu-id="e692b-123">Configure any other necessary properties for your component.</span></span>

     <span data-ttu-id="e692b-124">Le code suivant illustre la création d’un <xref:System.Windows.Forms.Timer> avec son `Interval` jeu de propriétés.</span><span class="sxs-lookup"><span data-stu-id="e692b-124">The following code shows the creation of a <xref:System.Windows.Forms.Timer> with its `Interval` property set.</span></span>

    ```vb
    Public Sub CreateTimer()
       Dim timerKeepTrack As New System.Windows.Forms.Timer
       timerKeepTrack.Interval = 1000
    End Sub
    ```

    ```csharp
    public void createTimer()
    {
       System.Windows.Forms.Timer timerKeepTrack = new
           System.Windows.Forms.Timer();
       timerKeepTrack.Interval = 1000;
    }
    ```

    ```cpp
    public:
       void createTimer()
       {
          System::Windows::Forms::Timer^ timerKeepTrack = gcnew
             System::Windows::Forms::Timer();
          timerKeepTrack->Interval = 1000;
       }
    ```

    > [!IMPORTANT]
    > <span data-ttu-id="e692b-125">Vous pouvez exposer votre ordinateur local à un risque de sécurité via le réseau en référençant un UserControl malveillant.</span><span class="sxs-lookup"><span data-stu-id="e692b-125">You might expose your local computer to a security risk through the network by referencing a malicious UserControl.</span></span> <span data-ttu-id="e692b-126">Il s’agit uniquement d’un problème dans le cas d’une personne malveillante, création d’un contrôle personnalisé causer des dommages, que vous suivi par inadvertance l’ajout à votre projet.</span><span class="sxs-lookup"><span data-stu-id="e692b-126">This would only be a concern in the case of a malicious person creating a damaging custom control, followed by you mistakenly adding it to your project.</span></span>

## <a name="see-also"></a><span data-ttu-id="e692b-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e692b-127">See also</span></span>

- [<span data-ttu-id="e692b-128">Contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e692b-128">Windows Forms Controls</span></span>](index.md)
- [<span data-ttu-id="e692b-129">Guide pratique pour Ajouter des contrôles aux Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e692b-129">How to: Add Controls to Windows Forms</span></span>](how-to-add-controls-to-windows-forms.md)
- [<span data-ttu-id="e692b-130">Guide pratique pour Ajouter des contrôles ActiveX aux Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e692b-130">How to: Add ActiveX Controls to Windows Forms</span></span>](how-to-add-activex-controls-to-windows-forms.md)
- [<span data-ttu-id="e692b-131">Guide pratique pour Copier des contrôles entre des Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e692b-131">How to: Copy Controls Between Windows Forms</span></span>](how-to-copy-controls-between-windows-forms.md)
- [<span data-ttu-id="e692b-132">Placement de contrôles dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e692b-132">Putting Controls on Windows Forms</span></span>](putting-controls-on-windows-forms.md)
- [<span data-ttu-id="e692b-133">Création d'étiquettes et de raccourcis pour les contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e692b-133">Labeling Individual Windows Forms Controls and Providing Shortcuts to Them</span></span>](labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)
- [<span data-ttu-id="e692b-134">Contrôles à utiliser dans les Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e692b-134">Controls to Use on Windows Forms</span></span>](controls-to-use-on-windows-forms.md)
- [<span data-ttu-id="e692b-135">Classement par fonction des contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e692b-135">Windows Forms Controls by Function</span></span>](windows-forms-controls-by-function.md)
