---
title: Désactiver RealTimeStylus pour les applications WPF
ms.date: 03/30/2017
ms.assetid: e0525309-5ede-4782-837d-dbf6e5554859
ms.openlocfilehash: ddf4a7f4488f957b2f413d61ad02aa59beba30f6
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33545660"
---
# <a name="disable-the-realtimestylus-for-wpf-applications"></a><span data-ttu-id="3056c-102">Désactiver RealTimeStylus pour les applications WPF</span><span class="sxs-lookup"><span data-stu-id="3056c-102">Disable the RealTimeStylus for WPF Applications</span></span>
<span data-ttu-id="3056c-103">Prise en charge pour le traitement d’entrée tactile Windows 7 intégrée Windows Presentation Foundation (WPF). La prise en charge est fournie via l’entrée de stylet en temps réel de la plateforme tablet en tant que <xref:System.Windows.UIElement.OnStylusDown%2A>, <xref:System.Windows.UIElement.OnStylusUp%2A>, et <xref:System.Windows.UIElement.OnStylusMove%2A> événements.</span><span class="sxs-lookup"><span data-stu-id="3056c-103">Windows Presentation Foundation (WPF) has built in support for processing Windows 7 touch input.The support comes through the tablet platform’s real-time stylus input as <xref:System.Windows.UIElement.OnStylusDown%2A>, <xref:System.Windows.UIElement.OnStylusUp%2A>, and <xref:System.Windows.UIElement.OnStylusMove%2A> events.</span></span> <span data-ttu-id="3056c-104">Windows 7 fournit également une entrée tactile en tant que messages de fenêtre WM_TOUCH Win32.</span><span class="sxs-lookup"><span data-stu-id="3056c-104">Windows 7 also provides multi-touch input as Win32 WM_TOUCH window messages.</span></span> <span data-ttu-id="3056c-105">Ces deux API s’excluent mutuellement sur le même HWND.</span><span class="sxs-lookup"><span data-stu-id="3056c-105">These two APIs are mutually exclusive on the same HWND.</span></span> <span data-ttu-id="3056c-106">Permettre l’entrée tactile via la plateforme Tablet PC (la valeur par défaut pour les applications WPF) désactive WM_TOUCH messages.</span><span class="sxs-lookup"><span data-stu-id="3056c-106">Enabling touch input via the tablet platform (the default for WPF applications) disables WM_TOUCH messages.</span></span> <span data-ttu-id="3056c-107">Par conséquent, pour utiliser WM_TOUCH pour recevoir des messages de contact à partir d’une fenêtre WPF, vous devez désactiver la prise en charge intégrée de stylet dans WPF.</span><span class="sxs-lookup"><span data-stu-id="3056c-107">As a result, to use WM_TOUCH to receive touch messages from a WPF window, you must disable the built-in stylus support in WPF.</span></span> <span data-ttu-id="3056c-108">Cela s’applique dans un scénario comme une fenêtre WPF hébergeant un composant qui utilise WM_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="3056c-108">This is applicable in a scenario such as a WPF window hosting a component that uses WM_TOUCH.</span></span>  
  
 <span data-ttu-id="3056c-109">Pour désactiver WPF à l’écoute de l’entrée du stylet, supprimez tout tablet prend désormais en charge par la fenêtre WPF.</span><span class="sxs-lookup"><span data-stu-id="3056c-109">To disable WPF listening to stylus input, remove any tablet support added by the WPF window.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3056c-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="3056c-110">Example</span></span>  
 <span data-ttu-id="3056c-111">L’exemple de code suivant montre comment supprimer la prise en charge de la plateforme de la tablette par défaut en utilisant la réflexion.</span><span class="sxs-lookup"><span data-stu-id="3056c-111">The following sample code shows how to remove the default tablet platform support by using reflection.</span></span>  
  
```  
public static void DisableWPFTabletSupport()  
{  
    // Get a collection of the tablet devices for this window.    
    TabletDeviceCollection devices = System.Windows.Input.Tablet.TabletDevices;  
  
    if (devices.Count > 0)  
    {     
        // Get the Type of InputManager.  
        Type inputManagerType = typeof(System.Windows.Input.InputManager);  
  
        // Call the StylusLogic method on the InputManager.Current instance.  
        object stylusLogic = inputManagerType.InvokeMember("StylusLogic",  
                    BindingFlags.GetProperty | BindingFlags.Instance | BindingFlags.NonPublic,  
                    null, InputManager.Current, null);  
  
        if (stylusLogic != null)  
        {  
            //  Get the type of the stylusLogic returned from the call to StylusLogic.  
            Type stylusLogicType = stylusLogic.GetType();  
  
            // Loop until there are no more devices to remove.  
            while (devices.Count > 0)  
            {  
                // Remove the first tablet device in the devices collection.  
                stylusLogicType.InvokeMember("OnTabletRemoved",  
                        BindingFlags.InvokeMethod | BindingFlags.Instance | BindingFlags.NonPublic,  
                        null, stylusLogic, new object[] { (uint)0 });  
            }                  
        }  
  
    }  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="3056c-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3056c-112">See Also</span></span>  
 [<span data-ttu-id="3056c-113">Interception d'entrée à partir du stylet</span><span class="sxs-lookup"><span data-stu-id="3056c-113">Intercepting Input from the Stylus</span></span>](../../../../docs/framework/wpf/advanced/intercepting-input-from-the-stylus.md)
