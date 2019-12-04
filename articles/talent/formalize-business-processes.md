---
title: Gera viðskiptaferli formleg
description: Þetta efnisatriði útskýrir hvernig hægt er að nota eiginleikann Viðskiptaferli til að búa til sniðmát viðskiptaferlis, fyrir ferli sem ljúka verður innan fyrirtækisins.
author: andreabichsel
manager: AnnBe
ms.date: 01/09/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: PersonnelBusinessProcessGenericWorkspace, BusinessProcessGenericTemplateListpage, BusinessProcessGenericMyTemplates, BusinessProcessGroupAssignment
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-01-09
ms.dyn365.ops.version: AX 7.1.0, Talent October 2017 update
ms.openlocfilehash: 2a245891e2e3e8c0eae4f28d0932776c3ee976dc
ms.sourcegitcommit: 9cc6a011bfdd1b0fe505760b6bf429eb6c65862a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/25/2019
ms.locfileid: "2832816"
---
# <a name="formalize-business-processes"></a>Gera viðskiptaferli formleg

[!include [banner](includes/banner.md)]

Eiginleikinn Viðskiptaferli gerir þér kleift að búa til sniðmát viðskiptaferlis, fyrir viðskiptaferli sem ljúka verður innan fyrirtækisins. Til dæmis lýkur fyrirtækið þitt endurskoðun mannauðsstjórnunar á hverju ári. Í þessu tilviki er hægt að búa til sniðmát sem fylgist með öllum verkþáttum sem endurskoðunarferlið samanstendur af. Þetta sniðmát getur þá hjálpað til við að tryggja að allir verkþættir séu framkvæmdir í hvert skipti sem endurskoðunin er gerð. Að auki, ef verkþáttum skal lokið í ákveðinni röð, getur sniðmátið hjálpað til við að tryggja að þeir séu framkvæmdir í réttri röð.

Sniðmát er hægt að endurnýta fyrir endurtekin ferli. Einnig er hægt að afrita þau og nota sem upphafspunkt til að búa til nýtt sniðmát.

Eftir að sniðmát viðskiptaferlis hefur verið stofnað, er hægt að hefja og fylgjast með viðskiptaferli í **Viðskiptaferli** vinnusvæðinu. Þegar viðskiptaferli er hafið er verkþáttum úthlutað til viðeigandi aðila og þau eru með skiladag.

## <a name="business-process-templates"></a>Sniðmát viðskiptaferlis
Sniðmát viðskiptaferlis sýnir hóp verkþátta sem mynda viðskiptaferli. Sjálfgefið er að mannauðsstjórar og aðstoðarmenn geti búið til viðskiptaferli. Þú getur hins vegar breytt hlutverkunum sem geta búið til viðskiptaferli með því að breyta **Vinna með almenn viðskiptaferli** aðgangsheimildinni í öryggisstillingu.

Fyrir hvert viðskiptaferli getur þú skilgreint eiganda ferlis. Eigandi ferlisins hefur innsýn í alla verkþætti ferlisins, og getur endurúthlutað verkþáttum eða breytt skiladögum. Til dæmis stofnar mannauðsstjórinn sniðmát viðskiptaferlis til að endurskoða fríðindi og tilgreinir umsjónaraðila launa og fríðinda sem eiganda ferlisins. Umsjónaraðili launa og fríðinda hefur þá innsýn í verkþættina sem verður að vera lokið sem hluta af endurskoðuninni.

Eigandi ferlis getur ekki búið til ný viðskiptaferli eða sniðmát viðskiptaferla, eða eytt virkum viðskiptaferlum eða sniðmátum viðskiptaferla.

## <a name="tasks"></a>Verk
Viðskiptaferli samanstendur oft af mörgum verkþáttum. Sumum verkþáttum, eins og t.d. endurskoðun á innri námskeiðstilboðum, er hægt að ljúka í Microsoft Dynamics 365 Talent. Í þessu tilviki er valkostur valinn í **Verkþáttatengill** reitnum. Aðrir verkþættir gætu falið í sér að endurskoða eða ljúka síðum á vefsíðu. Í þessu tilfelli er **vefslóð** valið í **Verkþáttatengill** og þá er hægt að slá inn veffangið. Þú getur slegið inn vefslóðir fyrir bæði ytri og innri síður. Þú getur einnig búið til verkþætti fyrir aðgerðir sem þú lýkur handvirkt, eins og t.d. endurskoðun á aðgengi allra formgerða. Í þessu tilviki er verkþáttatengils ekki krafist. Þessi sveigjanleiki gerir þér kleift að rekja margar gerðir af verkefnum í ítarlegu ferli.

Hægt er að úthluta verkþætti til ákveðins starfsmanns eða stöðu. Til dæmis mun umsjónaraðili launa og fríðinda alltaf vera sá sem framkvæmir endurskoðun á iðgjöldum. Þegar þú stofnar þennan verkþátt skal því velja **Staða** í **Úthlutunargerð** reitnum og velja svo **Umsjónaraðili launa og fríðinda** í **Staða** listanum. Þegar viðskiptaferlið er sett í gang, er verkþættinum úthlutað til starfsmannsins sem er í **Umsjónaraðili launa og fríðinda** stöðunni. Til að úthluta verkefni til tiltekins starfsmanns, veldu **Starfskraftur** í **Úthlutunargerð** reitnum og veldu síðan viðeigandi manneskju.

Skiladagar fyrir verkþætti fara eftir markmiðsdagsetningunni sem er slegið inn í upphafi viðskiptaferlisins. Sumum verkþáttum verða að vera lokið fyrir markmiðsdagsetninguna og hægt er að ljúka öðrum verkþáttum eftir markmiðsdagsetninguna. Þegar þú skilgreinir verkþátt, tilgreinir þú skiladag sem tengist markmiðsdagsetningu í **Frávik skiladags frá markmiðsdagsetningu** reitnum. Til dæmis þarf umsjónaraðili launa og fríðinda að framkvæma endurskoðun á iðgjöldum 10 dögum áður en endurskoðun mannauðsstjórnunar er lokið. Í þessu tilfelli er sá verkþáttur sem er búinn til fyrir endurskoðunina með **Frávik skiladags frá markmiðsdagsetningu** gildi upp á **-10**. Þess vegna, ef viðskiptaferlið er sett í gang 13. maí er skiladagur verkþáttarins 3. maí.

> [!NOTE]
> Einnig er hægt að breyta skiladagsetningum eftir að viðskiptaferlið er hafið.

Flóknir verkþættir gætu þurft margar skref eða fólkið sem framkvæma verkþættina gæti þurft að veita viðbótarupplýsingar. Fyrir þessar aðstæður geturðu bætt leiðbeiningum við verkþætti. Leiðbeiningarnar geta gefið þeim, sem er úthlutað því að ljúka verkþættinum, frekari upplýsingar um hvernig á að ljúka honum. Þú getur jafnvel haft RTF-snið með í leiðbeiningunum.

## <a name="starting-a-business-process"></a>Að hefja viðskiptaferli
Í sniðmáti viðskiptaferlis geturðu hafið viðskiptaferli með því að velja **Hefja ferli**. Þegar ferli er hafið eru verkþættir búnir til fyrir valda starfsmenn eða þær stöður sem eru skilgreindir í þeim verkþáttum sem eru innifaldir í sniðmátinu. Skiladegi er einnig úthlutað til sérhvers verkþáttar með því að bæta fjölda fráviksdaga við markmiðsdagsetninguna, eða draga þá frá henni, eins og lýst er í hlutanum „Verkþættir“. Hægt er að skoða virk viðskiptaferli í **Viðskiptaferli** vinnusvæðinu.

## <a name="employee-self-service"></a>Sjálfsafgreiðsla starfsmanna
Eftir að verkþætti hefur verið úthlutað til starfsmanns getur starfsmaðurinn skoðað hann, sem og alla aðra verkþætti sem honum hefur verið úthlutað, á síðunni **Sjálfsafgreiðsla starfsmanna**. Fyrir hvert viðskiptaferli sem honum er úthlutað, getur starfsmaðurinn séð nafn og lýsingu á verkþættinum, leiðbeiningar um hvernig skal ljúka honum og nafn tengiliðarins. Frá **Sjálfsafgreiðsla starfsmanna** síðunni getur starfsmaðurinn einnig opnað tengda síðu í Microsoft Dynamics 365 eða tengda vefsíðu, og getur merkt verkþætti í vinnslu, hætt við eða lokið.

## <a name="business-process-workspace"></a>Vinnusvæði viðskiptaferlis
Starfsfólk mannauðsstjórnunar geta skoðað virk viðskiptaferli í vinnusvæðinu **viðskiptaferli**. Þessi vinnusvæði sýnir lista yfir öll virk ferli og þá verkþætti sem tengjast hverju ferli. Hægt er að afmarka ítarlega verkefnalistann með lokadegi. Í vinnusvæðinu er einnig listi yfir verkþætti sem eru komnir fram yfir skiladag og verkþætti sem er sérstaklega úthlutað til starfsfólks mannauðsstjórnunar. Starfsmaður mannauðsstjórnunar getur einnig uppfært stöðu allra verkþátta og, eftir því sem þörf krefur, endurúthlutað verkþáttum til að hjálpa til við að halda heildarviðskiptaferlinu gangandi.

## <a name="my-business-processes-workspace"></a>Vinnusvæði fyrir mín viðskiptaferli
Eigendur ferlis geta skoðað virk viðskiptaferli sem er úthlutað til þeirra í **Mitt viðskiptaferli** vinnusvæði. Þetta vinnusvæði sýnir lista yfir öll virk ferli sem notandinn á, sem og tengda verkþætti. Hægt er að afmarka ítarlega verkefnalistann með lokadegi. Vinnusvæðið sýnir einnig lista yfir verkþætti sem er sérstaklega úthlutað til eiganda ferlisins. Eigandi ferlisins getur einnig uppfært stöðu allra verkþátta og tengt hvaða verkþætti sem er.

## <a name="navigating-business-processes"></a>Fletta í viðskiptaferlum
Til að búa til eða afrita sniðmát viðskiptaferlis, eða til að hefja viðskiptaferli, flettu að viðskiptaferli - tenglar - stjórnun viðskiptaferla. Þú getur þá framkvæmt eftirfarandi aðgerðir:

- Veldu **Nýtt** til að búa til nýtt sniðmát viðskiptaferlis.
- Veldu **Afrita frá sniðmáti** til að afrita valið sniðmát í nýtt sniðmát.
- Veldu **Byrja ferli** til að hefja valið viðskiptaferli, úthluta verkþáttum og reikna skiladaga.

Til að skoða virk ferli og tengda verkþætti, skal opna **Viðskiptaferli** vinnusvæðið.

