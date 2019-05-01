---
title: Propriétés dans les contrôles Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- custom controls [Windows Forms], properties overview (using code)
- controls [Windows Forms], properties
- properties [Windows Forms]
ms.assetid: 2785279b-fb57-4937-8f6b-2050e475db6f
ms.openlocfilehash: e531b80cffabb94d2589383936a425b740c9cc07
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62012501"
---
# <a name="properties-in-windows-forms-controls"></a><span data-ttu-id="c45d7-102">Propriétés dans les contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c45d7-102">Properties in Windows Forms Controls</span></span>
<span data-ttu-id="c45d7-103">Un contrôle Windows Forms hérite de nombreuses propriétés de la classe de base <xref:System.Windows.Forms.Control?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="c45d7-103">A Windows Forms control inherits many properties form the base class <xref:System.Windows.Forms.Control?displayProperty=nameWithType>.</span></span> <span data-ttu-id="c45d7-104">Ceux-ci incluent des propriétés comme <xref:System.Windows.Forms.Control.Font%2A>, <xref:System.Windows.Forms.Control.ForeColor%2A>, <xref:System.Windows.Forms.Control.BackColor%2A>, <xref:System.Windows.Forms.Control.Bounds%2A>, <xref:System.Windows.Forms.Control.ClientRectangle%2A>, <xref:System.Windows.Forms.Control.DisplayRectangle%2A>, <xref:System.Windows.Forms.Control.Enabled%2A>, <xref:System.Windows.Forms.Control.Focused%2A>, <xref:System.Windows.Forms.Control.Height%2A>, <xref:System.Windows.Forms.Control.Width%2A>, <xref:System.Windows.Forms.Control.Visible%2A>, <xref:System.Windows.Forms.Control.AutoSize%2A>et bien d’autres.</span><span class="sxs-lookup"><span data-stu-id="c45d7-104">These include properties such as <xref:System.Windows.Forms.Control.Font%2A>, <xref:System.Windows.Forms.Control.ForeColor%2A>, <xref:System.Windows.Forms.Control.BackColor%2A>, <xref:System.Windows.Forms.Control.Bounds%2A>, <xref:System.Windows.Forms.Control.ClientRectangle%2A>, <xref:System.Windows.Forms.Control.DisplayRectangle%2A>, <xref:System.Windows.Forms.Control.Enabled%2A>, <xref:System.Windows.Forms.Control.Focused%2A>, <xref:System.Windows.Forms.Control.Height%2A>, <xref:System.Windows.Forms.Control.Width%2A>, <xref:System.Windows.Forms.Control.Visible%2A>, <xref:System.Windows.Forms.Control.AutoSize%2A>, and many others.</span></span> <span data-ttu-id="c45d7-105">Pour plus d’informations sur les propriétés héritées, consultez <xref:System.Windows.Forms.Control?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="c45d7-105">For details about inherited properties, see <xref:System.Windows.Forms.Control?displayProperty=nameWithType>.</span></span>  
  
 <span data-ttu-id="c45d7-106">Vous pouvez remplacer les propriétés héritées de votre contrôle, mais aussi définir de nouvelles propriétés.</span><span class="sxs-lookup"><span data-stu-id="c45d7-106">You can override inherited properties in your control as well as define new properties.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="c45d7-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="c45d7-107">In This Section</span></span>  
 [<span data-ttu-id="c45d7-108">Définition d’une propriété</span><span class="sxs-lookup"><span data-stu-id="c45d7-108">Defining a Property</span></span>](defining-a-property-in-windows-forms-controls.md)  
 <span data-ttu-id="c45d7-109">Explique comment implémenter une propriété pour un composant ou un contrôle personnalisé et comment intégrer la propriété dans l’environnement de conception.</span><span class="sxs-lookup"><span data-stu-id="c45d7-109">Shows how to implement a property for a custom control or component and shows how to integrate the property into the design environment.</span></span>  
  
 [<span data-ttu-id="c45d7-110">Définition de valeurs par défaut avec les méthodes ShouldSerialize et Reset</span><span class="sxs-lookup"><span data-stu-id="c45d7-110">Defining Default Values with the ShouldSerialize and Reset Methods</span></span>](defining-default-values-with-the-shouldserialize-and-reset-methods.md)  
 <span data-ttu-id="c45d7-111">Explique comment définir les valeurs de propriété par défaut pour un composant ou un contrôle personnalisé.</span><span class="sxs-lookup"><span data-stu-id="c45d7-111">Shows how to define default property values for a custom control or component.</span></span>  
  
 [<span data-ttu-id="c45d7-112">Événements de modification de propriété</span><span class="sxs-lookup"><span data-stu-id="c45d7-112">Property-Changed Events</span></span>](property-changed-events.md)  
 <span data-ttu-id="c45d7-113">Décrit comment activer les notifications de modification de propriété lorsqu’une valeur de propriété change.</span><span class="sxs-lookup"><span data-stu-id="c45d7-113">Describes how to enable property-change notifications when a property value changes.</span></span>  
  
 [<span data-ttu-id="c45d7-114">Guide pratique pour Exposer les propriétés des contrôles constitutifs</span><span class="sxs-lookup"><span data-stu-id="c45d7-114">How to: Expose Properties of Constituent Controls</span></span>](how-to-expose-properties-of-constituent-controls.md)  
 <span data-ttu-id="c45d7-115">Explique comment exposer les propriétés des contrôles constitutifs d’un contrôle composite personnalisé.</span><span class="sxs-lookup"><span data-stu-id="c45d7-115">Shows how to expose properties of constituent controls in a custom composite control.</span></span>  
  
 [<span data-ttu-id="c45d7-116">Implémentation de méthode dans les contrôles personnalisés</span><span class="sxs-lookup"><span data-stu-id="c45d7-116">Method Implementation in Custom Controls</span></span>](method-implementation-in-custom-controls.md)  
 <span data-ttu-id="c45d7-117">Décrit comment implémenter des méthodes dans des composants et des contrôles personnalisés.</span><span class="sxs-lookup"><span data-stu-id="c45d7-117">Describes how to implement methods in custom controls and components.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="c45d7-118">Référence</span><span class="sxs-lookup"><span data-stu-id="c45d7-118">Reference</span></span>  
 <xref:System.Windows.Forms.UserControl>  
 <span data-ttu-id="c45d7-119">Décrit la classe de base pour l’implémentation des contrôles composites.</span><span class="sxs-lookup"><span data-stu-id="c45d7-119">Documents the base class for implementing composite controls.</span></span>  
  
 <xref:System.ComponentModel.TypeConverterAttribute>  
 <span data-ttu-id="c45d7-120">Décrit l’attribut qui spécifie le <xref:System.ComponentModel.TypeConverter> à utiliser pour un type de propriété personnalisée.</span><span class="sxs-lookup"><span data-stu-id="c45d7-120">Documents the attribute that specifies the <xref:System.ComponentModel.TypeConverter> to use for a custom property type.</span></span>  
  
 <xref:System.ComponentModel.EditorAttribute>  
 <span data-ttu-id="c45d7-121">Décrit l’attribut qui spécifie le <xref:System.Drawing.Design.UITypeEditor> à utiliser pour une propriété personnalisée.</span><span class="sxs-lookup"><span data-stu-id="c45d7-121">Documents the attribute that specifies the <xref:System.Drawing.Design.UITypeEditor> to use for a custom property.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="c45d7-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c45d7-122">Related Sections</span></span>  
 [<span data-ttu-id="c45d7-123">Attributs dans les contrôles Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c45d7-123">Attributes in Windows Forms Controls</span></span>](attributes-in-windows-forms-controls.md)  
 <span data-ttu-id="c45d7-124">Décrit les attributs que vous pouvez appliquer aux propriétés ou aux autres membres de vos composants et contrôles personnalisés.</span><span class="sxs-lookup"><span data-stu-id="c45d7-124">Describes the attributes you can apply to properties or other members of your custom controls and components.</span></span>  
  
 <span data-ttu-id="c45d7-125">[Attributs en mode design pour les composants](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/tk67c2t8(v=vs.120))</span><span class="sxs-lookup"><span data-stu-id="c45d7-125">[Design-Time Attributes for Components](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/tk67c2t8(v=vs.120))</span></span>  
 <span data-ttu-id="c45d7-126">Répertorie les attributs de métadonnées à appliquer aux composants et aux contrôles pour qu'ils s'affichent correctement au moment du design dans les concepteurs visuels.</span><span class="sxs-lookup"><span data-stu-id="c45d7-126">Lists metadata attributes to apply to components and controls so that they are displayed correctly at design time in visual designers.</span></span>  
  
 <span data-ttu-id="c45d7-127">[Extension de la prise en charge au moment du design](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/37899azc(v=vs.120))</span><span class="sxs-lookup"><span data-stu-id="c45d7-127">[Extending Design-Time Support](https://docs.microsoft.com/previous-versions/visualstudio/visual-studio-2013/37899azc(v=vs.120))</span></span>  
 <span data-ttu-id="c45d7-128">Décrit comment implémenter des classes telles que les éditeurs et concepteurs qui fournissent la prise en charge au moment du design.</span><span class="sxs-lookup"><span data-stu-id="c45d7-128">Describes how to implement classes such as editors and designers that provide design-time support.</span></span>
