### <a name="previewlostkeyboardfocus-is-called-repeatedly-if-its-handler-shows-a-windows-forms-message-box"></a>PreviewLostKeyboardFocus est appelé de façon répétée si son gestionnaire affiche une boîte de message Windows Forms

|   |   |
|---|---|
|Détails|À compter de la version 4.5 du .NET Framework, quand vous appelez <code>System.Windows.Forms.MessageBox.Show</code> à partir d’un gestionnaire <xref:System.Windows.UIElement.PreviewLostKeyboardFocus>, le gestionnaire est redéclenché quand la boîte de message est fermée, ce qui peut aboutir à une boucle infinie de boîtes de message.|
|Suggestion|Il existe deux options pour contourner ce problème :<ol><li>Vous pouvez appeler <code>System.Windows.MessageBox.Show</code> au lieu de <code>System.Windows.Forms.MessageBox.Show</code>.</li><li>Vous pouvez afficher la boîte de message à partir d’un gestionnaire d’événements <xref:System.Windows.UIElement.LostKeyboardFocus> (au lieu du gestionnaire d’événements <xref:System.Windows.UIElement.PreviewLostKeyboardFocus?displayProperty=name>).</li></ol>|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Windows.ContentElement.PreviewLostKeyboardFocus?displayProperty=nameWithType></li><li><xref:System.Windows.IInputElement.PreviewLostKeyboardFocus?displayProperty=nameWithType></li><li><xref:System.Windows.UIElement.PreviewLostKeyboardFocus?displayProperty=nameWithType></li><li><xref:System.Windows.UIElement3D.PreviewLostKeyboardFocus?displayProperty=nameWithType></li></ul>|

