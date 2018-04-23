### <a name="deadlock-may-result-when-using-reentrant-services"></a>Un blocage peut se produire lors de l’utilisation de services réentrants

|   |   |
|---|---|
|Détails|Un blocage peut survenir dans un service réentrant, ce qui limite les instances du service à un thread d’exécution à la fois. Les services susceptibles de rencontrer ce problème ont le <xref:System.ServiceModel.ServiceBehaviorAttribute> suivant dans leur code :<pre><code class="language-csharp">[ServiceBehavior(ConcurrencyMode = ConcurrencyMode.Reentrant)]&#13;&#10;</code></pre>|
|Suggestion|Pour résoudre ce problème, vous pouvez effectuer l’opération suivante :<ul><li>Définissez le mode d’accès concurrentiel du service sur <xref:System.ServiceModel.ConcurrencyMode.Single?displayProperty=nameWithType> ou sur &lt;System.ServiceModel.ConcurrencyMode.Multiple?displayProperty=nameWithType&gt;. Exemple :</li></ul><pre><code class="language-csharp">[ServiceBehavior(ConcurrencyMode = ConcurrencyMode.Single)]&#13;&#10;</code></pre><ul><li>Installez la dernière mise à jour sur .NET Framework 4.6.2 ou effectuez une mise à niveau vers une version ultérieure du .NET Framework. Cela désactive le flux de l’<xref:System.Threading.ExecutionContext> dans <xref:System.ServiceModel.OperationContext.Current?displayProperty=nameWithType>. Ce comportement est configurable. Cela équivaut à ajouter le paramètre d’application suivant à votre fichier de configuration :</li></ul><pre><code class="language-xml">&lt;appSettings&gt;&#13;&#10;&lt;add key=&quot;Switch.System.ServiceModel.DisableOperationContextAsyncFlow&quot; value=&quot;true&quot; /&gt;&#13;&#10;&lt;/appSettings&gt;&#13;&#10;&#13;&#10;The value of &#39;Switch.System.ServiceModel.DisableOperationContextAsyncFlow&#39; should never be set to &#39;false&#39; for Rentrant services.&#13;&#10;</code></pre>|
|Portée|Mineur|
|Version|4.6.2|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.ServiceModel.ServiceBehaviorAttribute?displayProperty=nameWithType></li><li><xref:System.ServiceModel.ConcurrencyMode.Reentrant?displayProperty=nameWithType></li></ul>|

