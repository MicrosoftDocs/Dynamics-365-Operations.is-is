---
title: Vinna með leigusamninga í innflutningsramma leigusamnings
description: Þetta efnisatriði útskýrir hvernig á að nota innflutningsramma leigusamnings til að breyta mörgum leigusamningum samtímis.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 90727e8624c8edb7cd9458089dd9d6dfaad67a7f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207232"
---
# <a name="manage-leases-through-the-lease-import-framework"></a><span data-ttu-id="01e9a-103">Vinna með leigusamninga í innflutningsramma leigusamnings</span><span class="sxs-lookup"><span data-stu-id="01e9a-103">Manage leases through the Lease import framework</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01e9a-104">Þetta efnisatriði útskýrir hvernig á að nota innflutningsramma leigusamnings til að breyta mörgum leigusamningum í einu skrefi.</span><span class="sxs-lookup"><span data-stu-id="01e9a-104">This topic explains how to use the Lease import framework to adjust multiple leases in one step.</span></span> <span data-ttu-id="01e9a-105">Notaðu þennan eiginleika til að spara tíma og til að tryggja nákvæmari breytingar með því að draga úr líkum á mannlegum mistökum.</span><span class="sxs-lookup"><span data-stu-id="01e9a-105">By using this capability, you can save time, and you can also ensure more accurate adjustments by reducing the chance of human error.</span></span> <span data-ttu-id="01e9a-106">Þar að auki getur þessi eiginleiki tengt Microsoft Dynamics 365 Finance við ytri gagnaeiningar til að hlaða upp gögnum á skilvirkan hátt.</span><span class="sxs-lookup"><span data-stu-id="01e9a-106">Additionally, this capability can connect Microsoft Dynamics 365 Finance with external data entities to efficiently upload data.</span></span>

<span data-ttu-id="01e9a-107">Eftirfarandi gagnaeiningar er hægt að nota til að samþætta eignarleigu við ytri kerfi:</span><span class="sxs-lookup"><span data-stu-id="01e9a-107">The following data entities can be used to integrate Asset leasing with external systems:</span></span>

- <span data-ttu-id="01e9a-108">Undirbúningur leigusamnings</span><span class="sxs-lookup"><span data-stu-id="01e9a-108">Lease staging</span></span>
- <span data-ttu-id="01e9a-109">Undirbúningur greiðslusamnings</span><span class="sxs-lookup"><span data-stu-id="01e9a-109">Payment contract staging</span></span>
- <span data-ttu-id="01e9a-110">Undirbúningur rekstrarsamnings</span><span class="sxs-lookup"><span data-stu-id="01e9a-110">Executory contract staging</span></span>

<span data-ttu-id="01e9a-111">Hægt er að nota innflutningsferlið til að gera breytingar á leigusamningi, uppfæra aðrar upplýsingar en fjárhagsupplýsingar eða bæta við nýjum leigusamningum.</span><span class="sxs-lookup"><span data-stu-id="01e9a-111">You can use the import process to adjust a lease, update non-financial information, or add new leases.</span></span> <span data-ttu-id="01e9a-112">Hægt er að skoða og breyta gögnum leigusamningsins áður en þau eru flutt inn.</span><span class="sxs-lookup"><span data-stu-id="01e9a-112">You can view and edit the leasing data before you import it.</span></span>

<span data-ttu-id="01e9a-113">Kerfið getur keyrt eftirfarandi þrjú ferli í gegnum innflutningspakka leigusamningsins.</span><span class="sxs-lookup"><span data-stu-id="01e9a-113">The system can run the following three processes through the lease import suite.</span></span>

| <span data-ttu-id="01e9a-114">Gerð ferlis</span><span class="sxs-lookup"><span data-stu-id="01e9a-114">Process type</span></span>  | <span data-ttu-id="01e9a-115">lýsing</span><span class="sxs-lookup"><span data-stu-id="01e9a-115">Description</span></span> |
|---------------|-------------|
| <span data-ttu-id="01e9a-116">Bæta við færslu</span><span class="sxs-lookup"><span data-stu-id="01e9a-116">Add record</span></span>    | <span data-ttu-id="01e9a-117">Fluttir leigusamningar sem eru með þessa vinnslugerð stofna leigusamning í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="01e9a-117">Migrated leases that have this process type create a lease in the system.</span></span> <span data-ttu-id="01e9a-118">Greiðsluáætlunina þarf að staðfesta handvirkt og nauðsynlegt er að bóka fyrstu viðurkenndu bókarfærsluna handvirkt eftir flutninginn.</span><span class="sxs-lookup"><span data-stu-id="01e9a-118">The payment schedule must be manually confirmed, and the initial recognition journal entry must be manually posted after the migration.</span></span> |
| <span data-ttu-id="01e9a-119">Uppfæra færslu</span><span class="sxs-lookup"><span data-stu-id="01e9a-119">Update record</span></span> | <span data-ttu-id="01e9a-120">Fluttir leigusamningar sem eru með þessa gerð ferils uppfæra reitargildi fyrir leigusamning sem er þegar í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="01e9a-120">Migrated leases that have this process type update field values for a lease that is already in the system.</span></span> <span data-ttu-id="01e9a-121">Aðeins svæði valdin í **Val á uppfærslu svæða** eru uppfærð.</span><span class="sxs-lookup"><span data-stu-id="01e9a-121">Only the fields that have been selected on the **Update fields selection** page are updated.</span></span> <span data-ttu-id="01e9a-122">Mælt er með því að notandi velji svæði sem ekki eru fjárhagslegir á síðunni **Val á uppfærslu svæða** vegna þess að þessi gerð ferlis breytir ekki leigusamningnum.</span><span class="sxs-lookup"><span data-stu-id="01e9a-122">We recommended that you select non-financial fields on the **Update fields selection** page, because this process type doesn't adjust the lease.</span></span> |
| <span data-ttu-id="01e9a-123">Leiðrétta færslu</span><span class="sxs-lookup"><span data-stu-id="01e9a-123">Adjust record</span></span> | <span data-ttu-id="01e9a-124">Fluttir leigusamningar sem eru með þessa gerð ferlis gera breytingar á leigusamningnum.</span><span class="sxs-lookup"><span data-stu-id="01e9a-124">Migrated leases that have this process type adjust the lease.</span></span> <span data-ttu-id="01e9a-125">Þessi breyting veldur fjárhagsbreytingum á leigusamningnum.</span><span class="sxs-lookup"><span data-stu-id="01e9a-125">This adjustment causes a financial lease modification of the lease.</span></span> <span data-ttu-id="01e9a-126">Þegar búið er að vinna úr leigusamningnum stofnar kerfið nýja greiðsluáætlun með því að nota nýju gögnin úr innflutningspakka leigusamningsins.</span><span class="sxs-lookup"><span data-stu-id="01e9a-126">After the lease is processed, the system creates a new payment schedule by using the new data from the lease import suite.</span></span> <span data-ttu-id="01e9a-127">Kerfið staðfestir ekki greiðsluáætlunina né bókar færslu leiðréttingarbókar.</span><span class="sxs-lookup"><span data-stu-id="01e9a-127">The system doesn't confirm the payment schedule or post the adjustment journal entry.</span></span> |

<span data-ttu-id="01e9a-128">Eftir að upplýsingum hefur verið hlaðið upp í gegnum vinnusvæðið **Gagnastjórnun** skal opna síðuna **Flytja inn haus** (**Eignarleiga \> Innflutningsrammi leigusamnings \> Flytja inn haus**).</span><span class="sxs-lookup"><span data-stu-id="01e9a-128">After information is uploaded through the **Data management** workspace, open the **Import header** page (**Asset leasing \> Lease import framework \> Import header**).</span></span> <span data-ttu-id="01e9a-129">Þessi síða sýnir allan innflutning á þrem gagnaeiningum sem voru áður skráðar.</span><span class="sxs-lookup"><span data-stu-id="01e9a-129">This page lists all imports of the three data entities that were listed earlier.</span></span>

<span data-ttu-id="01e9a-130">Til að skoða sviðsetningargögn leigusamningsins áður en vinnsla er keyrð skal velja **Sviðsetningargögn**.</span><span class="sxs-lookup"><span data-stu-id="01e9a-130">To view the lease staging data before processing is run, select **Staging data**.</span></span>

<span data-ttu-id="01e9a-131">Samanburðaraðgerð gerir þér kleift að bera saman færslu sem þú ert að flytja inn við samsvarandi færslu sem er þegar í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="01e9a-131">The compare function lets you compare a record that you're importing with the corresponding record that's already in your system.</span></span> <span data-ttu-id="01e9a-132">Til að bera saman hverja færslu leigusamnings skal velja leigusamning og síðan velja **Bera saman**.</span><span class="sxs-lookup"><span data-stu-id="01e9a-132">To compare an individual lease record, select a lease, and then select **Compare**.</span></span> <span data-ttu-id="01e9a-133">Þú ættir að ljúka þessu skrefi til að búa til skýrslu um **Mismun** -skýrslu áður en þú flytur færslur leigusamningsins.</span><span class="sxs-lookup"><span data-stu-id="01e9a-133">You should complete this step to generate a **Differences** report before you migrate the lease records.</span></span> <span data-ttu-id="01e9a-134">Samanburðarvirkni ber saman gildin í sviðsetningargögnunum við gildi leigusamninga sem þegar eru í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="01e9a-134">The Compare functionality compares the values in the staging data to the values for leases that are currently in the system.</span></span>

> [!NOTE]
> <span data-ttu-id="01e9a-135">Samanburðarvirkni virkar ekki fyrir leigusamninga sem eru með **Bæta við færslu** gerð ferils, vegna þess að ekkert er til staðar til að bera saman við viðkomandi leigusamning.</span><span class="sxs-lookup"><span data-stu-id="01e9a-135">The Compare functionality doesn't work for leases that have the **Add record** process type, because there is nothing to compare against that lease.</span></span>
>
> <span data-ttu-id="01e9a-136">Til að bera saman marga leigusamninga samtímis er farið í **Eignarleiga \> Innflutningsrammi leigusamnings \> Reglubundið \> Bera saman** og velja **Bera saman**.</span><span class="sxs-lookup"><span data-stu-id="01e9a-136">To compare multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic \> Compare**, and select **Compare**.</span></span>

<span data-ttu-id="01e9a-137">Fyrir hverja einingu er hægt að skoða mismuninn á því sem er í kerfinu og hvað er í sviðsetningartöflunum.</span><span class="sxs-lookup"><span data-stu-id="01e9a-137">For each entity, you can view the differences between what is currently in the system and what is in the staging tables.</span></span> <span data-ttu-id="01e9a-138">Fyrir hverja einingu í sviðsetningartöflunum skal velja **Sjá mismun**.</span><span class="sxs-lookup"><span data-stu-id="01e9a-138">For each entity in the staging tables, select **See differences**.</span></span> <span data-ttu-id="01e9a-139">Svarglugginn sem birtist sýnir núverandi gildi og áætlað sviðsetningargildi.</span><span class="sxs-lookup"><span data-stu-id="01e9a-139">The dialog box that appears shows the current value and the proposed staging value.</span></span>

<span data-ttu-id="01e9a-140">Einnig er hægt að uppfæra sviðsetningargildið með því að breyta því í dálkinum **Nýtt gildi** og velja síðan **Uppfæra sviðsetningu**.</span><span class="sxs-lookup"><span data-stu-id="01e9a-140">You can also update the staging value by changing it in the **New Value** column and then selecting **Update staging**.</span></span>

<span data-ttu-id="01e9a-141">Hægt er að villuleita leigusamninga til að tryggja að hægt sé að færa færslurnar inn í kerfið villulaust.</span><span class="sxs-lookup"><span data-stu-id="01e9a-141">You can validate leases to ensure that the records can be brought into the system without introducing errors.</span></span> <span data-ttu-id="01e9a-142">Áður en færsla leigusamnings er flutt keyrir kerfið nokkrar villuleitir til að tryggja að færslan verði flutt inn.</span><span class="sxs-lookup"><span data-stu-id="01e9a-142">Before a lease record is migrated, the system runs several validations to ensure that the record will be successfully imported.</span></span> <span data-ttu-id="01e9a-143">Til að villuleita tiltekinn leigusamning skal velja **Villuleita**.</span><span class="sxs-lookup"><span data-stu-id="01e9a-143">To validate an individual lease, select **Validate**.</span></span>

> [!NOTE]
> <span data-ttu-id="01e9a-144">Til að villuleita marga leigusamninga samtímis er farið í **Eignarleiga \> Innflutningsrammi leigusamnings \> Reglubundið \> Villuleita** og velja **Bera saman**.</span><span class="sxs-lookup"><span data-stu-id="01e9a-144">To validate multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic \> Validate**, and select **Compare**.</span></span>

<span data-ttu-id="01e9a-145">Til að vinna úr tilteknum leigusamningi skal velja **Flytja gögn leigusamnings** á síðunni **Flytja inn haus**.</span><span class="sxs-lookup"><span data-stu-id="01e9a-145">To process an individual lease, select **Migrate lease records** on the **Import header** page.</span></span> <span data-ttu-id="01e9a-146">Þegar leigusamningur er fluttur framkvæmir kerfið aðgerðina sem er tilgreind í svæðinu **Gerð ferlis**.</span><span class="sxs-lookup"><span data-stu-id="01e9a-146">When a lease is migrated, the system performs the action that is specified in the **Process type** field.</span></span>

> [!NOTE]
> <span data-ttu-id="01e9a-147">Til að villuleita marga leigusamninga samtímis er farið í **Eignarleiga \> Innflutningsrammi leigusamnings \> Reglubundið \> Villuleita** og velja **Bera saman**.</span><span class="sxs-lookup"><span data-stu-id="01e9a-147">To validate multiple leases at the same time, go to **Asset leasing \> Lease import framework \> Periodic \> Validate**, and select **Compare**.</span></span>

<span data-ttu-id="01e9a-148">Eftir að leigusamningar eru bornir saman er hægt að keyra skýrslu til að skoða mismuninn á hverjum leigusamningi sem er innifalinn í innflutningskenninu.</span><span class="sxs-lookup"><span data-stu-id="01e9a-148">After the leases are compared, you can run a report to view the differences for each lease that is included in the import ID.</span></span> <span data-ttu-id="01e9a-149">Til að keyra þessa skýrslu fyrir einn leigusamning skal velja viðkomandi leigusamning í sviðsetningargögnum og velja svo **Bera saman og skoða skýrslu \> Skýrsla um mismun**.</span><span class="sxs-lookup"><span data-stu-id="01e9a-149">To run the report for one lease, select that lease in the staging data, and then select **Compare and view report \> Differences report**.</span></span>

> [!NOTE]
> <span data-ttu-id="01e9a-150">Til að villuleita marga leigusamninga samtímis er farið í **Eignarleiga \> Fyrirspurnir og skýrslur \> Skýrsla um mismun** og velja **Bera saman**.</span><span class="sxs-lookup"><span data-stu-id="01e9a-150">To validate multiple leases at the same time, go to **Asset leasing \> Inquiries and reports \> Differences report**, and select **Compare**.</span></span>

## <a name="set-up-update-fields"></a><span data-ttu-id="01e9a-151">Setja upp uppfærð svæði</span><span class="sxs-lookup"><span data-stu-id="01e9a-151">Set up update fields</span></span>

<span data-ttu-id="01e9a-152">Ef verið er að nota innflutningsramma leigusamnings til að uppfæra leigusamninga, og gerð ferlisins er **Uppfæra færslu** er hægt að velja tiltekin svæði til að uppfæra.</span><span class="sxs-lookup"><span data-stu-id="01e9a-152">If you're using the Lease import framework to update leases, and the process type is **Update record**, you can select specific fields to update.</span></span>

1. <span data-ttu-id="01e9a-153">Opnaðu **Eignarleiga \> Innflutningsrammi leigusamnings \> Uppsetning \> Uppfæra val á svæði**.</span><span class="sxs-lookup"><span data-stu-id="01e9a-153">Go to **Asset leasing \> Lease import framework \> Setup \> Update field selection**.</span></span>
2. <span data-ttu-id="01e9a-154">Á síðunni sem birtist eru svæði valin til að uppfæra og síðan er græna örin valin til að færa þau yfir í listann yfir **Valin svæði**.</span><span class="sxs-lookup"><span data-stu-id="01e9a-154">On the page that appears, select the fields to update, and then select the green arrow to move them to the **Selected fields** list.</span></span> <span data-ttu-id="01e9a-155">Aðeins er hægt að uppfæra svæði á listanum **Valin svæði** með því að nota innflutningspakka leigusamnings.</span><span class="sxs-lookup"><span data-stu-id="01e9a-155">Only fields in the **Selected fields** list can be updated by using the lease import suite.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]