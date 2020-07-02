---
title: Flutningur gagnagerðar gjaldmiðils fyrir tvöföld skrif
description: Þetta efnisatriði lýsir því hvernig á að breyta fjölda aukastafa sem tvöföld skrif styðja fyrir gjaldmiðil.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: 889337560f073708fb16b2dc173f9872593dd570
ms.sourcegitcommit: be4fcf8f19c55e852a729b215a16e24e971ff5b7
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/16/2020
ms.locfileid: "3456815"
---
# <a name="currency-data-type-migration-for-dual-write"></a><span data-ttu-id="78e83-103">Flutningur gagnagerðar gjaldmiðils fyrir tvöföld skrif</span><span class="sxs-lookup"><span data-stu-id="78e83-103">Currency data-type migration for dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="78e83-104">Hægt er að fjölga fjölda aukastafa sem eru studdir fyrir upphæðir gjaldmiðla upp í allt að 10.</span><span class="sxs-lookup"><span data-stu-id="78e83-104">You can increase the number of decimal places that are supported for currency values to a maximum of 10.</span></span> <span data-ttu-id="78e83-105">Sjálfgefin mörk eru fjórir aukastafir.</span><span class="sxs-lookup"><span data-stu-id="78e83-105">The default limit is four decimal places.</span></span> <span data-ttu-id="78e83-106">Ef aukastöfum er fjölgað er komið í veg fyrir gagnatap þegar tvöföld skrif eru notuð til að samstilla gögn.</span><span class="sxs-lookup"><span data-stu-id="78e83-106">By increasing the number of decimal places, you help prevent data loss when you use dual-write to sync data.</span></span> <span data-ttu-id="78e83-107">Fjölgun aukastafa er breyting sem þarf að velja sérstaklega.</span><span class="sxs-lookup"><span data-stu-id="78e83-107">The increase in the number of decimal places is an opt-in change.</span></span> <span data-ttu-id="78e83-108">Til að innleiða hana þarf að biðja Microsoft um aðstoð.</span><span class="sxs-lookup"><span data-stu-id="78e83-108">To implement it, you must request assistance from Microsoft.</span></span>

<span data-ttu-id="78e83-109">Leiðin til að breyta fjölda aukastafa felur í sér tvö skref:</span><span class="sxs-lookup"><span data-stu-id="78e83-109">The process of changing the number of decimal places has two steps:</span></span>

1. <span data-ttu-id="78e83-110">Biðja um flutning frá Microsoft.</span><span class="sxs-lookup"><span data-stu-id="78e83-110">Request migration from Microsoft.</span></span>
2. <span data-ttu-id="78e83-111">Breyta fjölda aukastafa í Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="78e83-111">Change the number of decimal places in Common Data Service.</span></span>

<span data-ttu-id="78e83-112">Forritið Finance and Operations og Common Data Service verða að styðja sama fjölda aukastafa í upphæðum gjaldmiðla.</span><span class="sxs-lookup"><span data-stu-id="78e83-112">The Finance and Operations app and Common Data Service must support the same number of decimal places in currency values.</span></span> <span data-ttu-id="78e83-113">Annars getur gagnatap orðið þegar þessar upplýsingar eru samstilltar milli forrita.</span><span class="sxs-lookup"><span data-stu-id="78e83-113">Otherwise, data loss can occur when this information is synced between apps.</span></span> <span data-ttu-id="78e83-114">Flutningsferlið endurstillir hvernig gildi gjaldmiðils og gengis eru vistuð en það breytir ekki neinum gögnum.</span><span class="sxs-lookup"><span data-stu-id="78e83-114">The migration process reconfigures the way that currency and exchange rate values are stored, but it doesn't change any data.</span></span> <span data-ttu-id="78e83-115">Þegar flutningnum er lokið eru fjölda aukastafa fyrir gjaldmiðilskóða og verðlagningu fjölgað og gögnin sem notendur slá inn og skoða eru með meiri nákvæmni.</span><span class="sxs-lookup"><span data-stu-id="78e83-115">After the migration is completed, the number of decimal places for currency codes and pricing can be increased, and the data that users enter and view can have more decimal precision.</span></span>

<span data-ttu-id="78e83-116">Flutningur er valfrjáls.</span><span class="sxs-lookup"><span data-stu-id="78e83-116">Migration is optional.</span></span> <span data-ttu-id="78e83-117">Ef þú gætir notið góðs af stuðningi fyrir fleiri aukastafi, mælum við með að þú hugleiðir flutning.</span><span class="sxs-lookup"><span data-stu-id="78e83-117">If you might benefit from support for more decimal places, we recommend that you consider migration.</span></span> <span data-ttu-id="78e83-118">Fyrirtæki sem ekki þurfa gildi með fleiri en fjórum aukastöfum þurfa ekki að breyta.</span><span class="sxs-lookup"><span data-stu-id="78e83-118">Organizations that don't require values that have more than four decimal places don't have to migrate.</span></span>

## <a name="requesting-migration-from-microsoft"></a><span data-ttu-id="78e83-119">Beðið um flutning frá Microsoft</span><span class="sxs-lookup"><span data-stu-id="78e83-119">Requesting migration from Microsoft</span></span>

<span data-ttu-id="78e83-120">Geymsla fyrir núverandi gjaldmiðilsreiti í Common Data Service getur ekki stutt meira en fjóra aukastafi.</span><span class="sxs-lookup"><span data-stu-id="78e83-120">Storage for existing currency fields in Common Data Service can't support more than four decimal places.</span></span> <span data-ttu-id="78e83-121">Í flutningsferlinu eru gildi gjaldmiðla þar af leiðandi afrituð í nýja innri reiti í gagnagrunninum.</span><span class="sxs-lookup"><span data-stu-id="78e83-121">Therefore, during the migration process, currency values are copied to new internal fields in the database.</span></span> <span data-ttu-id="78e83-122">Þetta ferli heldur samfleytt áfram þar til öll gögn hafa verið flutt.</span><span class="sxs-lookup"><span data-stu-id="78e83-122">This process occurs continuously until all data has been migrated.</span></span> <span data-ttu-id="78e83-123">Innan fyrirtækisins, við lok flutnings, taka nýju geymslugerðirnar við af þeim eldri en gagnagildin haldast óbreytt.</span><span class="sxs-lookup"><span data-stu-id="78e83-123">Internally, at the end of migration, the new storage types replace the old storage types, but the data values are unchanged.</span></span> <span data-ttu-id="78e83-124">Gjaldmiðilsreitirnir geta í kjölfarið stutt allt að 10 aukastafi.</span><span class="sxs-lookup"><span data-stu-id="78e83-124">The currency fields can then support up to 10 decimal places.</span></span> <span data-ttu-id="78e83-125">Meðan á flutningi stendur, er hægt að halda áfram að nota Common Data Service án truflunar.</span><span class="sxs-lookup"><span data-stu-id="78e83-125">During the migration process, Common Data Service can continue to be used without interruption.</span></span>

<span data-ttu-id="78e83-126">Á sama tíma er gengi breytt þannig að það styður allt að 12 aukastafi í stað núgildandi hámarks upp á 10.</span><span class="sxs-lookup"><span data-stu-id="78e83-126">At the same time, exchange rates are modified so that they support up to 12 decimal places instead of the current limit of 10.</span></span> <span data-ttu-id="78e83-127">Þörf er á þessari breytingu svo að fjöldi aukastafa sé sá sami í bæði Finance and Operations-forritinu og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="78e83-127">This change is required so that the number of decimal places is the same in both the Finance and Operations app and Common Data Service.</span></span>

<span data-ttu-id="78e83-128">Flutningur breytir engum gögnum.</span><span class="sxs-lookup"><span data-stu-id="78e83-128">Migration doesn't change any data.</span></span> <span data-ttu-id="78e83-129">Þegar reitum gjaldmiðils og gengis hefur verið breytt, geta stjórnendur stillt kerfið til að nota allt að 10 aukastafi fyrir gjaldmiðilsreiti með því að tilgreina fjölda aukastafa fyrir hvern gjaldmiðil færslu og fyrir verðlagningu.</span><span class="sxs-lookup"><span data-stu-id="78e83-129">After the currency and exchange rate fields are converted, admins can configure the system to use up to 10 decimal places for currency fields by specifying the number of decimal places for each transaction currency and for pricing.</span></span>

### <a name="request-a-migration"></a><span data-ttu-id="78e83-130">Óska eftir flutningi</span><span class="sxs-lookup"><span data-stu-id="78e83-130">Request a migration</span></span>

<span data-ttu-id="78e83-131">Til að gera þennan eiginleika tiltækan skal senda tölvupóst á **CDSExpandDecimal@microsoft.com** og láta eftirfarandi upplýsingar fylgja með:</span><span class="sxs-lookup"><span data-stu-id="78e83-131">To make this feature available, email **CDSExpandDecimal@microsoft.com**, and include the following information:</span></span>

+ <span data-ttu-id="78e83-132">**Efnisatriði:** Óska eftir því að virkja stuðning við fjölgun aukastafa fyrir \<organizationID\></span><span class="sxs-lookup"><span data-stu-id="78e83-132">**Subject:** Request to enable expanded decimal support for \<organizationID\></span></span>
+ <span data-ttu-id="78e83-133">**Meginmál:** Mig langar að virkja stuðning við fjölgun aukastafa fyrir fyrirtækið \<organizationID\>.</span><span class="sxs-lookup"><span data-stu-id="78e83-133">**Body:** I would like to enable expanded decimal support for my org \<organizationID\>.</span></span>

<span data-ttu-id="78e83-134">Fulltrúi Microsoft mun hafa samband við þig innan tveggja til þriggja virkra daga fyrir næstu skref.</span><span class="sxs-lookup"><span data-stu-id="78e83-134">A Microsoft representative will contact you within two to three business days for the next steps.</span></span>

<span data-ttu-id="78e83-135">Þegar beðið er um flutning ætti að hafa eftirfarandi upplýsingar í huga og gera viðeigandi ráðstafanir:</span><span class="sxs-lookup"><span data-stu-id="78e83-135">When you request a migration, you should be aware of the following details and plan for them accordingly:</span></span>

+ <span data-ttu-id="78e83-136">Tíminn sem þarf til að flytja gögnin fer eftir gagnamagni í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="78e83-136">The time that is required to migrate the data depends the amount of data in the system.</span></span> <span data-ttu-id="78e83-137">Flutningur stórra gagnagrunna getur tekið nokkra daga.</span><span class="sxs-lookup"><span data-stu-id="78e83-137">Migration of large databases can take several days.</span></span>
+ <span data-ttu-id="78e83-138">Stærð gagnagrunnsins eykst tímabundið meðan flutningur er í gangi vegna þess að þörf er á viðbótarplássi fyrir vísa.</span><span class="sxs-lookup"><span data-stu-id="78e83-138">The size of the database temporarily increases while the migration is running, because additional space is needed for indexes.</span></span> <span data-ttu-id="78e83-139">Meirihluti viðbótarplássins er losað þegar flutningi lýkur.</span><span class="sxs-lookup"><span data-stu-id="78e83-139">Most of the additional space is freed when the migration is completed.</span></span>
+ <span data-ttu-id="78e83-140">Í flutningsferlinu, ef villur koma upp sem koma í veg fyrir að flutningi ljúki, eykur kerfið viðvaranir til notendaþjónustu Microsoft þannig að starfsfólk notendaþjónustu geti gripið inn í.</span><span class="sxs-lookup"><span data-stu-id="78e83-140">During the migration process, if errors occur that prevent the migration from being completed, the system raise alerts to Microsoft Support, so that Support staff can intervene.</span></span> <span data-ttu-id="78e83-141">En jafnvel þó að villur komi upp við flutninginn, verður áfram hægt að nota Common Data Service að fullu.</span><span class="sxs-lookup"><span data-stu-id="78e83-141">However, even if errors occur during the migration, Common Data Service remains fully available for regular use.</span></span>
+ <span data-ttu-id="78e83-142">Flutningsferlið er ekki afturkræft.</span><span class="sxs-lookup"><span data-stu-id="78e83-142">The migration process isn't reversible.</span></span>

## <a name="changing-the-number-of-decimal-places"></a><span data-ttu-id="78e83-143">Fjölda aukastafa breytt</span><span class="sxs-lookup"><span data-stu-id="78e83-143">Changing the number of decimal places</span></span>

<span data-ttu-id="78e83-144">Þegar flutningi er lokið getur Common Data Service vistað tölur sem eru með fleiri aukastöfum.</span><span class="sxs-lookup"><span data-stu-id="78e83-144">After the migration is completed, Common Data Service can store numbers that have more decimal places.</span></span> <span data-ttu-id="78e83-145">Stjórnendur geta valið hversu margir aukastafir eru notaðir fyrir tiltekna gjaldmiðilskóða og verðlagningu.</span><span class="sxs-lookup"><span data-stu-id="78e83-145">Admins can choose how many decimal places are used for specific currency codes and for pricing.</span></span> <span data-ttu-id="78e83-146">Notendur Microsoft Power Apps, Power BI og Power Automate geta þá skoðað og notað tölur sem eru með fleiri aukastöfum.</span><span class="sxs-lookup"><span data-stu-id="78e83-146">Users of Microsoft Power Apps, Power BI, and Power Automate can then view and use numbers that have more decimal places.</span></span>

<span data-ttu-id="78e83-147">Til að gera þessa breytingu þarf að uppfæra eftirfarandi stillingar í Power Apps:</span><span class="sxs-lookup"><span data-stu-id="78e83-147">To make this change, you must update the following settings in Power Apps:</span></span>

+ <span data-ttu-id="78e83-148">**Kerfisstillingar: Gjaldmiðilsnákvæmni fyrir verðlagningu** - Reiturinn **Stilla gjaldmiðilsnákvæmni sem notuð er fyrir verðlagningu í öllu kerfinu** skilgreinir hvernig gjaldmiðillinn virkar fyrir fyrirtækið þegar **Nákvæmni í verðlagningu** er valið.</span><span class="sxs-lookup"><span data-stu-id="78e83-148">**System Settings: Currency precision for pricing** – The **Set the currency precision that is used for pricing throughout the system** field defines how the currency will behave for the organization when **Pricing Precision** is selected.</span></span>
+ <span data-ttu-id="78e83-149">**Viðskiptastjórnun: Gjaldmiðlar** - Reiturinn **Nákvæmni gjaldmiðils** gerir notanda kleift að tilgreina sérsniðinn fjölda aukastafa fyrir tiltekinn gjaldmiðil.</span><span class="sxs-lookup"><span data-stu-id="78e83-149">**Business Management: Currencies** – The **Currency Precision** field lets you specify a custom number of decimal places for a specific currency.</span></span> <span data-ttu-id="78e83-150">Til er varastilling fyrir fyrirtækjastillinguna.</span><span class="sxs-lookup"><span data-stu-id="78e83-150">There is a fallback to the organization-wide setting.</span></span>

<span data-ttu-id="78e83-151">Nokkrar takmarkanir eru til staðar:</span><span class="sxs-lookup"><span data-stu-id="78e83-151">There are some limitations:</span></span>

+ <span data-ttu-id="78e83-152">Ekki er hægt að stilla gjaldmiðilsreitinn í einingu.</span><span class="sxs-lookup"><span data-stu-id="78e83-152">You can't configure the currency field on an entity.</span></span>
+ <span data-ttu-id="78e83-153">Aðeins er hægt að tilgreina fleiri en fjóra aukastafi á stigunum **Verðlagning** og **Gjaldmiðill færslu**.</span><span class="sxs-lookup"><span data-stu-id="78e83-153">You can specify more than four decimal places only at the **Pricing** and **Transaction Currency** levels.</span></span>

### <a name="system-settings-currency-precision-for-pricing"></a><span data-ttu-id="78e83-154">Kerfisstillingar: Nákvæmni gjaldmiðils fyrir verðlagningu</span><span class="sxs-lookup"><span data-stu-id="78e83-154">System Settings: Currency precision for pricing</span></span>

<span data-ttu-id="78e83-155">Eftir að flutningi er lokið geta stjórnendur stillt nákvæmni gjaldmiðilsins.</span><span class="sxs-lookup"><span data-stu-id="78e83-155">After migration is completed, admins can set the currency precision.</span></span> <span data-ttu-id="78e83-156">Opnið **Stillingar \> Stjórnun** og veljið **Kerfisstillingar**.</span><span class="sxs-lookup"><span data-stu-id="78e83-156">Go to **Settings \> Administration**, and select **System Settings**.</span></span> <span data-ttu-id="78e83-157">Síðan skal, í flipanum **Almennt**, breyta gildinu á reitnum **Stilla nákvæmni gjaldmiðils sem notaður er fyrir verðlagningu í öllu kerfinu** eins og sýnt er á eftirfarandi skýringarmynd.</span><span class="sxs-lookup"><span data-stu-id="78e83-157">Then, on the **General** tab, change the value of the **Set the currency precision that is used for pricing throughout the system** field, as shown in the following illustration.</span></span>

![Kerfisstillingar fyrir gjaldmiðil](media/currency-system-settings.png)

### <a name="business-management-currencies"></a><span data-ttu-id="78e83-159">Viðskiptastjórnun: Gjaldmiðlar</span><span class="sxs-lookup"><span data-stu-id="78e83-159">Business Management: Currencies</span></span>

<span data-ttu-id="78e83-160">Ef nákvæmni gjaldmiðils fyrir tiltekinn gjaldmiðil þarf að vera önnur en fyrir nákvæmni gjaldmiðils sem notaður er fyrir verðlagningu, er hægt að breyta henni.</span><span class="sxs-lookup"><span data-stu-id="78e83-160">If you require that the currency precision for a specific currency differ from the currency precision that is used for pricing, you can change it.</span></span> <span data-ttu-id="78e83-161">Opnið **Stillingar \> Viðskiptastjórnun**, veljið **Gjaldmiðlar** og veljið gjaldmiðilinn sem á að breyta.</span><span class="sxs-lookup"><span data-stu-id="78e83-161">Go to **Settings \> Business Management**, select **Currencies**, and select the currency to change.</span></span> <span data-ttu-id="78e83-162">Stillið síðan reitinn **Nákvæmni gjaldmiðils** á þann fjölda aukastafa sem sóst er eftir eins og sýnt er á eftirfarandi skýringarmynd.</span><span class="sxs-lookup"><span data-stu-id="78e83-162">Then set the **Currency Precision** field to the number of decimal places that you want, as shown in the following illustration.</span></span>

![Stillingar gjaldmiðils fyrir ákveðinn stað](media/specific-currency.png)

### <a name="entities-currency-field"></a><span data-ttu-id="78e83-164">Einingar: Gjaldmiðilsreitur</span><span class="sxs-lookup"><span data-stu-id="78e83-164">Entities: Currency field</span></span>

<span data-ttu-id="78e83-165">Fjöldi aukastafa sem hægt er að stilla fyrir tiltekna gjaldmiðilsreiti takmarkast við fjóra.</span><span class="sxs-lookup"><span data-stu-id="78e83-165">The number of decimal places that can be configured for specific currency fields is limited to four.</span></span>
