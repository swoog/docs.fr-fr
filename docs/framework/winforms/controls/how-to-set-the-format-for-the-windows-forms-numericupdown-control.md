---
title: 'Procédure : Définir le Format pour le contrôle NumericUpDown Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- NumericUpDown control [Windows Forms], formatting values
- up-down controls [Windows Forms], formatting numeric values
ms.assetid: fa7c5557-6bfb-45b2-975d-8887b23b0ba0
ms.openlocfilehash: 5574faf858c32752cfa99b6bf339ddf06cb6b345
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54631007"
---
# <a name="how-to-set-the-format-for-the-windows-forms-numericupdown-control"></a><span data-ttu-id="4ba46-102">Procédure : Définir le Format pour le contrôle NumericUpDown Windows Forms</span><span class="sxs-lookup"><span data-stu-id="4ba46-102">How to: Set the Format for the Windows Forms NumericUpDown Control</span></span>
<span data-ttu-id="4ba46-103">Vous pouvez configurer la façon dont les valeurs sont affichées dans les formulaires Windows <xref:System.Windows.Forms.NumericUpDown> contrôle.</span><span class="sxs-lookup"><span data-stu-id="4ba46-103">You can configure how values are displayed in the Windows Forms <xref:System.Windows.Forms.NumericUpDown> control.</span></span> <span data-ttu-id="4ba46-104">Le <xref:System.Windows.Forms.NumericUpDown.DecimalPlaces%2A> propriété détermine le nombre de numéros s’affichent après la virgule décimale ; la valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="4ba46-104">The <xref:System.Windows.Forms.NumericUpDown.DecimalPlaces%2A> property determines how many numbers appear after the decimal point; the default is 0.</span></span> <span data-ttu-id="4ba46-105">Le <xref:System.Windows.Forms.NumericUpDown.ThousandsSeparator%2A> propriété détermine si un séparateur doit être inséré entre tous les trois chiffres décimaux ; la valeur par défaut est `false`.</span><span class="sxs-lookup"><span data-stu-id="4ba46-105">The <xref:System.Windows.Forms.NumericUpDown.ThousandsSeparator%2A> property determines whether a separator will be inserted between every three decimal digits; the default is `false`.</span></span> <span data-ttu-id="4ba46-106">Le contrôle peut afficher des valeurs au format hexadécimal au lieu du format décimal, si le <xref:System.Windows.Forms.NumericUpDown.Hexadecimal%2A> propriété est définie sur `true`; la valeur par défaut est `false`.</span><span class="sxs-lookup"><span data-stu-id="4ba46-106">The control can display values in hexadecimal instead of decimal format, if the <xref:System.Windows.Forms.NumericUpDown.Hexadecimal%2A> property is set to `true`; the default is `false`.</span></span>  
  
### <a name="to-format-the-numeric-value"></a><span data-ttu-id="4ba46-107">Pour mettre en forme la valeur numérique</span><span class="sxs-lookup"><span data-stu-id="4ba46-107">To format the numeric value</span></span>  
  
-   <span data-ttu-id="4ba46-108">Afficher une valeur décimale en définissant le <xref:System.Windows.Forms.NumericUpDown.DecimalPlaces%2A> propriété à un entier et en affectant la <xref:System.Windows.Forms.NumericUpDown.ThousandsSeparator%2A> propriété `true` ou `false`.</span><span class="sxs-lookup"><span data-stu-id="4ba46-108">Display a decimal value by setting the <xref:System.Windows.Forms.NumericUpDown.DecimalPlaces%2A> property to an integer and setting the <xref:System.Windows.Forms.NumericUpDown.ThousandsSeparator%2A> property to `true` or `false`.</span></span>  
  
    ```vb  
    NumericUpDown1.DecimalPlaces = 2  
    NumericUpDown1.ThousandsSeparator = True  
    ```  
  
    ```csharp  
    numericUpDown1.DecimalPlaces = 2;  
    numericUpDown1.ThousandsSeparator = true;  
    ```  
  
    ```cpp  
    numericUpDown1->DecimalPlaces = 2;  
    numericUpDown1->ThousandsSeparator = true;  
    ```  
  
     <span data-ttu-id="4ba46-109">ou</span><span class="sxs-lookup"><span data-stu-id="4ba46-109">-or-</span></span>  
  
-   <span data-ttu-id="4ba46-110">Affiche la valeur hexadécimale en définissant le <xref:System.Windows.Forms.NumericUpDown.Hexadecimal%2A> propriété `true`.</span><span class="sxs-lookup"><span data-stu-id="4ba46-110">Display a hexadecimal value by setting the <xref:System.Windows.Forms.NumericUpDown.Hexadecimal%2A> property to `true`.</span></span>  
  
    ```vb  
    NumericUpDown1.Hexadecimal = True  
    ```  
  
    ```csharp  
    numericUpDown1.Hexadecimal = true;  
    ```  
  
    ```cpp  
    numericUpDown1->Hexadecimal = true;  
    ```  
  
    > [!NOTE]
    >  <span data-ttu-id="4ba46-111">Même si la valeur est affichée sur le formulaire comme hexadécimal, tous les tests que vous effectuer sur le <xref:System.Windows.Forms.NumericUpDown.Value%2A> propriété Testez sa valeur décimale.</span><span class="sxs-lookup"><span data-stu-id="4ba46-111">Even if the value is displayed on the form as hexadecimal, any tests you perform on the <xref:System.Windows.Forms.NumericUpDown.Value%2A> property will be testing its decimal value.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4ba46-112">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4ba46-112">See also</span></span>
- <xref:System.Windows.Forms.NumericUpDown>
- [<span data-ttu-id="4ba46-113">NumericUpDown, contrôle</span><span class="sxs-lookup"><span data-stu-id="4ba46-113">NumericUpDown Control</span></span>](../../../../docs/framework/winforms/controls/numericupdown-control-windows-forms.md)
- [<span data-ttu-id="4ba46-114">Vue d’ensemble du contrôle NumericUpDown</span><span class="sxs-lookup"><span data-stu-id="4ba46-114">NumericUpDown Control Overview</span></span>](../../../../docs/framework/winforms/controls/numericupdown-control-overview-windows-forms.md)
