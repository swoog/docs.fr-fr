---
title: 'Procédure : définir le format du contrôle NumericUpDown Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- NumericUpDown control [Windows Forms], formatting values
- up-down controls [Windows Forms], formatting numeric values
ms.assetid: fa7c5557-6bfb-45b2-975d-8887b23b0ba0
ms.openlocfilehash: a5d8de6db8a0d6f62a082fc381a7b855eb948514
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64630608"
---
# <a name="how-to-set-the-format-for-the-windows-forms-numericupdown-control"></a>Procédure : définir le format du contrôle NumericUpDown Windows Forms
Vous pouvez configurer la façon dont les valeurs sont affichées dans les formulaires Windows <xref:System.Windows.Forms.NumericUpDown> contrôle. Le <xref:System.Windows.Forms.NumericUpDown.DecimalPlaces%2A> propriété détermine le nombre de numéros s’affichent après la virgule décimale ; la valeur par défaut est 0. Le <xref:System.Windows.Forms.NumericUpDown.ThousandsSeparator%2A> propriété détermine si un séparateur doit être inséré entre tous les trois chiffres décimaux ; la valeur par défaut est `false`. Le contrôle peut afficher des valeurs au format hexadécimal au lieu du format décimal, si le <xref:System.Windows.Forms.NumericUpDown.Hexadecimal%2A> propriété est définie sur `true`; la valeur par défaut est `false`.  
  
### <a name="to-format-the-numeric-value"></a>Pour mettre en forme la valeur numérique  
  
- Afficher une valeur décimale en définissant le <xref:System.Windows.Forms.NumericUpDown.DecimalPlaces%2A> propriété à un entier et en affectant la <xref:System.Windows.Forms.NumericUpDown.ThousandsSeparator%2A> propriété `true` ou `false`.  
  
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
  
     ou  
  
- Affiche la valeur hexadécimale en définissant le <xref:System.Windows.Forms.NumericUpDown.Hexadecimal%2A> propriété `true`.  
  
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
    >  Même si la valeur est affichée sur le formulaire comme hexadécimal, tous les tests que vous effectuer sur le <xref:System.Windows.Forms.NumericUpDown.Value%2A> propriété Testez sa valeur décimale.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.NumericUpDown>
- [NumericUpDown, contrôle](numericupdown-control-windows-forms.md)
- [Vue d’ensemble du contrôle NumericUpDown](numericupdown-control-overview-windows-forms.md)
