### <a name="winrt-stream-adapters-no-long-call-flushasync-automatically-on-close"></a>Les adaptateurs de flux WinRT n’appellent plus FlushAsync automatiquement lors de la fermeture

|   |   |
|---|---|
|Détails|Dans les applications du Windows Store, les adaptateurs de flux Windows Runtime n’appellent plus la méthode FlushAsync à partir de la méthode Dispose.|
|Suggestion|Cette modification devrait être transparente. Les développeurs peuvent rétablir le comportement précédent en écrivant du code comme le suivant :<pre><code class="language-csharp">using (var stream = GetWindowsRuntimeStream() as Stream)&#13;&#10;{&#13;&#10;// do something&#13;&#10;await stream.FlushAsync();&#13;&#10;}&#13;&#10;</code></pre>|
|Portée|Transparent|
|Version|4.5.1|
|Type|Runtime|

