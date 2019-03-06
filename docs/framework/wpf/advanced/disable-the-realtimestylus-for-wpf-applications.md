---
title: Désactiver RealTimeStylus pour les applications WPF
ms.date: 03/30/2017
ms.assetid: e0525309-5ede-4782-837d-dbf6e5554859
ms.openlocfilehash: 6af7ff3addfe2673ab73ff0f977770f89c6234bb
ms.sourcegitcommit: 0c48191d6d641ce88d7510e319cf38c0e35697d0
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2019
ms.locfileid: "57371125"
---
# <a name="disable-the-realtimestylus-for-wpf-applications"></a>Désactiver RealTimeStylus pour les applications WPF
Prise en charge pour le traitement d’entrée tactile de Windows 7, Windows Presentation Foundation (WPF) a intégrée. La prise en charge est fournie par une entrée de stylet en temps réel de la plateforme Tablet PC en tant que <xref:System.Windows.UIElement.OnStylusDown%2A>, <xref:System.Windows.UIElement.OnStylusUp%2A>, et <xref:System.Windows.UIElement.OnStylusMove%2A> événements. Windows 7 fournit également l’entrée multipoint sous forme de messages de fenêtre Win32 WM_TOUCH. Ces deux API s’excluent mutuellement sur le même HWND. L’activation d’entrée tactile par le biais de la plate-forme Tablet PC (la valeur par défaut pour les applications WPF) désactive les messages WM_TOUCH. Par conséquent, pour utiliser WM_TOUCH pour recevoir des messages tactiles à partir d’une fenêtre WPF, vous devez désactiver la prise en charge intégrée de stylet dans WPF. Cela s’applique dans un scénario telle qu’une fenêtre WPF hébergeant un composant qui utilise WM_TOUCH.  
  
 Pour désactiver WPF à l’écoute à l’entrée du stylet, supprimez toute prise en charge de Tablet PC ajoutée par la fenêtre WPF.  
  
## <a name="example"></a>Exemple  
 L’exemple de code suivant montre comment supprimer la prise en charge de la plateforme de la tablette par défaut en utilisant la réflexion.  
  
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
  
## <a name="see-also"></a>Voir aussi
- [Interception d'entrée à partir du stylet](intercepting-input-from-the-stylus.md)
