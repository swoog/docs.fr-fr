---
title: Informations d'accessibilité sur les contrôles d'un Windows Form
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms controls, accessibility
- controls [Windows Forms], accessibility
- accessibility [Windows Forms], Windows Forms controls
ms.assetid: 887dee6f-5059-4d57-957d-7c6fcd4acb10
ms.openlocfilehash: 0f589f37d79c9ec8d55153aac4c846726a379055
ms.sourcegitcommit: 5b6d778ebb269ee6684fb57ad69a8c28b06235b9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/08/2019
ms.locfileid: "59218327"
---
# <a name="providing-accessibility-information-for-controls-on-a-windows-form"></a><span data-ttu-id="f5734-102">Informations d'accessibilité sur les contrôles d'un Windows Form</span><span class="sxs-lookup"><span data-stu-id="f5734-102">Providing Accessibility Information for Controls on a Windows Form</span></span>
<span data-ttu-id="f5734-103">Les aides à l’accessibilité sont des programmes et des dispositifs spécialisés qui aident les personnes handicapées à utiliser plus efficacement les ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="f5734-103">Accessibility aids are specialized programs and devices that help people with disabilities use computers more effectively.</span></span> <span data-ttu-id="f5734-104">Tel est le cas notamment des lecteurs d’écran pour les non-voyants et des systèmes d’entrée vocale pour les personnes qui prononcent des commandes verbales au lieu d’utiliser la souris ou le clavier.</span><span class="sxs-lookup"><span data-stu-id="f5734-104">Examples include screen readers for people who are blind and voice input utilities for people who provide verbal commands instead of using the mouse or keyboard.</span></span> <span data-ttu-id="f5734-105">Ces aides à l’accessibilité interagissent avec les propriétés d’accessibilité exposées par les contrôles Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="f5734-105">These accessibility aids interact with the accessibility properties exposed by Windows Forms controls.</span></span> <span data-ttu-id="f5734-106">Ces propriétés sont :</span><span class="sxs-lookup"><span data-stu-id="f5734-106">These properties are:</span></span>  
  
-   **<span data-ttu-id="f5734-107">AccessibilityObject</span><span class="sxs-lookup"><span data-stu-id="f5734-107">AccessibilityObject</span></span>**  
  
-   **<span data-ttu-id="f5734-108">AccessibleDefaultActionDescription</span><span class="sxs-lookup"><span data-stu-id="f5734-108">AccessibleDefaultActionDescription</span></span>**  
  
-   **<span data-ttu-id="f5734-109">AccessibleDescription</span><span class="sxs-lookup"><span data-stu-id="f5734-109">AccessibleDescription</span></span>**  
  
-   **<span data-ttu-id="f5734-110">AccessibleName</span><span class="sxs-lookup"><span data-stu-id="f5734-110">AccessibleName</span></span>**  
  
-   **<span data-ttu-id="f5734-111">AccessibleRole</span><span class="sxs-lookup"><span data-stu-id="f5734-111">AccessibleRole</span></span>**  
  
## <a name="accessibilityobject-property"></a><span data-ttu-id="f5734-112">Propriété AccessibilityObject</span><span class="sxs-lookup"><span data-stu-id="f5734-112">AccessibilityObject Property</span></span>  
 <span data-ttu-id="f5734-113">Cette propriété en lecture seule contient une instance de la <xref:System.Windows.Forms.AccessibleObject> .</span><span class="sxs-lookup"><span data-stu-id="f5734-113">This read-only property contains an <xref:System.Windows.Forms.AccessibleObject> instance.</span></span> <span data-ttu-id="f5734-114">La classe **AccessibleObject** implémente l’interface <xref:Accessibility.IAccessible> , qui fournit des informations concernant la description, l’emplacement à l’écran, les capacités de navigation et la valeur du contrôle.</span><span class="sxs-lookup"><span data-stu-id="f5734-114">The **AccessibleObject** implements the <xref:Accessibility.IAccessible> interface, which provides information about the control's description, screen location, navigational abilities, and value.</span></span> <span data-ttu-id="f5734-115">Le concepteur définit cette valeur au moment d’ajouter le contrôle au formulaire.</span><span class="sxs-lookup"><span data-stu-id="f5734-115">The designer sets this value when the control is added to the form.</span></span>  
  
## <a name="accessibledefaultactiondescription-property"></a><span data-ttu-id="f5734-116">Propriété AccessibleDefaultActionDescription</span><span class="sxs-lookup"><span data-stu-id="f5734-116">AccessibleDefaultActionDescription Property</span></span>  
 <span data-ttu-id="f5734-117">Cette chaîne décrit l’action du contrôle.</span><span class="sxs-lookup"><span data-stu-id="f5734-117">This string describes the action of the control.</span></span> <span data-ttu-id="f5734-118">Elle n’apparaît pas dans la fenêtre Propriétés et peut uniquement être définie dans du code.</span><span class="sxs-lookup"><span data-stu-id="f5734-118">It does not appear in the Properties window and may only be set in code.</span></span> <span data-ttu-id="f5734-119">Dans l’exemple de code suivant, cette propriété est définie pour un contrôle bouton :</span><span class="sxs-lookup"><span data-stu-id="f5734-119">The following example sets this property for a button control:</span></span>  
  
```  
' Visual Basic  
Button1.AccessibleDefaultActionDescription = _  
   "Closes the application."  
  
// C#  
Button1.AccessibleDefaultActionDescription =   
   "Closes the application.";  
  
// C++  
button1->AccessibleDefaultActionDescription =  
   "Closes the application.";  
```  
  
## <a name="accessibledescription-property"></a><span data-ttu-id="f5734-120">Propriété AccessibleDescription</span><span class="sxs-lookup"><span data-stu-id="f5734-120">AccessibleDescription Property</span></span>  
 <span data-ttu-id="f5734-121">Cette chaîne décrit le contrôle.</span><span class="sxs-lookup"><span data-stu-id="f5734-121">This string describes the control.</span></span> <span data-ttu-id="f5734-122">Elle peut être définie dans la fenêtre Propriétés ou dans du code comme suit :</span><span class="sxs-lookup"><span data-stu-id="f5734-122">It may be set in the Properties window, or in code as follows:</span></span>  
  
```  
' Visual Basic  
Button1.AccessibleDescription = "A button with text 'Exit'."  
  
// C#  
Button1.AccessibleDescription = "A button with text 'Exit'";  
  
// C++  
button1->AccessibleDescription = "A button with text 'Exit'";  
```  
  
## <a name="accessiblename-property"></a><span data-ttu-id="f5734-123">Propriété AccessibleName</span><span class="sxs-lookup"><span data-stu-id="f5734-123">AccessibleName Property</span></span>  
 <span data-ttu-id="f5734-124">Il s’agit du nom d’un contrôle indiqué aux aides à l’accessibilité.</span><span class="sxs-lookup"><span data-stu-id="f5734-124">This is the name of a control reported to accessibility aids.</span></span> <span data-ttu-id="f5734-125">Elle peut être définie dans la fenêtre Propriétés ou dans du code comme suit :</span><span class="sxs-lookup"><span data-stu-id="f5734-125">It may be set in the Properties window, or in code as follows:</span></span>  
  
```  
' Visual Basic  
Button1.AccessibleName = "Order"  
  
// C#  
Button1.AccessibleName = "Order";  
  
// C++  
button1->AccessibleName = "Order";  
```  
  
## <a name="accessiblerole-property"></a><span data-ttu-id="f5734-126">Propriété AccessibleRole</span><span class="sxs-lookup"><span data-stu-id="f5734-126">AccessibleRole Property</span></span>  
 <span data-ttu-id="f5734-127">Cette propriété, qui contient une <xref:System.Windows.Forms.AccessibleRole> , décrit le rôle du contrôle dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="f5734-127">This property, which contains an <xref:System.Windows.Forms.AccessibleRole> enumeration, describes the user interface role of the control.</span></span> <span data-ttu-id="f5734-128">Un nouveau contrôle a la valeur `Default`.</span><span class="sxs-lookup"><span data-stu-id="f5734-128">A new control has the value set to `Default`.</span></span> <span data-ttu-id="f5734-129">Cela signifie que, par défaut, un contrôle **Button** (bouton) agit en tant que **Button**.</span><span class="sxs-lookup"><span data-stu-id="f5734-129">This would mean that by default, a **Button** control acts as a **Button**.</span></span> <span data-ttu-id="f5734-130">Vous pouvez éventuellement réinitialiser cette propriété si un contrôle a un autre rôle.</span><span class="sxs-lookup"><span data-stu-id="f5734-130">You may want to reset this property if a control has another role.</span></span> <span data-ttu-id="f5734-131">Par exemple, si vous utilisez un contrôle **PictureBox** (zone d’image) en tant que **Chart**(graphique), vous pouvez faire en sorte que les aides à l’accessibilité indique le rôle **Chart**, et non **PictureBox**.</span><span class="sxs-lookup"><span data-stu-id="f5734-131">For example, you may be using a **PictureBox** control as a **Chart**, and you may want accessibility aids to report the role as a **Chart**, not as a **PictureBox**.</span></span> <span data-ttu-id="f5734-132">Vous pouvez aussi spécifier cette propriété pour des contrôles personnalisés que vous avez développés.</span><span class="sxs-lookup"><span data-stu-id="f5734-132">You may also want to specify this property for custom controls you have developed.</span></span> <span data-ttu-id="f5734-133">Cette propriété être définie dans la fenêtre Propriétés ou dans du code comme suit :</span><span class="sxs-lookup"><span data-stu-id="f5734-133">This property may be set in the Properties window, or in code as follows:</span></span>  
  
```  
' Visual Basic  
PictureBox1.AccessibleRole = AccessibleRole.Chart  
  
// C#  
PictureBox1.AccessibleRole = AccessibleRole.Chart;  
  
// C++  
pictureBox1->AccessibleRole = AccessibleRole::Chart;  
```  
  
## <a name="see-also"></a><span data-ttu-id="f5734-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5734-134">See also</span></span>

- <xref:System.Windows.Forms.AccessibleObject>
- <xref:System.Windows.Forms.Control.AccessibilityObject%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.AccessibleDefaultActionDescription%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.AccessibleDescription%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.AccessibleName%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.AccessibleRole%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.AccessibleRole>
