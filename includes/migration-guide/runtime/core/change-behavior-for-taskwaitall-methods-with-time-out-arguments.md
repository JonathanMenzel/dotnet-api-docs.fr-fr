### <a name="change-in-behavior-for-taskwaitall-methods-with-time-out-arguments"></a>Changement de comportement des méthodes Task.WaitAll avec des arguments de délai d’attente

|   |   |
|---|---|
|Détails|Le comportement de Task.WaitAll est devenu plus cohérent dans .NET 4.5. Dans .NET Framework 4, le comportement de ces méthodes n’était pas cohérent. Lorsque le délai d'attente expirait, si une ou plusieurs tâches étaient terminées ou annulées avant l'appel de la méthode, la méthode levait une exception <xref:System.AggregateException?displayProperty=name>. Lorsque le délai d’attente expirait, si aucune tâche n’était terminée ou annulée avant l’appel de la méthode alors qu’une ou plusieurs tâches adoptaient ces états après l’appel de la méthode, la méthode retournait la valeur false.<br/><br/>Dans .NET Framework 4.5, ces surcharges de méthode retournent désormais la valeur false si des tâches sont toujours en cours d’exécution quand l’intervalle de délai d’attente expire, et elles ne lèvent une exception <xref:System.AggregateException?displayProperty=name> que si une tâche d’entrée a été annulée (que cette annulation soit intervenue avant ou après l’appel de méthode) et qu’aucune autre tâche n’est en cours d’exécution.|
|Suggestion|Si une exception <xref:System.AggregateException?displayProperty=name> a été interceptée dans le but de détecter une tâche ayant été annulée avant l’appel de WaitAll, ce code doit procéder à la même détection via la propriété IsCanceled (par exemple, .Any(t =&gt; t.IsCanceled)), puisque .NET 4.6 ne lève une exception que si toutes les tâches attendues sont terminées avant le délai d’attente.|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.Int32)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.Int32,System.Threading.CancellationToken)?displayProperty=nameWithType></li><li><xref:System.Threading.Tasks.Task.WaitAll(System.Threading.Tasks.Task[],System.TimeSpan)?displayProperty=nameWithType></li></ul>|

