---
title: Désactiver RealTimeStylus pour les applications WPF
ms.date: 03/30/2017
ms.assetid: e0525309-5ede-4782-837d-dbf6e5554859
ms.openlocfilehash: 7b97a451c52b72ee1ddcec5c58e1848a0b10fb7e
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54616908"
---
# <a name="disable-the-realtimestylus-for-wpf-applications"></a><span data-ttu-id="715fa-102">Désactiver RealTimeStylus pour les applications WPF</span><span class="sxs-lookup"><span data-stu-id="715fa-102">Disable the RealTimeStylus for WPF Applications</span></span>
<span data-ttu-id="715fa-103">Prise en charge pour le traitement d’entrée tactile de Windows 7, Windows Presentation Foundation (WPF) a intégrée. La prise en charge est fournie par une entrée de stylet en temps réel de la plateforme Tablet PC en tant que <xref:System.Windows.UIElement.OnStylusDown%2A>, <xref:System.Windows.UIElement.OnStylusUp%2A>, et <xref:System.Windows.UIElement.OnStylusMove%2A> événements.</span><span class="sxs-lookup"><span data-stu-id="715fa-103">Windows Presentation Foundation (WPF) has built in support for processing Windows 7 touch input.The support comes through the tablet platform’s real-time stylus input as <xref:System.Windows.UIElement.OnStylusDown%2A>, <xref:System.Windows.UIElement.OnStylusUp%2A>, and <xref:System.Windows.UIElement.OnStylusMove%2A> events.</span></span> <span data-ttu-id="715fa-104">Windows 7 fournit également l’entrée multipoint sous forme de messages de fenêtre Win32 WM_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="715fa-104">Windows 7 also provides multi-touch input as Win32 WM_TOUCH window messages.</span></span> <span data-ttu-id="715fa-105">Ces deux API s’excluent mutuellement sur le même HWND.</span><span class="sxs-lookup"><span data-stu-id="715fa-105">These two APIs are mutually exclusive on the same HWND.</span></span> <span data-ttu-id="715fa-106">L’activation d’entrée tactile par le biais de la plate-forme Tablet PC (la valeur par défaut pour les applications WPF) désactive les messages WM_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="715fa-106">Enabling touch input via the tablet platform (the default for WPF applications) disables WM_TOUCH messages.</span></span> <span data-ttu-id="715fa-107">Par conséquent, pour utiliser WM_TOUCH pour recevoir des messages tactiles à partir d’une fenêtre WPF, vous devez désactiver la prise en charge intégrée de stylet dans WPF.</span><span class="sxs-lookup"><span data-stu-id="715fa-107">As a result, to use WM_TOUCH to receive touch messages from a WPF window, you must disable the built-in stylus support in WPF.</span></span> <span data-ttu-id="715fa-108">Cela s’applique dans un scénario telle qu’une fenêtre WPF hébergeant un composant qui utilise WM_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="715fa-108">This is applicable in a scenario such as a WPF window hosting a component that uses WM_TOUCH.</span></span>  
  
 <span data-ttu-id="715fa-109">Pour désactiver WPF à l’écoute à l’entrée du stylet, supprimez toute prise en charge de Tablet PC ajoutée par la fenêtre WPF.</span><span class="sxs-lookup"><span data-stu-id="715fa-109">To disable WPF listening to stylus input, remove any tablet support added by the WPF window.</span></span>  
  
## <a name="example"></a><span data-ttu-id="715fa-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="715fa-110">Example</span></span>  
 <span data-ttu-id="715fa-111">L’exemple de code suivant montre comment supprimer la prise en charge de la plateforme de la tablette par défaut en utilisant la réflexion.</span><span class="sxs-lookup"><span data-stu-id="715fa-111">The following sample code shows how to remove the default tablet platform support by using reflection.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="715fa-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="715fa-112">See also</span></span>
- [<span data-ttu-id="715fa-113">Interception d'entrée à partir du stylet</span><span class="sxs-lookup"><span data-stu-id="715fa-113">Intercepting Input from the Stylus</span></span>](../../../../docs/framework/wpf/advanced/intercepting-input-from-the-stylus.md)
