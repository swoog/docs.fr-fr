---
title: Transmission d'un URI au Windows Runtime
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Windows Runtime, .NET Framework support for
- Windows Runtime, passing a URI to
ms.assetid: 3eb5ce6f-f304-4f87-8e81-0f25092f5ad4
author: mairaw
ms.author: mairaw
ms.openlocfilehash: c5ce0d4ac2b95dc4d51e785e3a00026f56c13d2c
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61921379"
---
# <a name="passing-a-uri-to-the-windows-runtime"></a><span data-ttu-id="c9e79-102">Transmission d'un URI au Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="c9e79-102">Passing a URI to the Windows Runtime</span></span>
<span data-ttu-id="c9e79-103">Les méthodes Windows Runtime n'acceptent que des URI absolus.</span><span class="sxs-lookup"><span data-stu-id="c9e79-103">Windows Runtime methods accept only absolute URIs.</span></span> <span data-ttu-id="c9e79-104">Si vous transmettez un URI relatif à une méthode [!INCLUDE[wrt](../../../includes/wrt-md.md)], une exception <xref:System.ArgumentException> est levée.</span><span class="sxs-lookup"><span data-stu-id="c9e79-104">If you pass a relative URI to a [!INCLUDE[wrt](../../../includes/wrt-md.md)] method, an <xref:System.ArgumentException> exception is thrown.</span></span> <span data-ttu-id="c9e79-105">En voici les raisons : Lorsque vous utilisez le [!INCLUDE[wrt](../../../includes/wrt-md.md)] dans le code .NET Framework, le <xref:Windows.Foundation.Uri?displayProperty=nameWithType> classe apparaît sous la forme <xref:System.Uri?displayProperty=nameWithType> dans Intellisense.</span><span class="sxs-lookup"><span data-stu-id="c9e79-105">Here's why: When you use the [!INCLUDE[wrt](../../../includes/wrt-md.md)] in .NET Framework code, the <xref:Windows.Foundation.Uri?displayProperty=nameWithType> class appears as <xref:System.Uri?displayProperty=nameWithType> in Intellisense.</span></span> <span data-ttu-id="c9e79-106">Le <xref:System.Uri?displayProperty=nameWithType> classe autorise les URI relatifs, mais la <xref:Windows.Foundation.Uri?displayProperty=nameWithType> n’est pas le cas de classe.</span><span class="sxs-lookup"><span data-stu-id="c9e79-106">The <xref:System.Uri?displayProperty=nameWithType> class allows relative URIs, but the <xref:Windows.Foundation.Uri?displayProperty=nameWithType> class does not.</span></span> <span data-ttu-id="c9e79-107">Il en va de même pour les méthodes que vous exposez dans les composants [!INCLUDE[wrt](../../../includes/wrt-md.md)].</span><span class="sxs-lookup"><span data-stu-id="c9e79-107">This is also true for methods you expose in [!INCLUDE[wrt](../../../includes/wrt-md.md)] Components.</span></span> <span data-ttu-id="c9e79-108">Si votre composant expose une méthode qui prend un URI, la signature dans votre code inclut <xref:System.Uri?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="c9e79-108">If your component exposes a method that takes a URI, the signature in your code includes <xref:System.Uri?displayProperty=nameWithType>.</span></span> <span data-ttu-id="c9e79-109">Toutefois, pour les utilisateurs de votre composant, la signature inclut <xref:Windows.Foundation.Uri?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="c9e79-109">However, to users of your component, the signature includes <xref:Windows.Foundation.Uri?displayProperty=nameWithType>.</span></span> <span data-ttu-id="c9e79-110">Un URI transmis à votre composant doit être un URI absolu.</span><span class="sxs-lookup"><span data-stu-id="c9e79-110">A URI that is passed to your component must be an absolute URI.</span></span>  
  
<span data-ttu-id="c9e79-111">Cette rubrique montre comment détecter un URI absolu et comment en créer un pendant le référencement d'une ressource dans le package d'application.</span><span class="sxs-lookup"><span data-stu-id="c9e79-111">This topic shows how to detect an absolute URI and how to create one when referring to a resource in the app package.</span></span>  
  
## <a name="detecting-and-using-an-absolute-uri"></a><span data-ttu-id="c9e79-112">Détection et utilisation d'un URI absolu</span><span class="sxs-lookup"><span data-stu-id="c9e79-112">Detecting and using an absolute URI</span></span>  
<span data-ttu-id="c9e79-113">Utilisez la propriété <xref:System.Uri.IsAbsoluteUri%2A?displayProperty=nameWithType> pour vous assurer qu'un URI est absolu avant de le transmettre au [!INCLUDE[wrt](../../../includes/wrt-md.md)].</span><span class="sxs-lookup"><span data-stu-id="c9e79-113">Use the <xref:System.Uri.IsAbsoluteUri%2A?displayProperty=nameWithType> property to ensure that a URI is absolute before passing it to the [!INCLUDE[wrt](../../../includes/wrt-md.md)].</span></span> <span data-ttu-id="c9e79-114">Utiliser cette propriété est plus efficace qu'intercepter et gérer l'exception <xref:System.ArgumentException>.</span><span class="sxs-lookup"><span data-stu-id="c9e79-114">Using this property is more efficient than catching and handling the <xref:System.ArgumentException> exception.</span></span>  
  
## <a name="using-an-absolute-uri-for-a-resource-in-the-app-package"></a><span data-ttu-id="c9e79-115">Utilisation d'un URI absolu pour une ressource dans le package d'application</span><span class="sxs-lookup"><span data-stu-id="c9e79-115">Using an absolute URI for a resource in the app package</span></span>  
<span data-ttu-id="c9e79-116">Si vous souhaitez spécifier un URI pour une ressource qui se trouve dans votre package d'application, vous pouvez utiliser le schéma `ms-appx` ou `ms-appx-web` pour créer un URI absolu.</span><span class="sxs-lookup"><span data-stu-id="c9e79-116">If you want to specify a URI for a resource that your app package contains, you can use the `ms-appx` or `ms-appx-web` scheme to create an absolute URI.</span></span>  
  
<span data-ttu-id="c9e79-117">L’exemple suivant montre comment définir le <xref:Windows.UI.Xaml.Controls.WebView.Source%2A> propriété pour un <xref:Windows.UI.Xaml.Controls.WebView> contrôle et le <xref:Windows.UI.Xaml.Controls.Image.Source%2A> propriété pour un <xref:Windows.UI.Xaml.Controls.Image> contrôle aux ressources qui sont contenus dans un dossier nommé Pages, à l’aide de XAML et code.</span><span class="sxs-lookup"><span data-stu-id="c9e79-117">The following example shows how to set the <xref:Windows.UI.Xaml.Controls.WebView.Source%2A> property for a <xref:Windows.UI.Xaml.Controls.WebView> control and the <xref:Windows.UI.Xaml.Controls.Image.Source%2A> property for an <xref:Windows.UI.Xaml.Controls.Image> control to resources that are contained in a folder named Pages, using both XAML and code.</span></span>  
  
[!code-xaml[System.URIToWindowsURI#1](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.uritowindowsuri/cs/mainpage.xaml#1)]  
[!code-csharp[System.URIToWindowsURI#2](../../../samples/snippets/csharp/VS_Snippets_CLR_System/system.uritowindowsuri/cs/mainpage.xaml.cs#2)]
[!code-vb[System.URIToWindowsURI#2](../../../samples/snippets/visualbasic/VS_Snippets_CLR_System/system.uritowindowsuri/vb/mainpage.xaml.vb#2)]  
  
<span data-ttu-id="c9e79-118">Pour plus d’informations sur ces schémas, consultez [modèles URI](/windows/uwp/app-resources/uri-schemes) dans le centre de développement Windows.</span><span class="sxs-lookup"><span data-stu-id="c9e79-118">For more information about these schemes, see [URI schemes](/windows/uwp/app-resources/uri-schemes) in the Windows Dev Center.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c9e79-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9e79-119">See also</span></span>

- [<span data-ttu-id="c9e79-120">Prise en charge .NET Framework pour les applications Windows Store et Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="c9e79-120">.NET Framework Support for Windows Store Apps and Windows Runtime</span></span>](../../../docs/standard/cross-platform/support-for-windows-store-apps-and-windows-runtime.md)
