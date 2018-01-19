---
title: Framlengja virkni Microsoft Dynamics 365 for Talent
description: "Ef þú hefur búið til einhver Microsoft PowerApps geturðu opnað þau forrit frá tenglum innan Microsoft Dynamics 365 for Talent."
author: rschloma
manager: AnnBe
ms.date: 11/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-28
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: e1d0bbd71737001579218068e2ab0e02bc973f38
ms.contentlocale: is-is
ms.lasthandoff: 01/19/2018

---
# <a name="extend-the-functionality-of-microsoft-dynamics-365-for-talent"></a><span data-ttu-id="06ac8-103">Framlengja virkni Microsoft Dynamics 365 for Talent</span><span class="sxs-lookup"><span data-stu-id="06ac8-103">Extend the functionality of Microsoft Dynamics 365 for Talent</span></span>
<span data-ttu-id="06ac8-104">Ef þú hefur búið til einhver Microsoft PowerApps geturðu opnað þau forrit frá tenglum innan Microsoft Dynamics 365 for Talent.</span><span class="sxs-lookup"><span data-stu-id="06ac8-104">If you’ve created any Microsoft PowerApps, you can start those applications from links within Microsoft Dynamics 365 for Talent.</span></span> <span data-ttu-id="06ac8-105">Til að setja upp aðgang að forritunum þínum þarftu að setja upp nokkrar upplýsingar í Talent á forstillingasíðu sem þú getur opnað frá vinnusvæði **Kerfisstjórnun**.</span><span class="sxs-lookup"><span data-stu-id="06ac8-105">To set up access to your applications, you’ll need to set up some information in Talent on a configuration page that you can open from the **System administration** workspace.</span></span>

## <a name="configuring-embedded-powerapps-within-talent"></a><span data-ttu-id="06ac8-106">Grunnstilling innfelldra PowerApps innan Talent</span><span class="sxs-lookup"><span data-stu-id="06ac8-106">Configuring embedded PowerApps within Talent</span></span>
<span data-ttu-id="06ac8-107">Notaðu **Stilla innfelld Microsoft PowerApps** síðu til að forstilla Talent síður til að opna PowerApps forrit.</span><span class="sxs-lookup"><span data-stu-id="06ac8-107">Use the **Set embedded Microsoft PowerApps** page to configure Talent pages to start PowerApps applications.</span></span> <span data-ttu-id="06ac8-108">Til að opna **Stilla innfelld Microsoft PowerApps** síðuna skaltu opna **Kerfisstjórnun** vinnusvæði og opna síðan flipann **Tenglar**. Veldu **Microsoft PowerApps** úr **Uppsetning** hópnum.</span><span class="sxs-lookup"><span data-stu-id="06ac8-108">To open the **Set embedded Microsoft PowerApps** page, open the **System administration** workspace and then open the **Links** tab. Select **Microsoft PowerApps** from the **Setup** group.</span></span> 

<span data-ttu-id="06ac8-109">Eftirfarandi upplýsingar eru færðar inn eða stilltar á þessari síðu:</span><span class="sxs-lookup"><span data-stu-id="06ac8-109">The following information is entered or set on this page:</span></span> 

> - <span data-ttu-id="06ac8-110">Lýsandi heiti eða kennimerki fyrir hvert PowerApps forrit.</span><span class="sxs-lookup"><span data-stu-id="06ac8-110">A descriptive name or identifier for each PowerApps application.</span></span>
> - <span data-ttu-id="06ac8-111">Einkvæmt kennimerki (GUID) fyrir hvert forrit sem þú bætir við á Talent síðu.</span><span class="sxs-lookup"><span data-stu-id="06ac8-111">A unique identifier (GUID) for each application that you add to a Talent page.</span></span> <span data-ttu-id="06ac8-112">Kenni forrits er tiltækt á PowerApps svæðinu [powerapps.com](http://powerapps.com/).</span><span class="sxs-lookup"><span data-stu-id="06ac8-112">The app ID is available on the PowerApps site, [powerapps.com](http://powerapps.com/).</span></span> 
> - <span data-ttu-id="06ac8-113">Síðan þaðan sem notendur geta opnað forrit eða skýrslu.</span><span class="sxs-lookup"><span data-stu-id="06ac8-113">The page from which users can open an application or report.</span></span> <span data-ttu-id="06ac8-114">Ekki allar Talent síður styðja innfelld PowerApps og Power BI skýrslur.</span><span class="sxs-lookup"><span data-stu-id="06ac8-114">Not all Talent pages support embedded PowerApps and Power BI reports.</span></span> 

 > [!NOTE]
 >  <span data-ttu-id="06ac8-115">Sláðu inn innra nafn síðunnar, frekar en skjánafn sem birtist efst á síðunni.</span><span class="sxs-lookup"><span data-stu-id="06ac8-115">Enter the internal name of the page, rather than the display name that appears at the top of the page.</span></span> <span data-ttu-id="06ac8-116">Til að finna innri nafnið skaltu opna síðuna sem þú þarft innra nafnið á og hægrismella hvar sem er á síðunni.</span><span class="sxs-lookup"><span data-stu-id="06ac8-116">To find the internal name, open the page that you need the internal name of, and right-click anywhere on the page.</span></span> <span data-ttu-id="06ac8-117">Þegar valmyndin opnast skaltu sveima yfir **upplýsingar um skjámynd** atriðið.</span><span class="sxs-lookup"><span data-stu-id="06ac8-117">When the menu opens, hover over the **Form information** item.</span></span> <span data-ttu-id="06ac8-118">Innri skjámyndarnafnið birtist við hliðina á **Upplýsingar um skjámynd** atriðinu í valmyndinni.</span><span class="sxs-lookup"><span data-stu-id="06ac8-118">The internal form name is displayed next to the **Form information** item in the menu.</span></span>
 
> - <span data-ttu-id="06ac8-119">Tilgreindu skjámyndarstýringuna, þaðan sem forritið getur sótt samhengisgögn.</span><span class="sxs-lookup"><span data-stu-id="06ac8-119">Specify the form control from which the application can retrieve context data.</span></span> <span data-ttu-id="06ac8-120">Til dæmis gæti forrit notað gögn um starfsmaður.</span><span class="sxs-lookup"><span data-stu-id="06ac8-120">For example, an application might use data about a worker.</span></span> <span data-ttu-id="06ac8-121">Ef þú ferð inn á **Starfsmaður** síðuna í **Samhengi** reitnum opnast **Starfsmaður** síðan þegar þú opnar forritið.</span><span class="sxs-lookup"><span data-stu-id="06ac8-121">If you enter the **Worker** page in the **Context** field, the **Worker** page will open when you start the application.</span></span> <span data-ttu-id="06ac8-122">Færsla í **Samhengi** reitnum er valfrjálst.</span><span class="sxs-lookup"><span data-stu-id="06ac8-122">An entry in the **Context field** is optional.</span></span> 
> - <span data-ttu-id="06ac8-123">Stilla stærð svargluggans sem PowerApps forritin munu keyrast upp í.</span><span class="sxs-lookup"><span data-stu-id="06ac8-123">Set the size of the dialog box on which the PowerApps application will run.</span></span> <span data-ttu-id="06ac8-124">Svargluggarnir eru sjálfgefnir sem „lítill“ eða „stór“ til að fínstilla notendaviðmótið þegar forritið þitt er keyrt í síma eða á stærri tæki, eftir því sem við á.</span><span class="sxs-lookup"><span data-stu-id="06ac8-124">The dialog boxes are designated as “small” or “large” to optimize the user interface when your application for running on a phone or a larger device, respectively.</span></span> 

<span data-ttu-id="06ac8-125">Þú getur einnig tilgreint hvaða lögaðilar forritið verður í boði fyrir, eða þú getur gert það aðgengilegt öllum lögaðilum þínum.</span><span class="sxs-lookup"><span data-stu-id="06ac8-125">You can also specify which legal entities an application will be available for, or you can make it available to all your legal entities.</span></span> <span data-ttu-id="06ac8-126">Sjálfgefið er að PowerApps forritin þín eru í boði fyrir alla lögaðila.</span><span class="sxs-lookup"><span data-stu-id="06ac8-126">By default, your PowerApps applications are available to all legal entities.</span></span>

## <a name="opening-an-application"></a><span data-ttu-id="06ac8-127">Opna forrit</span><span class="sxs-lookup"><span data-stu-id="06ac8-127">Opening an application</span></span>
<span data-ttu-id="06ac8-128">Þegar þú hefur forstillt innfellt PowerApps forrit, verður tenglum á forritin sem þú tilgreindir bætt við síðurnar innan Talent.</span><span class="sxs-lookup"><span data-stu-id="06ac8-128">When you’ve configured embedded PowerApps applications, links to the applications that you specified will be added to the pages within Talent.</span></span> <span data-ttu-id="06ac8-129">Smella á tengil til að opna forrit.</span><span class="sxs-lookup"><span data-stu-id="06ac8-129">Click a link to open an application.</span></span> 



