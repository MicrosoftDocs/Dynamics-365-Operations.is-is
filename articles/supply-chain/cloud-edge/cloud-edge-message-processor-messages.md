---
title: Skilaboð um skilaboðaúrvinnslu
description: Í þessu efnisatriði er að finna upplýsingar um skilaboðaeiginleika skilaboðaúrvinnslu fyrir vinnuálag einingakvarða.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysMessageProcessorMessage, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 03d8cad743ac2b2b1e7b2832b8272ca3dbf5a163
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021056"
---
# <a name="message-processor-messages"></a><span data-ttu-id="1b2cc-103">Skilaboð um skilaboðaúrvinnslu</span><span class="sxs-lookup"><span data-stu-id="1b2cc-103">Message processor messages</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="1b2cc-104">Skilaboð skilaboðaúrvinnslu eru notuð þegar einingakvarðar skýs og jaðra er keyrt fyrir [vinnuálag framleiðslu](cloud-edge-workload-manufacturing.md) og [vinnuálag vöruhúsakerfis](cloud-edge-workload-warehousing.md).</span><span class="sxs-lookup"><span data-stu-id="1b2cc-104">Message processor messages are used when running cloud and edge scale units for [manufacturing workloads](cloud-edge-workload-manufacturing.md) and [warehouse management workloads](cloud-edge-workload-warehousing.md).</span></span>

<span data-ttu-id="1b2cc-105">Mikið magn gagna fer á milli uppsetningarumhverfa miðstöðvar og einingakvarða til að halda þeim samstilltum, en *skilaboðaúrvinnslan* vinnur einungis úr nokkrum þessara gagnaskipta.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-105">A large amount of data is exchanged between the hub and scale unit deployment environments to keep them in sync, but only a few of these data exchanges will be processed by the *message processor*.</span></span> <span data-ttu-id="1b2cc-106">Hægt er að skoða skilaboðin sem skilaboðaúrvinnslan vinnur úr með því að fara í **Kerfisstjórnun > Skilaboðaúrvinnsla > Skilaboð skilaboðaúrvinnslu**.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-106">You can view the messages processed by the message processor by going to **System administration > Message processor > Message processor messages**.</span></span>

## <a name="message-grid-columns-and-filters"></a><span data-ttu-id="1b2cc-107">Dálkar og síur í skilaboðakerfi</span><span class="sxs-lookup"><span data-stu-id="1b2cc-107">Message grid columns and filters</span></span>

<span data-ttu-id="1b2cc-108">Hægt er að nota reitina efst á síðunni **Skilaboð skilaboðaúrvinnslu** til að auðvelda að finna ákveðin skilaboð sem leitað er að.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-108">You can use the fields at the top of the **Message processor messages** page to help find any particular messages you are looking for.</span></span> <span data-ttu-id="1b2cc-109">Flestar þessar síur passa við dálkhausana í skilaboðakerfinu.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-109">Most of these filters match the column headings in the message grid.</span></span> <span data-ttu-id="1b2cc-110">Eftirtaldar síur og dálkayfirskriftir eru tiltækar:</span><span class="sxs-lookup"><span data-stu-id="1b2cc-110">The following filters and column headings are available:</span></span>

- <span data-ttu-id="1b2cc-111">**Gerð skilaboða** – Tilgreinir gerð skilaboða.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-111">**Message type** – Specifies the type of message.</span></span>
- <span data-ttu-id="1b2cc-112">**Skilaboðabiðröð** – Tilgreinir heiti biðraðarinnar sem á að vinna skilaboðin í.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-112">**Message queue** – Specifies the name of the queue in which the message is to be processed.</span></span> <span data-ttu-id="1b2cc-113">Eftirfarandi biðraðir eru í boði:</span><span class="sxs-lookup"><span data-stu-id="1b2cc-113">The following queues are provided:</span></span>
  - <span data-ttu-id="1b2cc-114">*Einingarkvarði til miðstöðvar*</span><span class="sxs-lookup"><span data-stu-id="1b2cc-114">*Scale unit to hub*</span></span>
  - <span data-ttu-id="1b2cc-115">*Miðstöð fyrir kvörðunareiningu vöruhúsakeyrslu*</span><span class="sxs-lookup"><span data-stu-id="1b2cc-115">*Hub to warehouse execution scale unit*</span></span>
  - <span data-ttu-id="1b2cc-116">*Miðstöð fyrir framkvæmd framleiðslu kvörðunareiningar*</span><span class="sxs-lookup"><span data-stu-id="1b2cc-116">*Hub to manufacturing execution scale unit*</span></span>
- <span data-ttu-id="1b2cc-117">**Staða skilaboða** – Tilgreinir stöðu skilaboðanna.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-117">**Message state** – Specifies the state of the message.</span></span> <span data-ttu-id="1b2cc-118">Eftirfarandi stöður eru til:</span><span class="sxs-lookup"><span data-stu-id="1b2cc-118">The following states exists:</span></span>
  - <span data-ttu-id="1b2cc-119">*Í biðröð* – Skilaboðin eru tilbúin til vinnslu hjá skilaboðaúrvinnslunni.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-119">*Queued* – The message is ready to be processed by the message processor.</span></span>
  - <span data-ttu-id="1b2cc-120">*Meðhöndlað* – Skilaboðin voru unnin af skilaboðaforritinu.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-120">*Processed* – The message was successfully processed by the message processor.</span></span>
  - <span data-ttu-id="1b2cc-121">*Hætt við* - Skilaboðin voru unnin en úrvinnsla mistókst.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-121">*Canceled* – The message was processed, but processing failed.</span></span>
- <span data-ttu-id="1b2cc-122">**Efni skilaboða** – Þessi sía leitar að texta í öllu efni skilaboða.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-122">**Message content** – This filter does a full-text search of message content.</span></span> <span data-ttu-id="1b2cc-123">(Efni skilaboða er ekki sýnt í hnitanetinu.) Sían vinnur flest sértákn (á borð við „-“) sem bil og stafabilstákn sem Boole OR-virknitákn.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-123">(Message content is not shown in the grid.) The filter treats most special symbols (such as "-") as spaces, and treats all space characters as Boolean OR operators.</span></span> <span data-ttu-id="1b2cc-124">T=Til dæmis þýðir þetta að ef leitað er að tilteknu `journalid` gildi sem jafngildir „USMF-123456“ mun kerfið finna öll skilaboð sem innihalda „USMF“ eða „123456“, sem verður líklega langur listi.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-124">T=For example, this means if you search for a specific `journalid` value equal "USMF-123456", the system will find all messages that contain "USMF" or "123456", which is likely to be a long list.</span></span> <span data-ttu-id="1b2cc-125">Því væri betra að slá aðeins inn „123456“ því það skilar sértækari niðurstöðum.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-125">Therefore, it would be better to enter just "123456" alone because that will return more specific results.</span></span>

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a><span data-ttu-id="1b2cc-126">Dæmi um skilaboðagerð: Beiðni um fjárhagslega uppfærslu birgðaleiðréttingar</span><span class="sxs-lookup"><span data-stu-id="1b2cc-126">Example message type: Request inventory adjustment financial update</span></span>

<span data-ttu-id="1b2cc-127">Til dæmis er **Skilaboðagerðin** *Beiðni um fjárhagslega uppfærslu birgðaleiðréttingar* notuð til að stofna og bóka talningarbók í miðstöðinni þegar starfsmaður notar vöruhúsaforritið til að [skrá birgðaleiðréttingu](cloud-edge-warehouse-inventory-adjustment.md) í einingakvarða vinnuálags vöruhúsakerfis.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-127">For example, the **Message type** *Request inventory adjustment financial update* is used to create and post a counting journal on the hub when a worker uses the warehouse app to [register an inventory adjustment](cloud-edge-warehouse-inventory-adjustment.md) on a scale unit warehouse management workload.</span></span> <span data-ttu-id="1b2cc-128">Þar sem þetta tiltekna ferli er upprunnið úr einingakvarða mun reiturinn **Biðröð skilaboða** sýna gildið *Einingakvarði til miðstöðvar*.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-128">Because this specific process originates from a scale unit, the **Message queue** field will show the value *Scale unit to hub*.</span></span>

<span data-ttu-id="1b2cc-129">Fyrir þessa skilaboðategund skráir vinnuálag skilaboðin sem hluta af aðgerð til að leiðrétta birgðaskrá vöruhúsaforrits.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-129">For this message type, a scale unit workload records the message as part of a warehouse app inventory adjustment operation.</span></span> <span data-ttu-id="1b2cc-130">Gögn skilaboða eru síðan flutt til miðstöðvar sem hluti af sama ferlinu sem notað er fyrir [Skipulag Commerce Data Exchange](../../commerce/commerce-architecture.md).</span><span class="sxs-lookup"><span data-stu-id="1b2cc-130">The message data is then transferred to the hub as part of the same process used for the [Commerce data exchange architecture](../../commerce/commerce-architecture.md).</span></span> <span data-ttu-id="1b2cc-131">Skilaboðin verða uppfærð til að sýna **Staða skilaboða** sem *Í biðröð*.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-131">The message will be updated to show **Message state** as *Queued*.</span></span> <span data-ttu-id="1b2cc-132">Skilaboðaúrvinnslan reynir þá að vinna úr skilaboðunum og uppfærir **Stöðu skilaboða** í *Unnið* þegar tekst, eða *Hætt við* þegar mistekst.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-132">The message processor then attempts to process the message and updates the **Message state** to *Processed* on success, or *Canceled* on failure.</span></span>

## <a name="view-the-message-log-message-content-and-details"></a><span data-ttu-id="1b2cc-133">Skoða skilaboðaannál, innihald skilaboða og upplýsingar</span><span class="sxs-lookup"><span data-stu-id="1b2cc-133">View the message log, message content, and details</span></span>

<span data-ttu-id="1b2cc-134">Nákvæmar upplýsingar um skilaboð er hægt að finna með því að velja þau í hnitanetinu og síðan opna flipana **Kladdi** eða **Efni skilaboða** undir hnitaneti skilaboða þar sem hvert tilvik úrvinnslu er sýnt.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-134">You can find detailed information about a message by selecting it in the grid and then opening the **Log** or **Message content** tabs under the message grid, where each processing event is shown.</span></span>

<span data-ttu-id="1b2cc-135">**Efni skilaboða** fer eftir **Gerð skilaboða** og verður því með mismunandi textalengd.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-135">The **Message content** depends on the **Message type** and will therefore have different text length.</span></span> <span data-ttu-id="1b2cc-136">Dæmigerður texti um efni skilaboða hefst á **{** og endar á **}** og inn á milli með reitarheiti á borð við `journalId` og á eftir því **:** og gildi á borð við *USMF-123456*.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-136">A typical message content text will start with a **{** and end with a **}** and in between have field names such as `journalId` followed by a **:** and a value such as *USMF-123456*.</span></span>

<span data-ttu-id="1b2cc-137">Á tækjastikunni á flipanum **Kladdi** eru eftirfarandi hnappar:</span><span class="sxs-lookup"><span data-stu-id="1b2cc-137">The toolbar on the **Log** tab includes the following buttons:</span></span>

- <span data-ttu-id="1b2cc-138">**Kladdi** – Birtir úrvinnsluniðurstöðurnar.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-138">**Log** – Displays the processing results.</span></span> <span data-ttu-id="1b2cc-139">Þetta er sérstaklega gagnlegt til að skilja ástæður þess af hverju úrvinnsla skilaboða hafi mistekst með **Niðurstaða úrvinnslu** sem *Mistókst*.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-139">This is especially helpful for understanding the reasons for a processing failure for messages having a **Processing result** of *Failed*.</span></span>
- <span data-ttu-id="1b2cc-140">**Búnt** – Hægt er að keyra margar skilaboðaaðgerðir sem hluta af sömu runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-140">**Bundle** – Multiple message processing operations can run as part of the same batch process.</span></span> <span data-ttu-id="1b2cc-141">Velja þennan hnapp til að skoða þessi ítarlegu gögn.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-141">Select this button to view this detailed data.</span></span> <span data-ttu-id="1b2cc-142">Til dæmis er hægt að sjá hvort til séu tengingar sem krefjast þess að kerfið vinni úr ákveðnum skilaboðum í ákveðinni röð.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-142">For example, you can see whether dependencies exist that require the system to process certain messages in a specific sequence.</span></span>

## <a name="message-processor-batch-job"></a><span data-ttu-id="1b2cc-143">Runuvinnsla skilaboðaúrvinnslu</span><span class="sxs-lookup"><span data-stu-id="1b2cc-143">Message processor batch job</span></span>

<span data-ttu-id="1b2cc-144">Þegar skýja- og jaðrauppsetning er keyrð verður kallað sjálfkrafa á runuvinnsluna *Skilaboðaúrvinnsla* þegar ný skilaboð eru búin til fyrir úrvinnsluna, þannig að ekki ætti að vera þörf á því að tímasetja þessa vinnslu handvirkt.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-144">When running a cloud and edge deployment, the *Message processor* batch job will automatically be evoked when a new message is created for processing, so you should not need to schedule this job manually.</span></span>

<span data-ttu-id="1b2cc-145">Ef nauðsyn krefur er hægt að fá aðgang að runuvinnslunni með því að fara í **Kerfisstjórnun > Skilaboðaúrvinnsla > Skilaboðaúrvinnsla**.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-145">If necessary, you can access the batch job by going to **System administration > Message  processor > Message processor**.</span></span>

## <a name="manually-process-or-cancel-a-message"></a><span data-ttu-id="1b2cc-146">Vinna handvirkt úr eða hætta við skilaboð</span><span class="sxs-lookup"><span data-stu-id="1b2cc-146">Manually process or cancel a message</span></span>

<span data-ttu-id="1b2cc-147">Ef þörf krefur er hægt að vinna úr eða hætta við skilaboð handvirkt, allt eftir stöðu þeirra.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-147">If needed, you can manually process or cancel a message, depending on its current state.</span></span> <span data-ttu-id="1b2cc-148">Til að gera það skal velja skilaboðin í hnitanetinu og síðan velja **Vinna úr** eða **Hætta við** á aðgerðasvæðinu</span><span class="sxs-lookup"><span data-stu-id="1b2cc-148">To do so, select the message in the grid and then select **Process** or **Cancel** on the Action Pane</span></span>

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a><span data-ttu-id="1b2cc-149">Setja upp viðskiptatilvik til að senda viðvaranir vegna misheppnaðra úrvinnsluniðurstaðna</span><span class="sxs-lookup"><span data-stu-id="1b2cc-149">Set up business events to deliver alerts for failed processing results</span></span>

<span data-ttu-id="1b2cc-150">Auk þess að sía gildið fyrir **Skilaboðastöðuna** *Hætt við* til að grennslast fyrir um mislukkuð skilaboð, er hægt að setja upp [Viðskiptatilvik](../../fin-ops-core/dev-itpro/business-events/home-page.md) í miðstöðinni til að láta þegar úrvinnsla mistekst.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-150">In addition to filtering on the **Message state** value *Canceled* to inquire for failed messages, you can set up [Business events](../../fin-ops-core/dev-itpro/business-events/home-page.md) on the hub to alert you to failed processing results.</span></span> <span data-ttu-id="1b2cc-151">Til að gera það þarf að virkja viðskiptatilvikið sem kallast *Skilaboð skilaboðaúrvinnslu meðhöndluð* á síðunni **Efnisskrá viðskiptatilvika** (**Kerfisstjórnun > Uppsetning > Viðskiptatilvik > Efnisskrá viðskiptatilvika**).</span><span class="sxs-lookup"><span data-stu-id="1b2cc-151">To do so, activate the business event named *Message processor message processed*  on the **Business events catalog** page (**System administration > Setup > Business events > Business events catalog**).</span></span>

<span data-ttu-id="1b2cc-152">Sem hluti af virkjunarferlinu verður þér leiðbeint um hvernig á að tilgreina hvort tilvikið eigi við um einn eða alla lögaðila og gefa upp **Heiti endastöðvar**, sem þarf fyrst að skilgreina.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-152">As part of the activation process, you will be guided to specify whether the event is specific to one or all legal entities and provide an **Endpoint name**, which must be defined first.</span></span>

>[!NOTE]
> <span data-ttu-id="1b2cc-153">Ef **Þegar viðskiptatilvik á sér stað** er stillt á *Microsoft Power Automate* (frekar en til dæmis *HTTPS*) verður **Heiti endastöðvar** sjálfkrafa stofnað í Supply Chain Management samkvæmt *Microsoft Power Automate* uppsetningunni.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-153">If **When a Business Event occurs** is set to *Microsoft Power Automate* (rather than *HTTPS*, for example), the **Endpoint name** will automatically be created in Supply Chain Management based on the *Microsoft Power Automate* setup.</span></span>

### <a name="microsoft-power-automate-example"></a><span data-ttu-id="1b2cc-154">Microsoft Power Automate dæmi</span><span class="sxs-lookup"><span data-stu-id="1b2cc-154">Microsoft Power Automate example</span></span>

<span data-ttu-id="1b2cc-155">Í þessu dæmi skal nota **Þegar viðskiptatilvik á sér stað** með *Microsoft Power Automate* sendir tölvupósta sem innihalda InfoLog-skilaboð og tengla til að opna síðuna **Skilaboð skilaboðaúrvinnslu** fyrir tiltekin skilaboð sem mistókust í uppsetningu miðstöðvarinnar.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-155">In this example, use **When a Business Event occurs** with *Microsoft Power Automate* sends emails containing InfoLog messages and hyperlinks to open the **Message processor messages** page for a specific failed message on the hub deployment.</span></span> <span data-ttu-id="1b2cc-156">Ef þörf krefur er hægt að bæta við aukareglu til að senda tilkynningarnar samhliða með því að nota mismunandi rásir og stjórna viðtakendum samkvæmt gögnum tilviksins.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-156">If needed, you can add extra logic to send the notifications in parallel using different channels and control the recipients based on the event data.</span></span>

1. <span data-ttu-id="1b2cc-157">Í [Power Automate](https://preview.flow.microsoft.com) skal búa til nýtt sjálfvirkt skýjaflæði fyrir flæðisræsinguna **Þegar viðskiptatilvik á sér stað - Forrit Fin & Ops (Dynamics 365)** og í kjölfarið fylgja skrefin **Þátta JSON** og **Senda tölvupóst** eins og sýnt er á eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-157">In [Power Automate](https://preview.flow.microsoft.com), create a new automated cloud flow for the flow trigger **When a Business Event occurs - Fin & Ops App (Dynamics 365)** followed by the **Parse JSON** and **Send an email** steps, as shown in the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="Power Automate sjálfvirkt skýjaflæði":::

1. <span data-ttu-id="1b2cc-159">Í skrefinu **Þegar viðskiptatilvik á sér stað** er hægt að fletta upp eða færa inn miðstöðina **Tilvik** sem fylgir á eftir **Flokknum** og síðan **Viðskiptatilvikið** *Skilaboð skilaboðaúrvinnslu meðhöndluð* eins og sýnt er á eftirfarandi mynd.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-159">In the **When a Business Event occurs** step, you can look up or enter the hub **Instance** following the **Category** and then the **Business event** *Message processor message processed*, as shown in the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Power Automate Þegar skref viðskiptaviðburðar á sér stað":::

1. <span data-ttu-id="1b2cc-161">Fyrir skrefið **Þátta JSON** skal færa inn **Skema** sem skilgreinir stækkaða reiti.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-161">For the **Parse JSON** step, enter a **Schema** that defines the extended fields.</span></span> <span data-ttu-id="1b2cc-162">Hægt er að nota valkostinn *Sækja skema* á síðunni **Efnisskrá viðskiptatilvika** í Supply Chain Management eða byrja á því að líma inn textadæmi skema.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-162">You can use the *Download schema* option on the **Business events catalog** page in Supply Chain Management or start by pasting in the example schema text.</span></span> <span data-ttu-id="1b2cc-163">Þessi dæmatexti er gefinn eftir eftirfarandi skýringarmynd.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-163">This example text is provided after the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example3.png" alt-text="Power Automate Þátta JSON-skref":::

    ```json
    {
        "properties": {
            "BusinessEventId": {
                "type": "string"
            },
            "ControlNumber": {
                "type": "integer"
            },
            "EventId": {
                "type": "string"
            },
            "EventTime": {
                "type": "string"
            },
            "MajorVersion": {
                "type": "integer"
            },
            "MessageContent": {
                "type": "string"
            },
            "MessageDestinationCompanyId": {
                "type": "string"
            },
            "MessageDestinationOperationalSiteId": {
                "type": "string"
            },
            "MessageDestinationWarehouseId": {
                "type": "string"
            },
            "MessageDestinationWorkloadName": {
                "type": "string"
            },
            "MessageInfolog": {
                "type": "string"
            },
            "MessageProcessingResult": {
                "type": "string"
            },
            "MessageProcessingResultLabel": {
                "type": "string"
            },
            "MessageProcessorMessagePageUrl": {
                "type": "string"
            },
            "MessageQueue": {
                "type": "string"
            },
            "MessageQueueLabel": {
                "type": "string"
            },
            "MessageSourceCompanyId": {
                "type": "string"
            },
            "MessageSourceOperationalSiteId": {
                "type": "string"
            },
            "MessageSourceWarehouseId": {
                "type": "string"
            },
            "MessageSourceWorkloadName": {
                "type": "string"
            },
            "MessageState": {
                "type": "string"
            },
            "MessageStateLabel": {
                "type": "string"
            },
            "MessageType": {
                "type": "string"
            },
            "MessageTypeLabel": {
                "type": "string"
            },
            "MinorVersion": {
                "type": "integer"
            }
        },
        "type": "object"
    }
    ```

1. <span data-ttu-id="1b2cc-165">Í skrefinu **Senda tölvupóst** er hægt að velja einstaka reiti eða byrja á því að líma dæmið um meginmál tölvupósts í reitinn **Meginmál**.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-165">In the **Send an email** step, you can select the individual fields or start by pasting the email body example into the **Body** field.</span></span> <span data-ttu-id="1b2cc-166">Þetta dæmi er gefið eftir eftirfarandi skýringarmynd.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-166">This example is provided after the following illustration.</span></span>

    :::image type="content" source="./media/cloud-edge-power-automate-example4.png" alt-text="Power Automate skref tölvupóstssendingar":::

    ```plaintext
    Message queue: @{body('Parse_JSON')?['MessageQueue']}
    Message queue label: @{body('Parse_JSON')?['MessageQueueLabel']}
    Message type: @{body('Parse_JSON')?['MessageQueueType']}
    Message type label: @{body('Parse_JSON')?['MessageQueueTypeLabel']}
    Message content: @{body('Parse_JSON')?['MessageContent']}
    Message state: @{body('Parse_JSON')?['MessageState']}
    Message state label: @{body('Parse_JSON')?['MessageStateLabel']}
    Message processing result: @{body('Parse_JSON')?['MessageProcessingResult']}
    Message processing result label: @{body('Parse_JSON')?['MessageProcessingResultLabel']}
    Message infolog: @{body('Parse_JSON')?['MessageInfolog']}
    Message source company ID: @{body('Parse_JSON')?['MessageSourceCompanyId']}
    Message source workload name: @{body('Parse_JSON')?['MessageSourceWorkloadName']}
    Message source site ID: @{body('Parse_JSON')?['MessageSourceOperationalSiteId']}
    Message source warehouse ID: @{body('Parse_JSON')?['MessageSourceWarehouseId']}
    Message destination company ID: @{body('Parse_JSON')?['MessageDestinationCompanyId']}
    Message destination workload name: @{body('Parse_JSON')?['MessageDestinationWorkloadName']}
    Message destination site ID: @{body('Parse_JSON')?['MessageDestinationOperationalSiteId']}
    Message destination warehouse ID: @{body('Parse_JSON')?['MessageDestinationWarehouseId']}
    Message processor message page URL: @{body('Parse_JSON')?['MessageProcessorMessagePageUrl']}
    ```

1. <span data-ttu-id="1b2cc-168">Þegar viðburðurinn er vistaður er hann sjálfkrafa virkjaður og tilbúinn til notkunar sem hluti af Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1b2cc-168">When you save the business event, it will automatically be activated and ready to use as part of Supply Chain Management.</span></span>
