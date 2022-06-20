---
title: Tilkynningar bylgjukerslu
description: Þessi grein lýsir tilkynningum um bylgjuframkvæmd og útskýrir hvernig á að setja þær upp.
author: Mirzaab
ms.date: 04/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WhsWaveNotificationPolicy, WHSParameters, WHSWaveTemplateTable, BusinessEventsWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 6f8f43bcdaae9a14350c66039d204caf38d33768
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8906972"
---
# <a name="wave-execution-notifications"></a>Tilkynningar bylgjukerslu

[!include [banner](../includes/banner.md)]

Eiginleikinn *Tilkynningar bylgjukeyrslu* notar viðskiptatilvik og aðgerðamiðstöð til að senda tilkynningar sem tengjast bylgjukeyrslunni. Hann gerir kleift að tilgreina tilviksgerðir sem búa til tilkynningar, vöruhúsin sem mynda þær og notendurna sem taka á móti þeim.

Hnappurinn **Sýna skilaboð** (bjöllutáknið) hægra megin á yfirlitsstikunn gefur til kynna hvenær skilaboð aðgerðamiðstöðvar verða tiltæk fyrir núverandi notanda. Notandinn getur valið hnappinn **Sýna skilaboð** til að opna aðgerðamiðstöðina og fara yfir skilaboðin.

Viðskiptatilvik eiga sér stað þegar viðskiptaferli eru keyrð. Viðskiptaferli samanstanda af verkum. Í viðskiptaferli framkvæma notendur sem taka þátt í því viðskiptaaðgerðir til að ljúka þessum verkum. Viðskiptaviðburðir bjóða upp á kerfi sem gerir ytri kerfum kleift að fá tilkynningar frá Finance and Operations forritum. Þannig geta kerfin framkvæmt viðskiptaaðgerðir til að bregðast við viðskiptatilvikunum. Frekari upplýsingar eru í [Yfirlit viðskiptatilvika](../../fin-ops-core/dev-itpro/business-events/home-page.md).

## <a name="turn-the-wave-execution-notifications-feature-on-or-off"></a>Kveiktu eða slökktu á Wave execution notifications eiginleikanum

Frá og með Supply Chain Management útgáfu 10.0.25 er sjálfgefið kveikt á þessum eiginleika. Stjórnendur geta kveikt eða slökkt á þessari virkni með því að leita að *Tilkynningar um framkvæmd bylgju* eiginleiki í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) vinnurými.

## <a name="scenario-send-wave-batch-execution-notifications-to-the-action-center"></a>Atburðarás: Senda tilkynningar um framkvæmd bylgjurunu til aðgerðamiðstöðvar

Þessi atburðarás sýnir heildarverkflæðið þegar tilkynningar eru sendar um villur vegna framkvæmdar bylgjurunu á tiltekið hlutverk í gegnum aðgerðamiðstöðina.

### <a name="make-demo-data-available"></a>Bjóða upp á sýnigögn

Til að fylgja þessari atburðarás verður þú að hafa sýnigögn sett upp og þú verður að velja lögaðilann **USMF**.

### <a name="make-sure-that-waves-are-run-in-batch-mode"></a>Gangið úr skugga um að bylgjurnar séu keyrðar í runustillingu

1. Farðu í **vöruhúsakerfi \> Uppsetning \> Færibreytur vöruhúsakerfis**.
1. Í flýtiflipanum **Bylgjuvinnsla** skal stilla valkostinn **Vinna bylgjur í runu** á *Já*.

> [!NOTE]
> Ef ætluni slökkva á tilkynningum vegna framkvæmdar bylgjuruna skal stilla valkostinn **Gera tilkynningar um runu bylgjuvinnslu óvirkar** á *Já*.

### <a name="configure-a-wave-notification-policy"></a>Skilgreina reglu um tilkynningu bylgju

Reglur bylgjutilkynningar skilgreina þær gerðir af tilkynningum sem eru sendar og notendurna sem fá tilkynningar.

1. Farið í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Reglur bylgjutilkynningar**.
1. Búið til færslu sem er með eftirfarandi stillingum:

    - **Regla um tilkynningu bylgju:** *24BatchError*
    - **Lýsing:** *Vöruhús 24 villa bylgjurunu*
    - **Senda tilkynningu þann:** *Aðeins villa*
    - **Á hlutverk:** *Kerfisstjóri*

        > [!NOTE]
        > Vegna þess að þessi atburðarás notar sýnigögn er hlutverkið *Kerfisstjóri* valið til einföldunar. Þar af leiðandi, vegna þess að þú ert skráð(ur) inn sem kerfisstjóri, færðu sendar tilkynningar. Hins vegar ætti undir venjulegum kringumstæðum að yfirleitt velja sértækara hlutverk til að senda tilkynningu um villu vegna framkvæmdar bylgjurunu, t.d. *Vöruhúsastjórnandi*.

1. Í aðgerðarúðunni skal velja **Vista**.

### <a name="configure-a-wave-template"></a>Skilgreina bylgjusniðmát

Bylgjusniðmát leyfa þér að tengja sérstök tilvik af bylgjuaðferðum við samsvarandi bylgjumerkissniðmát.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Bylgjusniðmát**.
1. Á listasvæðinu skal stilla reitinn **Bylgjusniðmátsgerð** á *Sending* og síðan velja bylgjusniðmátið *Sjálfgefin sending 24* fyrir vöruhús 24.
1. Í flýtiflipanum **Almennt** skal stilla reitinn **Regla um tilkynningu bylgju** á *24BatchError*.

### <a name="configure-a-work-template"></a>Stilla vinnusnið

Vinnusniðmát eru notuð í við framkvæmd bylgjukeyrslu til að búa til vinnu. Í þessari atburðarás ætti framkvæmd bylgju að leiða til villu. Með því að stilla fyrirspurn vinnusniðmáts á að nota vöruhús sem er ekki til, er gengið úr skugga um að framkvæmd bylgju mistakist og að tilkynning verði send.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnusniðmát**.
1. Á listasvæðinu skal stilla reitinn **Vinnusniðmátsgerð** á *Sölupantanir* og síðan velja vinnusniðmátið *24 stig sölupöntunar* fyrir vöruhús 24.
1. Á aðgerðasvæðinu skal velja **Breyta fyrirspurn**.
1. Í svarglugga fyrirspurnarritils, í flipanum **Svið**, skal breyta eftirfarandi línu (eða bæta henni við ef hún er ekki til):

    - **Tafla:** *Tímabundnar vinnufærslur*
    - **Afleidd tafla:** *Tímabundnar vinnufærslur*
    - **Svæði:** *Vöruhús*
    - **Skilyrði:** Breytið gildinu úr *24* í *Villa*.

1. Veldu **Í lagi** og staðfestu breytinguna.

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Stofna sölupöntun og losa hana í vöruhúsið.

1. Opnið **Sala og markaðssetning \> Sölupöntun \> Allar sölupantanir**.
1. Stofna sölupöntun sem er með eftirfarandi stillingar:

    - **Viðskiptavinalykill:** *US-001*
    - **Vöruhús:** *24*

1. Í flýtiflipanum **Sölupöntunarlínur** skal bæta við sölupöntunarlínu sem er með eftirfarandi stillingum:

    - **Vörunúmer:** *A0001*
    - **Magn:** *10*

    > [!NOTE]
    > Þessi atriði og magn eru aðeins dæmi. Tilgreint vöruhús verður að innihalda nóg af birgðum.

1. Á meðan nýja línan er enn valin í flýtiflipanum **Sölupöntunarlínur** skal velja **Birgðir \> Frátekning** á tækjastikunni.
1. Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota**. Því næst skal loka síðunni.
1. Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.

### <a name="notifications-from-wave-batch-job-execution"></a>Tilkynningar frá framkvæmd runuvinnslu bylgju

Það fer eftir uppsetningu viðskiptatilvikanna, en að lokum kemur tilkynning um að framkvæmd bylgju hafi mistekist. Skilaboð aðgerðamiðstöðvarinnar munu líkjast eftirfarandi dæmi og innihalda tengil á bylgjuna sem mistókst.

> **Villa við keyrslu bylgju**  
> Villa kom upp þegar bylgja var keyrð USMF-000000001.  
> Síðustu skilaboð: Engin vinna var stofnuð fyrir bylgju USMF-000000001.
>
> **STAÐA**  
> Í gangi
>
> Upplýsingar um opna bylgju

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
