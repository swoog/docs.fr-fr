### <a name="wpf-textboxtext-can-be-out-of-sync-with-databinding"></a>Dans WPF, TextBox.Text et la liaison de données peuvent être désynchronisés

|   |   |
|---|---|
|Détails|Dans certains cas, la propriété <xref:System.Windows.Controls.TextBox.Text> reflète une valeur précédente de la propriété liée aux données si cette propriété est modifiée au cours d'une opération d'écriture de liaison de données.|
|Suggestion|Cela ne doit pas avoir d'impact négatif. Vous pouvez, cependant, restaurer le comportement précédent en affectant à la propriété <xref:System.Windows.FrameworkCompatibilityPreferences.KeepTextBoxDisplaySynchronizedWithTextProperty> la valeur <code>false</code>.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Windows.Controls.TextBox.Text?displayProperty=nameWithType></li></ul>|

