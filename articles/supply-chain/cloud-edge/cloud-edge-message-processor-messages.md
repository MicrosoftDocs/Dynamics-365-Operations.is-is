---
title: Skilaboð um skilaboðaúrvinnslu
description: Í þessu efnisatriði er að finna upplýsingar um skilaboðaeiginleika skilaboðaúrvinnslu fyrir vinnuálag einingakvarða.
author: perlynne
manager: tfehr
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: b1428e2e657e653874d4ec07605932a32bd803b2
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938251"
---
# <a name="message-processor-messages"></a>Skilaboð um skilaboðaúrvinnslu

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Skilaboð skilaboðaúrvinnslu eru notuð þegar einingakvarðar skýs og jaðra er keyrt fyrir [vinnuálag framleiðslu](cloud-edge-workload-manufacturing.md) og [vinnuálag vöruhúsakerfis](cloud-edge-workload-warehousing.md).

Mikið magn gagna fer á milli uppsetningarumhverfa miðstöðvar og einingakvarða til að halda þeim samstilltum, en *skilaboðaúrvinnslan* vinnur einungis úr nokkrum þessara gagnaskipta. Hægt er að skoða skilaboðin sem skilaboðaúrvinnslan vinnur úr með því að fara í **Kerfisstjórnun > Skilaboðaúrvinnsla > Skilaboð skilaboðaúrvinnslu**.

## <a name="message-grid-columns-and-filters"></a>Dálkar og síur í skilaboðakerfi

Hægt er að nota reitina efst á síðunni **Skilaboð skilaboðaúrvinnslu** til að auðvelda að finna ákveðin skilaboð sem leitað er að. Flestar þessar síur passa við dálkhausana í skilaboðakerfinu. Eftirtaldar síur og dálkayfirskriftir eru tiltækar:

- **Gerð skilaboða** – Tilgreinir gerð skilaboða.
- **Skilaboðabiðröð** – Tilgreinir heiti biðraðarinnar sem á að vinna skilaboðin í. Eftirfarandi biðraðir eru í boði:
  - *Einingarkvarði til miðstöðvar*
  - *Miðstöð fyrir kvörðunareiningu vöruhúsakeyrslu*
  - *Miðstöð fyrir framkvæmd framleiðslu kvörðunareiningar*
- **Staða skilaboða** – Tilgreinir stöðu skilaboðanna. Eftirfarandi stöður eru til:
  - *Í biðröð* – Skilaboðin eru tilbúin til vinnslu hjá skilaboðaúrvinnslunni.
  - *Meðhöndlað* – Skilaboðin voru unnin af skilaboðaforritinu.
  - *Hætt við* - Skilaboðin voru unnin en úrvinnsla mistókst.
- **Efni skilaboða** – Þessi sía leitar að texta í öllu efni skilaboða. (Efni skilaboða er ekki sýnt í hnitanetinu.) Sían vinnur flest sértákn (á borð við „-“) sem bil og stafabilstákn sem Boole OR-virknitákn. T=Til dæmis þýðir þetta að ef leitað er að tilteknu `journalid` gildi sem jafngildir „USMF-123456“ mun kerfið finna öll skilaboð sem innihalda „USMF“ eða „123456“, sem verður líklega langur listi. Því væri betra að slá aðeins inn „123456“ því það skilar sértækari niðurstöðum.

## <a name="example-message-type-request-inventory-adjustment-financial-update"></a>Dæmi um skilaboðagerð: Beiðni um fjárhagslega uppfærslu birgðaleiðréttingar

Til dæmis er **Skilaboðagerðin** *Beiðni um fjárhagslega uppfærslu birgðaleiðréttingar* notuð til að stofna og bóka talningarbók í miðstöðinni þegar starfsmaður notar vöruhúsaforritið til að [skrá birgðaleiðréttingu](cloud-edge-warehouse-inventory-adjustment.md) í einingakvarða vinnuálags vöruhúsakerfis. Þar sem þetta tiltekna ferli er upprunnið úr einingakvarða mun reiturinn **Biðröð skilaboða** sýna gildið *Einingakvarði til miðstöðvar*.

Fyrir þessa skilaboðategund skráir vinnuálag skilaboðin sem hluta af aðgerð til að leiðrétta birgðaskrá vöruhúsaforrits. Gögn skilaboða eru síðan flutt til miðstöðvar sem hluti af sama ferlinu sem notað er fyrir [Skipulag Commerce Data Exchange](../../commerce/commerce-architecture.md). Skilaboðin verða uppfærð til að sýna **Staða skilaboða** sem *Í biðröð*. Skilaboðaúrvinnslan reynir þá að vinna úr skilaboðunum og uppfærir **Stöðu skilaboða** í *Unnið* þegar tekst, eða *Hætt við* þegar mistekst.

## <a name="view-the-message-log-message-content-and-details"></a>Skoða skilaboðaannál, innihald skilaboða og upplýsingar

Nákvæmar upplýsingar um skilaboð er hægt að finna með því að velja þau í hnitanetinu og síðan opna flipana **Kladdi** eða **Efni skilaboða** undir hnitaneti skilaboða þar sem hvert tilvik úrvinnslu er sýnt.

**Efni skilaboða** fer eftir **Gerð skilaboða** og verður því með mismunandi textalengd. Dæmigerður texti um efni skilaboða hefst á **{** og endar á **}** og inn á milli með reitarheiti á borð við `journalId` og á eftir því **:** og gildi á borð við *USMF-123456*.

Á tækjastikunni á flipanum **Kladdi** eru eftirfarandi hnappar:

- **Kladdi** – Birtir úrvinnsluniðurstöðurnar. Þetta er sérstaklega gagnlegt til að skilja ástæður þess af hverju úrvinnsla skilaboða hafi mistekst með **Niðurstaða úrvinnslu** sem *Mistókst*.
- **Búnt** – Hægt er að keyra margar skilaboðaaðgerðir sem hluta af sömu runuvinnslu. Velja þennan hnapp til að skoða þessi ítarlegu gögn. Til dæmis er hægt að sjá hvort til séu tengingar sem krefjast þess að kerfið vinni úr ákveðnum skilaboðum í ákveðinni röð.

## <a name="message-processor-batch-job"></a>Runuvinnsla skilaboðaúrvinnslu

Þegar skýja- og jaðrauppsetning er keyrð verður kallað sjálfkrafa á runuvinnsluna *Skilaboðaúrvinnsla* þegar ný skilaboð eru búin til fyrir úrvinnsluna, þannig að ekki ætti að vera þörf á því að tímasetja þessa vinnslu handvirkt.

Ef nauðsyn krefur er hægt að fá aðgang að runuvinnslunni með því að fara í **Kerfisstjórnun > Skilaboðaúrvinnsla > Skilaboðaúrvinnsla**.

## <a name="manually-process-or-cancel-a-message"></a>Vinna handvirkt úr eða hætta við skilaboð

Ef þörf krefur er hægt að vinna úr eða hætta við skilaboð handvirkt, allt eftir stöðu þeirra. Til að gera það skal velja skilaboðin í hnitanetinu og síðan velja **Vinna úr** eða **Hætta við** á aðgerðasvæðinu

## <a name="set-up-business-events-to-deliver-alerts-for-failed-processing-results"></a>Setja upp viðskiptatilvik til að senda viðvaranir vegna misheppnaðra úrvinnsluniðurstaðna

Auk þess að sía gildið fyrir **Skilaboðastöðuna** *Hætt við* til að grennslast fyrir um mislukkuð skilaboð, er hægt að setja upp [Viðskiptatilvik](../../fin-ops-core/dev-itpro/business-events/home-page.md) í miðstöðinni til að láta þegar úrvinnsla mistekst. Til að gera það þarf að virkja viðskiptatilvikið sem kallast *Skilaboð skilaboðaúrvinnslu meðhöndluð* á síðunni **Efnisskrá viðskiptatilvika** (**Kerfisstjórnun > Uppsetning > Viðskiptatilvik > Efnisskrá viðskiptatilvika**).

Sem hluti af virkjunarferlinu verður þér leiðbeint um hvernig á að tilgreina hvort tilvikið eigi við um einn eða alla lögaðila og gefa upp **Heiti endastöðvar**, sem þarf fyrst að skilgreina.

>[!NOTE]
> Ef **Þegar viðskiptatilvik á sér stað** er stillt á *Microsoft Power Automate* (frekar en til dæmis *HTTPS*) verður **Heiti endastöðvar** sjálfkrafa stofnað í Supply Chain Management samkvæmt *Microsoft Power Automate* uppsetningunni.

### <a name="microsoft-power-automate-example"></a>Microsoft Power Automate dæmi

Í þessu dæmi skal nota **Þegar viðskiptatilvik á sér stað** með *Microsoft Power Automate* sendir tölvupósta sem innihalda InfoLog-skilaboð og tengla til að opna síðuna **Skilaboð skilaboðaúrvinnslu** fyrir tiltekin skilaboð sem mistókust í uppsetningu miðstöðvarinnar. Ef þörf krefur er hægt að bæta við aukareglu til að senda tilkynningarnar samhliða með því að nota mismunandi rásir og stjórna viðtakendum samkvæmt gögnum tilviksins.

1. Í [Power Automate](https://preview.flow.microsoft.com) skal búa til nýtt sjálfvirkt skýjaflæði fyrir flæðisræsinguna **Þegar viðskiptatilvik á sér stað - Forrit Fin & Ops (Dynamics 365)** og í kjölfarið fylgja skrefin **Þátta JSON** og **Senda tölvupóst** eins og sýnt er á eftirfarandi mynd.

    :::image type="content" source="./media/cloud-edge-power-automate-example1.png" alt-text="Power Automate sjálfvirkt skýjaflæði":::

1. Í skrefinu **Þegar viðskiptatilvik á sér stað** er hægt að fletta upp eða færa inn miðstöðina **Tilvik** sem fylgir á eftir **Flokknum** og síðan **Viðskiptatilvikið** *Skilaboð skilaboðaúrvinnslu meðhöndluð* eins og sýnt er á eftirfarandi mynd.

    :::image type="content" source="./media/cloud-edge-power-automate-example2.png" alt-text="Power Automate Þegar skref viðskiptaviðburðar á sér stað":::

1. Fyrir skrefið **Þátta JSON** skal færa inn **Skema** sem skilgreinir stækkaða reiti. Hægt er að nota valkostinn *Sækja skema* á síðunni **Efnisskrá viðskiptatilvika** í Supply Chain Management eða byrja á því að líma inn textadæmi skema. Þessi dæmatexti er gefinn eftir eftirfarandi skýringarmynd.

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

1. Í skrefinu **Senda tölvupóst** er hægt að velja einstaka reiti eða byrja á því að líma dæmið um meginmál tölvupósts í reitinn **Meginmál**. Þetta dæmi er gefið eftir eftirfarandi skýringarmynd.

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

1. Þegar viðburðurinn er vistaður er hann sjálfkrafa virkjaður og tilbúinn til notkunar sem hluti af Supply Chain Management.
