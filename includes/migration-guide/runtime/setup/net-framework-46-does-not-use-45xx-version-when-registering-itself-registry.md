### <a name="the-net-framework-46-does-not-use-a-45xx-version-when-registering-itself-in-the-registry"></a>.NET Framework 4.6 n’utilise pas une version 4.5.x.x lors de son inscription dans le Registre

|   |   |
|---|---|
|Détails|Comme prévu, la clé de version définie dans le Registre (au niveau <code>HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\NET Framework Setup\NDP\v4\Full</code>) pour .NET Framework 4.6 commence par 4.6 et non 4.5. Les applications qui dépendent de ces clés de Registre pour savoir quelles versions du .NET Framework sont installées sur un ordinateur doivent être mises à jour afin de comprendre que 4.6 est une nouvelle version possible et qui est compatible avec les précédentes versions 4.5.x.|
|Suggestion|Mettez à jour les applications qui cherchent à découvrir une installation de .NET Framework 4.5 en recherchant les clés de Registre 4.5 pour accepter également 4.6.|
|Portée|Microsoft Edge|
|Version|4.6|
|Type|Runtime|

