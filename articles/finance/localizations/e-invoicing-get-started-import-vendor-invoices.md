---
title: Nota rafræna reikningsþjónustu til að flytja inn reikninga lánardrottna
description: Í þessu efnisatriði er að finna upplýsingar um hvernig á að flytja inn reikninga lánardrottna með rafrænni reikningsfærsluþjónustu.
author: gionoder
ms.date: 08/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 434bf1f6a5a727a71592493b85ab166cbeff2f0980c2c968c99973a03f4dc660
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6751253"
---
# <a name="use-the-electronic-invoicing-service-to-import-vendor-invoices"></a>Nota rafræna reikningsþjónustu til að flytja inn reikninga lánardrottna

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Í þessu efnisatriði er að finna upplýsingar sem hjálpa til við að komast af stað með að flytja inn reikninga lánardrottins með rafrænni reikningsfærsluþjónustu. Þær leiða þig í gegnum skilgreiningarskrefin í Regulatory Configuration Services (RCS), Dynamics 365 Finance og Dynamics 365 Supply Chain Management sem þú verður að fylgja til að fá rafræna reikninga lánardrottna frá lánardrottnum.

## <a name="set-up-vendor-invoice-import-in-rcs"></a>Setja upp innflutning á reikningi lánardrottins í RCS
Til að setja upp innflutning reikning lánardrottins í RCS skaltu fylgja þessum skrefum:

1. Skoðaðu listann yfir [almennt aðgengilegir eiginleikar rafrænnar reikningsfærslu](e-invoicing-configuration-rcs.md#generally-available-features).
2. Veldu og flyttu inn eiginleika rafrænnar reikningsfærslu. Frekari upplýsingar eru í [Flytja inn eiginleika rafrænnar reikningsfærslu úr skilgreiningarveitu Microsoft](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider).
3. Stofnaðu eiginleika rafrænnar reikningsfærslu fyrir fyrirtækið þitt. Frekari upplýsingar eru í [Stofna eiginleika rafrænnar reikningsfærslu undir þjónustuveitu fyrirtækisins](e-invoicing-get-started.md#create-an-electronic-invoicing-feature-under-your-organization-provider).

## <a name="configure-an-email-account-channel"></a>Skilgreina rás tölvupóstsreiknings

Skilgreindu rás tölvupóstsreiknings ef eiginleiki rafrænnar reikningsfærslu sem þú stofnaðir flytur inn rafræna reikninga lánardrottna úr viðhengdum skrám sem koma í tölvupósti.

1. Í RCS, veljið eiginleika rafrænnar reikningsfærslu sem var stofnaður. Gakktu úr skugga um að þú veljir útgáfu með stöðuna **Drög**.
2. Í flipanum **Uppsetningar**, í hnitanetinu, skal velja uppsetningu eiginleika og því næst **Breyta**.
3. Í flipanum **Gagnarás**, í reitahópnum **Færibreytur**, skal velja **Vistfang þjóns** og slá inn þjónustuaðila tölvupóstsreiknings.
4. Veldu **Gátt netþjóns** og sláðu inn gáttina sem þjónustuaðili tölvupóstsreikningsins notar.
5. Veldu **Leynilykill notandanafns** og færðu inn heiti á leynilykli lyklageymslu sem inniheldur auðkennið fyrir notandareikning tölvupóstsins.
6. Veldu **Leynilykill fyrir aðgangsorð notanda** og færðu inn heiti á leynilykli lyklageymslu sem inniheldur aðgangsorðið fyrir notandareikning tölvupóstsins.
7. Veldu **Efnissía**. Farðu yfir og uppfærðu strenginn sem inniheldur sjálfgefið netfang sem gefur upp tölvupóstinn sem inniheldur rafrænan reikning lánardrottins sem á að flytja inn.
8. Í flipanum **Gildissviðsreglur** skal fara yfir og uppfæra skilyrðið ef á þarf að halda. Frekari upplýsingar er að finna í [Gildissviðsreglur](e-invoicing-configuration-rcs.md#applicability-rules).
9. Veljið **Vista** og lokið síðunni.

### <a name="configure-a-microsoft-sharepoint-channel"></a>Skilgreina Microsoft SharePoint rás

Skilgreindu rás Microsoft SharePoint ef eiginleiki rafrænnar reikningsfærslu flytur inn rafræna reikninga lánardrottna úr skrám sem staðsettar eru í SharePoint möppum.

1. Í RCS, veljið eiginleika rafrænnar reikningsfærslu sem var stofnaður. Gakktu úr skugga um að þú hafir valið **Útgáfu** með stöðuna **Drög**.
2. Í flipanum **Uppsetningar**, í hnitanetinu, skal velja Uppsetningu eiginleika og því næst **Breyta**.
3. Í flipanum **Gagnarás**, í reitahópnum **Færibreytur**, skal velja **SharePoint vistfang** og slá inn SharePoint vefslóðina.
4. Veldu **Gátt netþjóns** og sláðu inn gáttina sem þjónustuaðili tölvupóstsreikningsins notar.
5. Veldu **Forritsauðkenni** og færðu inn heiti á leynilykli lyklageymslu sem inniheldur auðkennið fyrir SharePoint biðlarann.
6. Veldu **Leynilykil forrits** og færðu inn heiti á leynilykli lyklageymslu sem inniheldur aðgangsorðið fyrir SharePoint biðlarann.
7. Veldu **Skráarafmörkun**. Farðu yfir og uppfærðu síuna til að sía skrárnar sem innihalda rafrænan reikning lánardrottins sem á að flytja inn.
8. Í flipanum **Gildissviðsreglur** skal fara yfir og uppfæra skilyrðið ef á þarf að halda. Frekari upplýsingar er að finna í [Gildissviðsreglur](e-invoicing-configuration-rcs.md#applicability-rules).
9. Veljið **Vista** og lokið síðunni

### <a name="deploy-an-electronic-invoicing-feature"></a>Nota eiginleika rafrænnar reikningsfærslu

Til að nota eiginleika rafrænnar reikningagerðar skal sjá [Nota eiginleika rafrænnar reikningsfærslu í þjónustuumhverfi](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment).

## <a name="set-up-vendor-invoice-import-in-finance-and-supply-chain-management"></a>Setja upp innflutning á reikningi lánardrottins í Finance og Supply Chain Management
Ljúktu skrefunum í eftirfarandi tveimur hlutum til að setja upp mismunandi gerðir af innflutningi lánardrottnareikninga.

### <a name="import-vendor-invoices-from-email"></a>Flytja inn reikninga lánardrottins úr tölvupósti

1. Skráðu þig inn í umhverfi Finance eða Supply Chain Management og gakktu úr skugga um að þú sért í réttum lögaðila.
2. Farið í **Fyrirtækisstjórnun** > **Uppsetning** > **Færibreytur rafræns skjals**.
3. Í flipanum **Eiginleikar** skal ganga úr skugga um að **NF-e Federal - Rafrænn reikningur fyrir Brasilíu** sé valinn.
4. Í **Ytri rásir**, í reitahópnum **Rásir**, skal velja **Bæta við**.
5. Í reitinn **Rás** skal færa inn **NFe** (heiti rásarinnar sem gefið er upp í skilgreiningu gagnarásar fyrir eiginleika rafrænnar reikningsfærslu í RCS).
6. Í reitnum **Lýsing** skal færa inn lýsingu. Í reitnum **Fyrirtæki** skal velja lögaðilann.
7. Í reitnum **Samhengi skjals** skal velja **Samhengi fjárhagsskjals - Samhengislíkan viðskiptavinareiknings**.
8. Í reitnum **Flytja inn uppruna** skal velja **Bæta við**.
9. Í reitinn **Heiti** skal færa inn **XmlFile** (heiti **Viðhengissíunnar** sem gefið er upp í skilgreiningu gagnarásar fyrir eiginleika rafrænnar reikningsfærslu í RCS).
10. Í reitinn **Lýsing** skal færa inn lýsingu og í reitnum **Heiti gagnaeiningar** skal velja **Móttekin XML-skjöl Nf-e**.
11. Í reitnum **Líkanavörpun** skal velja **Innflutningur NF-e í tölvupósti – Innflutningur NF-e í tölvupósti (BR)** og veldu svo **Vista**.
12. Í flipanum **Rafrænt skjal**, í reitahópnum **Rafræn skýrslugerð**, skal velja **Bæta við** og síðan í reitnum **Töfluheiti** skal velja **Móttekið XML-skjal NF-e**.
13. Í reitnum **Samhengi skjals** skal velja **Spyrjast fyrir um samhengi fjárhagsskjals – Samhengi viðskiptavinareiknings**.
14. Í reitnum **Líkanavörpun rafræns skjals** skal velja **Spyrjast fyrir um vörpun – Vörpun fjárhagsskjals**.
15. Veljið **Svargerðir** og veljið síðan **Ný**.
16. Í reitinn **Gerð svars** skal færa inn **Svar**. Í reitinn **Staða innsendingar** skal færa inn **Tímasett**.
17. Í reitnum **Líkanavörpun** skal velja **Líkanavörpun úr svarskilaboðum – Innflutningssnið svarskilaboða**.
18. Veljið **Vista** og lokið síðan síðunni.

### <a name="import-peppol-electronic-vendor-invoices"></a>Flytja inn PEPPOL rafrænan reikningur lánardrottins

1. Farðu á vinnusvæðið **Rafræn skýrslugerð** og veldu **Skýrsluskilgreiningar**.
2. Veldu **Samhengislíkan viðskiptavinareiknings** og stofnaðu afleidda skilgreiningu.
3. Í **Drögum** að útgáfu skal velja **Hönnuð**.
4. Í trénu **Gagnalíkan** skal velja **Reikning viðskiptavinar** og síðan velja **Varpa líkani á gagnagjafa**.
5. Í **Skilgreiningatrénu** skal velja **CustomerInvoice** og síðan velja **Hönnuður**.
6. Í trénu **Gagnagjafar** skal velja **Samhengi\_Rás**. Í reitnum **Gildi** skal velja **PEPPOL**. Þetta er heiti rásarinnar sem gefið er upp í skilgreiningu gagnarásar fyrir eiginleika rafrænnar reikningsfærslu í RCS. 
7. Veljið **Vista** og lokið síðunni.
8. Lokið síðunni.
9. Veldu **Samhengislíkan viðskiptavinareiknings** og í flýtiflipanum **Útgáfur** skal velja **Breyta stöðu** > **Lokið**.
10. Farðu í **Fyrirtækisstjórnun** > **Uppsetning** > **Færibreytur rafrænna skjala** og í flipanum **Eiginleikar** skal ganga úr skugga um að **Altækir rafrænir reikningar PEPPOL** sé valið. 
11. Í flipanum **Ytri rásir**, í reitahópnum **Rásir**, skal velja **Bæta við**.
12. Í reitinn **Rás** skal færa inn **PEPPOL**. Í reitnum **Lýsing** skal færa inn lýsingu.
13. Í reitnum **Fyrirtæki** skal velja lögaðilann. Í reitnum **Samhengi skjals** skal velja **Samhengi viðskiptavinareiknings - Samhengislíkan viðskiptavinareiknings**.
14. Veljið **Vista** og lokið síðan síðunni.


## <a name="receive-electronic-invoices"></a>Taka á móti rafrænum reikningum
Til að fá rafræna reikninga skal fylgja þessum skrefum:

1. Farðu í **Fyrirtækisstjórnun** > **Reglubundið** > **Rafræn skjöl** > **Móttaka rafræn skjöl**.
2. Veldu **Í lagi** og lokaði svo síðunni.

## <a name="view-receive-logs-for-electronic-invoices"></a>Skoða móttökukladda fyrir rafræna reikninga

Til að skoða móttökukladdana fyrir rafræna reikninga er farið í **Fyrirtækisstjórnun** > **Reglubundið** > **Rafræn skjöl** > **Móttökukladdi rafræns skjals**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
