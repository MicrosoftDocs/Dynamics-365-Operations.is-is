---
title: Setja upp tilraun
description: Þessi grein lýsir því hvernig á að setja upp tilraun í þjónustu þriðja aðila.
author: sushma-rao
ms.date: 06/08/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: 1073cdc509622279ce7388b8b406079a4e6e9e09
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946167"
---
# <a name="set-up-an-experiment"></a>Setja upp tilraun

Þegar búið er að [skilgreina og ákvarða hvaða árangursmælingar á að nota](experimentation-identify.md) þarf að setja upp tilraunina í þjónustu þriðja aðila. Eftirfarandi skýringarmynd sýnir öll skrefin sem taka þátt í uppsetningu og vinnslu á tilraun á vefsvæði rafrænna viðskipta í Dynamics 365 Commerce. Fjallað er um fleiri skref í aðskildum greinum.

[ ![Tilraunaferli notanda - Uppsetning.](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)


## <a name="set-up-your-experiment-in-the-third-party-service"></a>Setja upp tilraun í þjónustu þriðja aðila
Nú ætti að vera búið að velja þjónustu þriðja aðila til að keyra og fylgjast með tilrauninni og setja upp tengil tilraunarinnar. Þessi skilyrði eru skráð í [Tilraunagerð í Dynamics 365 Commerce](experimentation-overview.md).

Fylgið skrefunum sem þarf til að búa til tilraunir í þjónustu þriðja aðila. Ef tengillinn er skilgreindur á réttan hátt verður fullbúinn listi yfir allar tilraunir sem settar eru upp í þjónustu þriðja birtur í vefsmið Commerce innan 5 mínútna.

## <a name="set-up-your-success-metrics"></a>Setja upp árangursmælingar
Sérhver tilraun þarf mælingar til að mæla áhrif afbrigðanna og til að sannprófa tilgátuna. Fylgið skrefunum hér að neðan til að virkja útreikning á mælingum í þjónustu þriðja aðila með virkum tilvikum fjarmælinga úr Dynamics 365 Commerce.

Fylgdu þessum skrefum til að setja upp árangursmælingar þínar fyrir útbúnar einingar.

1. Í vefsmið Commerce skal velja **Síður** á vinstra yfirlitssvæðinu og síðan velja síðuna sem á að safna mælingum fyrir. 
1. Farið í hlutann **Kenni tilvika til að fylgjast með** á eiginleikasvæðinu hægra megin á síðunni eða einingunni sem á að fylgjast með.
1. Velja **Skoða**. Listi yfir öll auðkenni smellaviðburða birtist. Afritaðu viðburðinn sem þú vilt fylgjast með og límdu síðan viðburðarlykilinn inn á tilgreindan stað í þjónustu þriðja aðila. Ef þörf er á fleiri en einu tilviki skal afrita lyklana einn í einu. 
1. Fyrir síðuskoðanir, notaðu SHA-256 kjötkássagildi síðuheitisins í vefsvæðisgerð sem bætt er við `.PageView`. Til dæmis, auðkenni viðburðar fyrir`Homepage.PageView` væri `e217eb66c7808ecc43b0f5c517c6a83b39d72b91412fbd54a485da9d8e186a9`.
1. Farið í gegnum öll önnur skref til að rekja mælingar eins og krafist er í þjónustu þriðja aðila.

Fylgdu þessum skrefum fyrir smelli á sérsniðnum einingum til að mæla smellitilvikin:

1. Undirbúa a **TelemetryContent** hlut fyrir eininguna með því að nota aðgerðina hér að neðan. Þessi aðgerð tekur síðuheitið, heiti einingarinnar og SDK-útvegaðan sjálfgefinn fjarmælingarhlut sem inntak.

    ```TypeScript
    getTelemetryObject(pageName: string, moduleName: string, telemetry: ITelemetry): ITelemetryContent
    ```
    
    Eftirfarandi er dæmi: 
    
    ```TypeScript
    private readonly telemetryContent: ITelemetryContent = getTelemetryObject(this.props.context.request.telemetryPageName!, this.props.friendlyName, this.props.telemetry);
    ```
    
1. Búðu til farmgögnin sem innihalda upplýsingar um það sem þarf að fanga. Fyrir hnappa og aðrar kyrrstöðustýringar geturðu látið fylgja með **texti** eins og "Verslaðu núna" eða "Leita". Og fyrir íhluti með smelli eins og að smella á vörukort geturðu sent **endurtaka** sem er skráningarauðkenni vörunnar eða vöruauðkenni.

    ```TypeScript
    getPayloadObject(eventType: string, telemetryContent: ITelemetryContent, etext: string, recid?: string): IPayLoad
    ```
    Sem dæmi um kyrrstöðustýringar, sendu textastreng hnappsins eins og sýnt er hér að neðan:

    ```TypeScript
    const payLoad = getPayloadObject('click', this.props.telemetryContent, 'Shop Now', '');
    ```
    Sem dæmi um vörusmelli, sendu vöruskráningarnúmerið eins og sýnt er hér að neðan:

    ```TypeScript
    const payLoad = getPayloadObject('click', telemetryContent!, '', product.RecordId.toString());
    ```
    
1. Hringdu í **OnClick** aðgerð til að skrá viðburðinn.

    ```TypeScript
    onTelemetryClick = (telemetryContent: ITelemetryContent, payLoad: IPayLoad, linkText: string) => () =>
    ```

    Eftirfarandi er dæmi:

    ```TypeScript
    onClick: onTelemetryClick(this.props.telemetryContent, payLoad, linkText)
    ```

## <a name="previous-step"></a>Fyrra skref
[Auðkenna tilgátu og ákvarða mælieiningar fyrir tilraun](experimentation-identify.md) 


## <a name="next-step"></a>Næsta skref
[Tengja og breyta tilraun](experimentation-connect-edit.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
