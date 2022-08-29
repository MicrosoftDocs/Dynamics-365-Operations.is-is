---
title: Nota rafræna reikningsþjónustu til að flytja inn reikninga lánardrottna
description: Þessi grein veitir upplýsingar um hvernig á að flytja inn reikninga lánardrottins með því að nota rafræna reikningaþjónustu.
author: gionoder
ms.date: 09/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423,  ""intro-internal
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: c98f33345b37a72c4099f01e37c82e27002ac687
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283146"
---
# <a name="use-the-electronic-invoicing-service-to-import-vendor-invoices"></a>Nota rafræna reikningsþjónustu til að flytja inn reikninga lánardrottna

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Þessi grein veitir upplýsingar sem hjálpa þér að hefjast handa við að flytja inn reikninga lánardrottna með því að nota rafræna reikningaþjónustu. Það leiðir þig í gegnum stillingarskrefin í Regulatory Configuration Services (RCS), Dynamics 365 Finance og Dynamics 365 Supply Chain Management sem þú verður að fylgja til að fá rafræna lánardrottnareikninga frá söluaðilum.

## <a name="set-up-vendor-invoice-import-in-rcs"></a>Setja upp innflutning á reikningi lánardrottins í RCS
Til að setja upp innflutning reikning lánardrottins í RCS skaltu fylgja þessum skrefum:

1. Skoðaðu listann yfir [almennt aðgengilegir eiginleikar rafrænnar reikningsfærslu](e-invoicing-configuration-rcs.md#generally-available-features).
2. Veldu og flyttu inn eiginleika rafrænnar reikningsfærslu. Frekari upplýsingar eru í [Flytja inn eiginleika rafrænnar reikningsfærslu úr skilgreiningarveitu Microsoft](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider).
3. Stofnaðu eiginleika rafrænnar reikningsfærslu fyrir fyrirtækið þitt. Frekari upplýsingar eru í [Stofna eiginleika rafrænnar reikningsfærslu undir þjónustuveitu fyrirtækisins](e-invoicing-get-started.md#create-an-electronic-invoicing-feature-under-your-organization-provider).

## <a name="configure-an-email-account-channel"></a>Skilgreina rás tölvupóstsreiknings

Skilgreindu rás tölvupóstsreiknings ef eiginleiki rafrænnar reikningsfærslu sem þú stofnaðir flytur inn rafræna reikninga lánardrottna úr viðhengdum skrám sem koma í tölvupósti.

1. Í RCS, veljið eiginleika rafrænnar reikningsfærslu sem var stofnaður. Gakktu úr skugga um að þú veljir útgáfu með stöðuna **Drög**.
2. Í flipanum **Uppsetningar**, í hnitanetinu, skal velja uppsetningu eiginleika og því næst **Breyta**.
3. Í flipann **Gagnarás** í reitahópinn **Færibreytur**, í reitinn **Gagnarás**, skal færa inn heiti rásarinnar. Heiti rásarinnar ætti að innihalda í mesta lagi 10 stafi.
4. Í reitinn **Vistfang þjóns** skal færa inn þjónustuaðila tölvupóstsreikningsins. Til dæmis vistfang þjónsins fyrir **https://outlook.live.com/** er **imap-mail.outlook.com**.
5. Í reitinn **Gátt netþjóns** skal slá inn gáttina sem þjónustuaðili tölvupóstsreikningsins notar. Til dæmis er gátt netþjónsins fyrir **https://outlook.live.com/** **993**.
6. Í reitinn **Leynilykill notandanafns** skal færa inn heiti á leynilykli lyklageymslu sem inniheldur auðkennið fyrir notandareikning tölvupóstsins. Þennan leynilykil þarf að búa til í Azure-lyklageymslu og setja upp í þjónustuumhverfinu. 
7. Í reitinn **Leynilykill fyrir aðgangsorð notanda** skal færa inn heiti á leynilykli lyklageymslu sem inniheldur aðgangsorðið fyrir notandareikning tölvupóstsins.
8. Valfrjálst - Færið inn gildi í reitina **Frá síu**, **Efnissía** og **Dagsetningarsía**.
9. Færið inn heiti pósthólfanna þar sem póstarnir verða:

    - Flutt inn úr: **aðalmappa**
    - Vistað eftir heppnaða úrvinnslu: **Safnmappa**
    - Vistað eftir úrvinnsla mistókst: **Villumappa** Þú þarft ekk að búa til þessar möppur í pósthólfinu. Möppurnar eru sjálfkrafa búnar til eftir fyrsta innflutning og úrvinnslu á rafrænum reikningi. 
   
10. Í reitahópnum **Viðhengjasía** skal bæta við upplýsingum um skráasíun. Aðeins viðhengi sem fullnægja skilgreindri síu eru afgreidd. Til dæmis er hægt að setja upp „\*.xml“ fyrir viðhengi með xml-skrárendingu. Heiti viðhengisins er notað í Dynamics 365 Finance eða Dynamics 365 Supply Chain Management við uppsetningu. 
11. Í flipanum **Gildissviðsreglur** skal fara yfir og uppfæra skilyrðið ef á þarf að halda. Reiturinn **Rás** verður að jafngilda **Gagnarásinni** sem gefin var upp hér á undan. Frekari upplýsingar er að finna í [Gildissviðsreglur](e-invoicing-configuration-rcs.md#applicability-rules).
12. Veljið **Vista** og lokið síðunni.

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

## <a name="set-up-vendor-invoice-import-in-finance-or-supply-chain-management"></a>Setja upp innflutning á reikningi lánardrottins í Finance eða Supply Chain Management
Ljúktu skrefunum í eftirfarandi tveimur hlutum til að setja upp mismunandi gerðir af innflutningi lánardrottnareikninga.

### <a name="import-brazilian-nf-e-from-email"></a>Flytja inn brasilískt NF-e frá netfangi

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
2. Veldu **Samhengislíkan viðskiptavinareiknings** og veldu svo **Stofna skilgreiningu** > **Afleiða frá heiti: Samhengislíkan viðskiptavinareiknings, Microsoft** til að stofna afleidda skilgreiningu.
3. Í útgáfunni **Drög** skal velja **Hönnuður** og í trénu **Gagnalíkan** skal velja **Varpa líkani á gagnagjafa**.
4. Í **Skilgreiningatrénu** skal velja **DataChannel** og síðan velja **Hönnuður**.
5. Í trénu **Gagnagjafar** skal stækka geymsluna **$Context\_Rás**. Í reitnum **Gildi** skal velja **Breyta** og færa inn heiti rásarinnar. Þetta er heiti rásarinnar sem gefið er upp í skilgreiningu gagnarásar fyrir eiginleika rafrænnar reikningsfærslu í RCS. 
7. Veljið **Vista** og lokið síðunni.
8. Lokið síðunni.
9. Veldu afleidda skilgreiningu sem þú varst að búa til í **Samhengislíkan viðskiptavinareiknings** og í flýtiflipanum **Útgáfur** skal velja **Breyta stöðu** > **Lokið**.
10. Farðu í **Fyrirtækisstjórnun** > **Uppsetning** > **Færibreytur rafrænna skjala** og í flipanum **Eiginleikar** skal ganga úr skugga um að **Altækir rafrænir reikningar PEPPOL** sé valið. 
11. Í flipanum **Ytri rásir**, í reitahópnum **Rásir**, skal velja **Bæta við**.
12. Í reitinn **Rás** skal færa inn heiti gagnarásar og í reitinn **Upplýsingar** skal færa inn lýsingu.
13. Í reitnum **Fyrirtæki** skal velja lögaðilann. 
14. Í reitnum **Samhengi skjals** skal velja nýja afleidda skilgreiningu úr **Samhengislíkan viðskiptavinareiknings**. Lýsing vörpunar ætti að vera **Samhengi gagnarásar**.
15. Í reitnum **Flytja inn uppruna** skal velja **Bæta við**.
16. Í reitinn **Heiti** skal færa inn **Heiti viðhengissíu** og í reitnum **Heiti gagnaeiningar** skal velja **Reikningshaus lánardrottins**.
17. Í reitnum **Líkanavörpun** skal velja **Innflutningur lánardrottnareiknings - Flytja inn lánardrottnareikning**.
18. Smellið á **Vista** og lokið síðan skjámyndinni.


## <a name="receive-electronic-invoices"></a>Taka á móti rafrænum reikningum

Rafræn reikningsfærsluþjónusta fer í gegnum tvö skref við innflutning reiknings úr gagnarásum:

1. Opnar pósthólfið og les tölvupóst.
2. Vinnur úr tölvupóstunum. 
    
Til að framkvæma þessi tvö skref ætti viðskiptavinurinn að hringja í þjónustuna fyrir hvort skref. Hins vegar er mælt með því að sett sé upp runa fyrir móttöku rafrænna skjala.

Til að fá rafræna reikninga skal fylgja þessum skrefum:

1. Farðu í **Fyrirtækisstjórnun** > **Reglubundið** > **Rafræn skjöl** > **Móttaka rafræn skjöl**.
2. Veldu **Í lagi** og lokaði svo síðunni.


## <a name="view-receive-logs-for-electronic-invoices"></a>Skoða móttökukladda fyrir rafræna reikninga

Til að skoða móttökukladdana fyrir rafræna reikninga er farið í **Fyrirtækisstjórnun** > **Reglubundið** > **Rafræn skjöl** > **Móttökukladdi rafræns skjals**.
Ef þú sérð ekki reikninga sem búið er að vinna úr skaltu fjarlægja töflusíuna.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
