### <a name="machinekeyencode-and-machinekeydecode-methods-are-now-obsolete"></a><span data-ttu-id="be079-101">Les méthodes MachineKey.Encode et MachineKey.Decode sont maintenant obsolètes</span><span class="sxs-lookup"><span data-stu-id="be079-101">MachineKey.Encode and MachineKey.Decode methods are now obsolete</span></span>

|   |   |
|---|---|
|<span data-ttu-id="be079-102">Détails</span><span class="sxs-lookup"><span data-stu-id="be079-102">Details</span></span>|<span data-ttu-id="be079-103">Ces méthodes sont désormais obsolètes.</span><span class="sxs-lookup"><span data-stu-id="be079-103">These methods are now obsolete.</span></span> <span data-ttu-id="be079-104">La compilation du code qui appelle ces méthodes génère un avertissement du compilateur.</span><span class="sxs-lookup"><span data-stu-id="be079-104">Compilation of code that calls these methods produces a compiler warning.</span></span>|
|<span data-ttu-id="be079-105">Suggestion</span><span class="sxs-lookup"><span data-stu-id="be079-105">Suggestion</span></span>|<span data-ttu-id="be079-106">Les alternatives recommandées sont <xref:System.Web.Security.MachineKey.Protect(System.Byte[],System.String[])> et <xref:System.Web.Security.MachineKey.Unprotect(System.Byte[],System.String[])>.</span><span class="sxs-lookup"><span data-stu-id="be079-106">The recommended alternatives are <xref:System.Web.Security.MachineKey.Protect(System.Byte[],System.String[])> and <xref:System.Web.Security.MachineKey.Unprotect(System.Byte[],System.String[])>.</span></span> <span data-ttu-id="be079-107">Vous pouvez également supprimer les avertissements de génération, ou les éviter en utilisant un compilateur plus ancien.</span><span class="sxs-lookup"><span data-stu-id="be079-107">Alternatively, the build warnings can be suppressed, or they can be avoided by using an older compiler.</span></span> <span data-ttu-id="be079-108">Ces API sont toujours prises en charge.</span><span class="sxs-lookup"><span data-stu-id="be079-108">The APIs are still supported.</span></span>|
|<span data-ttu-id="be079-109">Portée</span><span class="sxs-lookup"><span data-stu-id="be079-109">Scope</span></span>|<span data-ttu-id="be079-110">Mineur</span><span class="sxs-lookup"><span data-stu-id="be079-110">Minor</span></span>|
|<span data-ttu-id="be079-111">Version</span><span class="sxs-lookup"><span data-stu-id="be079-111">Version</span></span>|<span data-ttu-id="be079-112">4.5</span><span class="sxs-lookup"><span data-stu-id="be079-112">4.5</span></span>|
|<span data-ttu-id="be079-113">Type</span><span class="sxs-lookup"><span data-stu-id="be079-113">Type</span></span>|<span data-ttu-id="be079-114">Reciblage</span><span class="sxs-lookup"><span data-stu-id="be079-114">Retargeting</span></span>|
|<span data-ttu-id="be079-115">API affectées</span><span class="sxs-lookup"><span data-stu-id="be079-115">Affected APIs</span></span>|<ul><li><xref:System.Web.Security.MachineKey.Encode(System.Byte[],System.Web.Security.MachineKeyProtection)?displayProperty=nameWithType></li><li><xref:System.Web.Security.MachineKey.Decode(System.String,System.Web.Security.MachineKeyProtection)?displayProperty=nameWithType></li></ul>|
