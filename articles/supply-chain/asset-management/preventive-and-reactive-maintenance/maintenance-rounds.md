---
title: Viðhaldslotur
description: Þetta efni útskýrir viðhaldslotur í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a0ac4820d2efa37387382c2890e3ddc7dbc0878b
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875711"
---
# <a name="maintenance-rounds"></a><span data-ttu-id="39543-103">Viðhaldslotur</span><span class="sxs-lookup"><span data-stu-id="39543-103">Maintenance rounds</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="39543-104">Í **Eignastjórnun** er hægt er að stofna viðhaldslotur fyrir ýmsar eignir, þar sem þú þarft að framkvæma svipað verk með reglulegu millibili.</span><span class="sxs-lookup"><span data-stu-id="39543-104">In **Asset Management**, you can create maintenance rounds for various assets, on which you need to carry out a similar task at regular intervals.</span></span> <span data-ttu-id="39543-105">Til dæmis smurverk eða öryggisskoðunarstörf sem þarf að framkvæma á fjölda véla með sama millibili.</span><span class="sxs-lookup"><span data-stu-id="39543-105">For example, lubrication jobs or safety inspection jobs that need to be carried out on a number of machines within the same intervals.</span></span> <span data-ttu-id="39543-106">Fyrsta skrefið er að búa til viðhaldslotu, einnig á eignum sem krefjast sams konar viðhaldsverka.</span><span class="sxs-lookup"><span data-stu-id="39543-106">First step is to create a maintenance round, including assets that require the same form of maintenance job.</span></span> <span data-ttu-id="39543-107">Næst skipuleggur þú viðhaldsloturnar.</span><span class="sxs-lookup"><span data-stu-id="39543-107">Next, you schedule the maintenance rounds.</span></span> <span data-ttu-id="39543-108">Þegar þú hefur lokið áætlun um viðhaldsloturnar geturðu séð allar starfsskrárnar sem tengjast lotunni í **Allar viðhaldsáætlanir** og **Opnar viðhaldsáætlunarlínur**.</span><span class="sxs-lookup"><span data-stu-id="39543-108">When you have completed the maintenance rounds schedule, you can see all the job records relating to the round in the **All maintenance schedule** and **Open maintenance schedule lines**.</span></span>

>[!NOTE]
><span data-ttu-id="39543-109">Einnig er hægt að setja upp viðhaldslotur á virkum staðsetningum til að ljúka við á eignunum sem voru settar upp á virkri staðsetningu þegar stofnað var til lotubyggðrar verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="39543-109">Maintenance rounds can also be set up on functional locations to be completed on the assets installed on the functional location at the time of creation of the round-based work order.</span></span> <span data-ttu-id="39543-110">Sjá [Stofna virkar staðsetningar](../functional-locations/create-functional-locations.md) til að fá frekari upplýsingar um skipulag á viðhaldslotum á virkum stöðum.</span><span class="sxs-lookup"><span data-stu-id="39543-110">Refer to [Create functional locations](../functional-locations/create-functional-locations.md) for more information on the setup of maintenance rounds on functional locations.</span></span>

## <a name="set-up-a-maintenance-round"></a><span data-ttu-id="39543-111">Setja upp viðhaldslotu</span><span class="sxs-lookup"><span data-stu-id="39543-111">Set up a maintenance round</span></span>

1. <span data-ttu-id="39543-112">Smelltu á **Eignastjórnun** > **Uppsetning** > **Forvirkt viðhald** > **Viðhaldslotur**.</span><span class="sxs-lookup"><span data-stu-id="39543-112">Click **Asset management** > **Setup** > **Preventive maintenance** > **Maintenance rounds**.</span></span>

2. <span data-ttu-id="39543-113">Smelltu á **Nýtt** til að stofna nýja viðhaldslotu.</span><span class="sxs-lookup"><span data-stu-id="39543-113">Click **New** to create a new maintenance round.</span></span>

3. <span data-ttu-id="39543-114">Settu inn auðkenni í reitinn **Viðhaldslota** og heiti fyrir viðhaldsumferðina í reitinn **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="39543-114">Insert and ID in the **Maintenance round** field, and a name for the maintenance round in the **Name** field.</span></span>

4. <span data-ttu-id="39543-115">Veldu upphafsdagsetningu fyrir lotu í reitnum **Upphafsdagur**.</span><span class="sxs-lookup"><span data-stu-id="39543-115">Select a start date for the round in the **Start date** field.</span></span>

5. <span data-ttu-id="39543-116">Í reitunum **Ljúka innan daga** og **Ljúka innan klukkustunda** er hægt að setja inn áætlaða lokadagsetningu í dögum eða klukkustundum.</span><span class="sxs-lookup"><span data-stu-id="39543-116">In the **Finish within days** and **Finish within hours** fields, you can insert expected end date in days or hours.</span></span> <span data-ttu-id="39543-117">Væntanlegur lokadagur er reiknaður miðað við upphafsdaginn, sem reiknaður er þegar línur viðhaldsskema eru búnar til.</span><span class="sxs-lookup"><span data-stu-id="39543-117">The expected end date is calculated relative to the start date, which is calculated when maintenance schedule lines are created.</span></span> <span data-ttu-id="39543-118">Til dæmis er hægt að setja „7“ í reitinn **Ljúka innan daga** til að gefa til kynna að skyldri vinnslu skuli vera lokið innan viku frá upphafsdegi.</span><span class="sxs-lookup"><span data-stu-id="39543-118">For example, you can insert "7" in the **Finish within days** field to indicate that the related job should be completed within a week from the start date.</span></span>

6. <span data-ttu-id="39543-119">Veldu „Já“ á skiptihnappinum **Stofna sjálfvirkt** ef verkbeiðnir skulu vera sjálfkrafa stofnaðar út frá viðhaldsskemalínum sem eru búnar til úr þessari viðhaldslotu.</span><span class="sxs-lookup"><span data-stu-id="39543-119">Select "Yes" on the **Auto create** toggle button if work orders should automatically be created from maintenance schedule lines that are created from this maintenance round.</span></span>

7. <span data-ttu-id="39543-120">Í reitnum **Gerð verkbeiðni** velurðu þá gerð verkbeiðni sem á að nota í verkbeiðnum sem búnar eru til úr þessari viðhaldslotu.</span><span class="sxs-lookup"><span data-stu-id="39543-120">In the **Work order type** field, select the work order type to be used on work orders created from this maintenance round.</span></span>

8. <span data-ttu-id="39543-121">Í reitnum **Þjónustustig** velurðu það þjónustustig verkbeiðni sem á að nota í verkbeiðnum sem búnar eru til úr þessari viðhaldslotu.</span><span class="sxs-lookup"><span data-stu-id="39543-121">In the **Service level** field, select the work order service level to be used on work orders created from this maintenance round.</span></span>

9. <span data-ttu-id="39543-122">Á flýtiflipanum **Eignalínur** smellirðu á **Bæta við** til að bæta við eign í viðhaldslotunni.</span><span class="sxs-lookup"><span data-stu-id="39543-122">On the **Asset lines** FastTab, click **Add** to add an asset to the maintenance round.</span></span>

10. <span data-ttu-id="39543-123">Línunúmer er sjálfkrafa fært inn í reitinn **Línunúmer** til að sýna röð eigna í viðhaldslotu.</span><span class="sxs-lookup"><span data-stu-id="39543-123">A line number is automatically inserted in the **Line number** field to indicate the sequence of the assets in maintenance round.</span></span>

11. <span data-ttu-id="39543-124">Veljið eign í reitnum **Eign**.</span><span class="sxs-lookup"><span data-stu-id="39543-124">Select the asset in the **Asset** field.</span></span>

12. <span data-ttu-id="39543-125">Veldu gerð viðhaldsverka fyrir eignina í reitnum **Tegund viðhaldsverka**.</span><span class="sxs-lookup"><span data-stu-id="39543-125">Select the maintenance job type for the asset in the **Maintenance job type** field.</span></span>

13. <span data-ttu-id="39543-126">Veldu, ef þörf krefur **Afbrigði af gerð viðhaldsvinnslu** og **Viðskipti** sem tengjast tegund viðhaldsvinnslu.</span><span class="sxs-lookup"><span data-stu-id="39543-126">If required, select **Maintenance job typ variant** and **Trade** related to the maintenance job type.</span></span>

14. <span data-ttu-id="39543-127">Veldu endurtekningu (dag, viku osfrv.) í reitnum **Tímabilsgerð**.</span><span class="sxs-lookup"><span data-stu-id="39543-127">Select the recurrence (day, week, etc.) in the **Period type** field.</span></span>

15. <span data-ttu-id="39543-128">Í reitinn **Tímabilstíðni** seturðu inn fjölda endurtekninga fyrir viðhaldslotuna.</span><span class="sxs-lookup"><span data-stu-id="39543-128">In the **Period frequency** field, insert the number of recurrences for the maintenance round.</span></span> <span data-ttu-id="39543-129">Dæmi: Ef þú hefur valið „Dag“ í reitnum **Tímabilsgerð** og þú setur inn töluna „7“ í þennan reit, eru nýjar viðhaldslotulínur stofnaðar við tímasetningu á forvirku viðhaldi einu sinni í viku.</span><span class="sxs-lookup"><span data-stu-id="39543-129">Example: If you have selected "Day" in the **Period type** field, and you insert the number "7" in this field, new maintenance round lines are created during preventive maintenance scheduling once a week.</span></span>

16. <span data-ttu-id="39543-130">Veldu upphafsdagsetningu eignarinnar sem á að vera með í viðhaldslotunni í reitnum **Upphafsdagsetning**.</span><span class="sxs-lookup"><span data-stu-id="39543-130">Select a start date for the asset to be included in the maintenance round in the **Start date** field.</span></span> <span data-ttu-id="39543-131">Þessi dagsetning getur verið frábrugðin upphafsdeginum sem sett er fram í viðhaldsumlotunni.</span><span class="sxs-lookup"><span data-stu-id="39543-131">This date may differ from the start date set on the maintenance round.</span></span>

17. <span data-ttu-id="39543-132">Endurtakið þrep 9-16 til 16 til að bæta fleiri eignum við viðhaldslotuna.</span><span class="sxs-lookup"><span data-stu-id="39543-132">Repeat steps 9-16 to add more assets to the maintenance round.</span></span>

18. <span data-ttu-id="39543-133">Á flýtiflipanum **Línur virkrar staðsetningar** smellirðu á **Bæta við** til að bæta við virkri staðsetningu í viðhaldslotunni.</span><span class="sxs-lookup"><span data-stu-id="39543-133">On the **Functional location lines** FastTab, click **Add** to add a functional location to the maintenance round.</span></span> <span data-ttu-id="39543-134">Vísaðu til lýsingar á tengdum reitum hér að ofan.</span><span class="sxs-lookup"><span data-stu-id="39543-134">Refer to the description of the related fields above.</span></span> <span data-ttu-id="39543-135">Sömu reitir eru tiltækir og til að búa til eignalínu, en þú getur líka valið **Framleiðandi** og **Tegund** fyrir virka staðsetningu, ef þess er krafist.</span><span class="sxs-lookup"><span data-stu-id="39543-135">The same fields are available as for creating an asset line, but you can also select **Manufacturer** and **Model** for a functional location, if required.</span></span> <span data-ttu-id="39543-136">Ef þú velur aðeins virka staðsetningu á línu, en gerir ekkert val í **Gerð eignar**, **Framleiðandi**, **Tegund**, **Gerð viðhaldsverks**, **Afbrigði af viðhaldsverkum** og **Viðskipti** eru allar eignir sem tengjast þeirri virku staðsetningu á þeim tíma sem viðhaldsáætlun er tekin með í viðhaldslotunni.</span><span class="sxs-lookup"><span data-stu-id="39543-136">If you only select a functional location on a line, but make no selections in **Asset type**, **Manufacturer**, **Model**, **Maintenance job type**, **Maintenance job type variant** and **Trade**, all assets related to that functional location at the time of maintenance scheduling will be included in the maintenance round.</span></span>

19. <span data-ttu-id="39543-137">Á flýtiflipanum **Söfn** smellirðu á **Bæta við** til að velja verkbeiðnisafn sem á að vera með í viðhaldslotunni.</span><span class="sxs-lookup"><span data-stu-id="39543-137">On the **Pools** FastTab, click **Add** to select a work order pool to be included in the maintenance round.</span></span> <span data-ttu-id="39543-138">Hægt er að tengja nokkur verkbeiðnisöfn við eina viðhaldslotu.</span><span class="sxs-lookup"><span data-stu-id="39543-138">Several work order pools can be connected to one maintenance round.</span></span>

20. <span data-ttu-id="39543-139">Vistaðu uppsetninguna.</span><span class="sxs-lookup"><span data-stu-id="39543-139">Save your setup.</span></span>

>[!NOTE]
><span data-ttu-id="39543-140">Reitirnir **Eignir** og **Línur** sem eru staðsettir í hópnum **Upplýsingar** á flýtiflipanum **Haus** sýnir heildarfjölda eigna og lína sem tengjast valinni viðhaldslotu.</span><span class="sxs-lookup"><span data-stu-id="39543-140">The **Assets** and **Lines** fields located in the **Details** group on the **Header** FastTab show the total number of assets and lines related to the selected maintenance round.</span></span>

![Mynd 1](media/13-preventive-maintenance.png)


## <a name="schedule-maintenance-rounds"></a><span data-ttu-id="39543-142">Tímasetja viðhaldslotur</span><span class="sxs-lookup"><span data-stu-id="39543-142">Schedule maintenance rounds</span></span>

<span data-ttu-id="39543-143">Þegar þú hefur sett upp viðhaldslotu keyrirðu röðunarvinnslu til að tímasetja allar vinnslur sem tengjast viðhaldslotunni.</span><span class="sxs-lookup"><span data-stu-id="39543-143">When you have set up a maintenance round, you run a schedule job to schedule all the jobs related to the maintenance round.</span></span>

1. <span data-ttu-id="39543-144">Smelltu á **Eignastýring** > **Reglubundið** > **Forvirkt viðhald** > **Tímasetja viðhaldslotur**, eða **Eignastýring** > **Algengt** > **Viðhaldsskema** > **Öll viðhaldsskemu** eða **Opna viðhaldsskemalínur** eða **Opna viðhaldsskemasöfn** > veldu viðhaldsskemalínu á listanum > hnappinn **Viðhaldslotur**.</span><span class="sxs-lookup"><span data-stu-id="39543-144">Click **Asset management** > **Periodic** > **Preventive maintenance** > **Schedule maintenance rounds**, or **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines** or **Open maintenance schedule pools** > select maintenance schedule line in the list > **Maintenance rounds** button.</span></span>

2. <span data-ttu-id="39543-145">Í reitnum **Tímabil** skal velja tímabilsgerðina sem á að nota fyrir tímasetningarvinnsluna.</span><span class="sxs-lookup"><span data-stu-id="39543-145">In the **Period** field, select the period type to be used for the scheduling job.</span></span>

3. <span data-ttu-id="39543-146">Í reitinn **Tímabilstíðni** skaltu setja inn fjölda tímabila sem eiga að vera með í tímasetningarvinnslunni.</span><span class="sxs-lookup"><span data-stu-id="39543-146">In the **Period frequency** field, insert the number of periods to be included in the scheduling job.</span></span> <span data-ttu-id="39543-147">Upphaf tímasetningar er núverandi dagsetning.</span><span class="sxs-lookup"><span data-stu-id="39543-147">The start of the scheduling is the current date.</span></span>

4. <span data-ttu-id="39543-148">Veldu „Já“ á skiptihnappnum **Stofna sjálfvirkt** ef verkbeiðni á að vera sjálfkrafa stofnuð á grundvelli viðhaldslotu.</span><span class="sxs-lookup"><span data-stu-id="39543-148">Select "Yes" on the **Auto create** toggle button if a work order should automatically be created on the basis of a maintenance round.</span></span>

>[!NOTE]
><span data-ttu-id="39543-149">Ef þessi rofahnappur er stilltur á „Já“ og rofahnappurinn **Stofna sjálfvirkt** er einnig stilltur á „Já“ í viðhaldslotunni í skjámyndinni **Viðhaldslotur** eru verkbeiðnir búnar til út frá viðhaldslotulínum og viðhaldsskemalínur með stöðuna „Verkbeiðni stofnuð“ eru einnig stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="39543-149">If this toggle button is set to "Yes", and the **Auto create** toggle button is also set to "Yes" on the maintenance round in **Maintenance rounds** form, work orders are created based on the maintenance round lines, and maintenance schedule lines with status "Work order created" are also created.</span></span> <span data-ttu-id="39543-150">Ef aðeins einn af rofahnöppunum **Stofna sjálfkrafa** eru stilltir á „Já“ í þessari fellivalmynd eða í **Viðhaldslotur** eru aðeins viðhaldsskemalínur stofnaðar með stöðuna „Stofnað“.</span><span class="sxs-lookup"><span data-stu-id="39543-150">If only one of the **Auto create** toggle buttons is set to "Yes", in this drop-down or in **Maintenance rounds**, only maintenance schedule lines are created with status "Created".</span></span> <span data-ttu-id="39543-151">Þá eru engar verkbeiðnir stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="39543-151">In that case, no work orders are created.</span></span>

5. <span data-ttu-id="39543-152">Ef þess er krafist geturðu valið sérstakar lotur eða annan upphafsdag fyrir röðunarvinnsluna.</span><span class="sxs-lookup"><span data-stu-id="39543-152">If required, you can select specific rounds or another start date for the schedule job.</span></span> <span data-ttu-id="39543-153">Smelltu á **Sía** og bættu við lotum sem á að vera með.</span><span class="sxs-lookup"><span data-stu-id="39543-153">Click **Filter**, and add the rounds to be included.</span></span>

6. <span data-ttu-id="39543-154">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="39543-154">Click **OK**.</span></span>

7. <span data-ttu-id="39543-155">Núna geturðu séð viðhaldslotuvinnslurnar í **Eignastjórnun** > **Sameiginlegt** > **Viðhaldsskema** > **Öll viðhaldsskemu** eða **Opna viðhaldsskemalínur**.</span><span class="sxs-lookup"><span data-stu-id="39543-155">You are now able to see the maintenance rounds jobs in **Asset management** > **Common** > **Maintenance schedule** > **All maintenance schedule** or **Open maintenance schedule lines**.</span></span> <span data-ttu-id="39543-156">Ef tímasettar lotur eru tengdar við verkbeiðnisafn sérðu einnig viðhaldsskemalínur í **Opna viðhaldsskemasöfn**.</span><span class="sxs-lookup"><span data-stu-id="39543-156">If the scheduled rounds are connected to a work order pool, you also see maintenance schedule lines in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="39543-157">Viðhaldsskemalínur sem eru stofnaðar úr lotum hafa tilvísunargerðina „Viðhaldslotur“.</span><span class="sxs-lookup"><span data-stu-id="39543-157">Maintenance schedule lines created from a round have the reference type "Maintenance rounds".</span></span>

![Mynd 2](media/14-preventive-maintenance.png)

![Mynd 3](media/15-preventive-maintenance.png)

- <span data-ttu-id="39543-160">Þegar verkbeiðnir eru búnar til handvirkt á eignum sem falla undir ábyrgð lánadrottins er sýndur gluggi til að gera notandanum grein fyrir ábyrgðinni.</span><span class="sxs-lookup"><span data-stu-id="39543-160">When work orders are manually created on assets that are covered by a vendor warranty, a dialog box is shown to make the user aware of the warranty.</span></span> <span data-ttu-id="39543-161">Þá er hægt að hætta við að búa til verkbeiðnina.</span><span class="sxs-lookup"><span data-stu-id="39543-161">The creation of the work order can then be canceled.</span></span> <span data-ttu-id="39543-162">Hætt er við athugun á ábyrgðartengslum vegna verkbeiðna sem eru búnar til sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="39543-162">The check for a warranty relation is omitted for work orders that are automatically created.</span></span>  
- <span data-ttu-id="39543-163">Þú getur sett upp runuvinnslu á flýtiflipanum **Keyra í bakgrunni** til að skipuleggja lotur með reglulegu millibili.</span><span class="sxs-lookup"><span data-stu-id="39543-163">You can set up a batch job on the **Run in the background** FastTab to schedule rounds at regular intervals.</span></span>  
- <span data-ttu-id="39543-164">Ef lota er innifalin í nokkrum verkbeiðnisöfnum (sjá [Verkbeiðnisöfn](../work-orders/work-order-pools.md)) er sýnd ein skrá fyrir hvert safn í **Opna viðhaldsskemasöfn**.</span><span class="sxs-lookup"><span data-stu-id="39543-164">If a round is included in several work order pools (refer to [Work order pools](../work-orders/work-order-pools.md)), one record is shown for each pool in **Open maintenance schedule pools**.</span></span> <span data-ttu-id="39543-165">Þetta er gert til að hámarka síunarvalkosti fyrir verkbeiðnisöfn.</span><span class="sxs-lookup"><span data-stu-id="39543-165">This is done to optimize the filtering options for work order pools.</span></span>

