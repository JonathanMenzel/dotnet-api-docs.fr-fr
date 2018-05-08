### <a name="reflection-objects-can-no-longer-be-passed-from-managed-code-to-out-of-process-dcom-clients"></a><span data-ttu-id="4e5ff-101">Les objets de réflexion ne peuvent plus être passés du code managé aux clients DCOM hors processus</span><span class="sxs-lookup"><span data-stu-id="4e5ff-101">Reflection objects can no longer be passed from managed code to out-of-process DCOM clients</span></span>

|   |   |
|---|---|
|<span data-ttu-id="4e5ff-102">Détails</span><span class="sxs-lookup"><span data-stu-id="4e5ff-102">Details</span></span>|<span data-ttu-id="4e5ff-103">Les objets de réflexion ne peuvent plus être passés du code managé aux clients DCOM hors processus.</span><span class="sxs-lookup"><span data-stu-id="4e5ff-103">Reflection objects can no longer be passed from managed code to out-of-process DCOM clients.</span></span> <span data-ttu-id="4e5ff-104">Les types suivants sont concernés :</span><span class="sxs-lookup"><span data-stu-id="4e5ff-104">The following types are affected:</span></span><ul><li><xref:System.Reflection.Assembly?displayProperty=name></li><li><span data-ttu-id="4e5ff-105"><xref:System.Reflection.MemberInfo?displayProperty=name> (et ses types dérivés, dont <xref:System.Reflection.FieldInfo?displayProperty=name>, <xref:System.Reflection.MethodInfo?displayProperty=name>, <xref:System.Type?displayProperty=name> et <xref:System.Reflection.TypeInfo?displayProperty=name>)</span><span class="sxs-lookup"><span data-stu-id="4e5ff-105"><xref:System.Reflection.MemberInfo?displayProperty=name> (and its derived types, including <xref:System.Reflection.FieldInfo?displayProperty=name>, <xref:System.Reflection.MethodInfo?displayProperty=name>, <xref:System.Type?displayProperty=name>, and <xref:System.Reflection.TypeInfo?displayProperty=name>)</span></span></li><li><xref:System.Reflection.MethodBody?displayProperty=name></li><li><xref:System.Reflection.Module?displayProperty=name></li><li><span data-ttu-id="4e5ff-106"><xref:System.Reflection.ParameterInfo?displayProperty=name>.</span><span class="sxs-lookup"><span data-stu-id="4e5ff-106"><xref:System.Reflection.ParameterInfo?displayProperty=name>.</span></span></li></ul><span data-ttu-id="4e5ff-107">Les appels à <code>IMarshal</code> pour l’objet retournent <code>E_NOINTERFACE</code>.</span><span class="sxs-lookup"><span data-stu-id="4e5ff-107">Calls to <code>IMarshal</code> for the object return <code>E_NOINTERFACE</code>.</span></span>|
|<span data-ttu-id="4e5ff-108">Suggestion</span><span class="sxs-lookup"><span data-stu-id="4e5ff-108">Suggestion</span></span>|<span data-ttu-id="4e5ff-109">Mettez à jour le code de marshaling pour utiliser des objets autres que des objets de réflexion.</span><span class="sxs-lookup"><span data-stu-id="4e5ff-109">Update marshaling code to work with non-reflection objects</span></span>|
|<span data-ttu-id="4e5ff-110">Portée</span><span class="sxs-lookup"><span data-stu-id="4e5ff-110">Scope</span></span>|<span data-ttu-id="4e5ff-111">Mineur</span><span class="sxs-lookup"><span data-stu-id="4e5ff-111">Minor</span></span>|
|<span data-ttu-id="4e5ff-112">Version</span><span class="sxs-lookup"><span data-stu-id="4e5ff-112">Version</span></span>|<span data-ttu-id="4e5ff-113">4.6</span><span class="sxs-lookup"><span data-stu-id="4e5ff-113">4.6</span></span>|
|<span data-ttu-id="4e5ff-114">Type</span><span class="sxs-lookup"><span data-stu-id="4e5ff-114">Type</span></span>|<span data-ttu-id="4e5ff-115">Runtime</span><span class="sxs-lookup"><span data-stu-id="4e5ff-115">Runtime</span></span>|
