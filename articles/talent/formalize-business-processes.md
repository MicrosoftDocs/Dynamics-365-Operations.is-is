---
title: "Móta viðskiptaferla"
description: "Eiginleiki viðskiptaferils gerir þér kleift að búa til sniðmát viðskiptaferla fyrir ferla sem þarf að ljúka innan fyrirtækisins."
author: ShielaSogge
manager: AnnBe
ms.date: 01/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: PersonnelBusinessProcessGenericWorkspace, BusinessProcessGenericTemplateListpage, BusinessProcessGenericMyTemplates, BusinessProcessGroupAssignment
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: ShielaS
ms.search.validFrom: 2018-01-09
ms.dyn365.ops.version: AX 7.1.0, Talent October 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 1b50a97f5e2fc94255ff71702faf91ab36e68eb4
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="formalize-business-processes"></a>Móta viðskiptaferla
Eiginleiki viðskiptaferils gerir þér kleift að búa til sniðmát viðskiptaferla fyrir ferla sem þarf að ljúka innan fyrirtækisins. Til dæmis getur fyrirtækið lokið mannauðsúttekt á hverju ári. Hægt er að búa til sniðmát til að fylgjast með öllum þeim verkefnum sem felast í úttektinni til að tryggja að öll verkefnin séu gerð í hvert skipti sem ferlinu lýkur og ef nauðsyn krefur, til að tryggja að verkefnin séu framkvæmd í réttri röð. Sniðmát er hægt að endurnota fyrir endurtekna ferla eða afrita til að nota sem upphafsstað þegar ný sniðmát eru stofnuð.

Þegar sniðmát hefur verið stofnað er hægt að hefja ferli og rekja það á vinnusvæði Viðskiptaferlis.  Þegar viðskiptaferli er hafið verður verkefnum úthlutað á viðeigandi fólk og mun innihalda lokadag. Við munum fara yfir þessa þætti í smáatriðum hér að neðan.

## <a name="business-process-template"></a>Sniðmát viðskiptaferlis
Sniðmát viðskiptaferlis sýnir hóp verkefna sem mynda viðskiptaferil. Starfsmannastjórar og aðstoðarmenn geta sjálfgefið stofnað viðskiptaferla.  Hins vegar er hægt að breyta þessu í öryggisstillingum með því að breyta aðgangsheimildinni „Vinna með almenn viðskiptaferli.“

Ferileiganda er hægt að skilgreina fyrir hvert ferli. Ferileigandinn mun hafa sýnileika í öll verkefni ferlisins og getur endurúthlutað verkefnum eða breytt lokadögum.  Til dæmis gæti starfsmannastjórinn stofnað sniðmát viðskiptaferlis fyrir yfirferð á fríðindum.  Stjórnandi launa og fríðinda getur verið stilltur sem ferileigandi þannig að hann eða hún geti haft innsýn í verkefnin sem þarf að ljúka sem hluta af yfirferðinni.  Ferileigandi getur ekki stofnað eða eytt virkum viðskiptaferlum eða sniðmátum viðskiptaferla.

## <a name="task"></a>Verkefni
Viðskiptiferli samanstendur oft af mörgum verkefnum. Hægt er að ljúka sumum verkefnum innan Dynamics 365 for Talent, t.d. yfirferð á innri námskeiðsboðum. Í þessu tilviki er valmyndaratriði valið í reit verkefnatengils. Önnur verkefni gætu falið í sér að yfirfara eða útfylla eyðublöð á vefsíðu. Að velja vefslóð í reit verkefnatengils býður upp á að veffang sé slegið inn. Þú getur slegið inn vefslóðir fyrir bæði ytri og innri síður í þessum reit. Þú getur einnig búið til verkefni fyrir aðgerðir sem þú lýkur handvirkt, svo sem að yfirfara aðgengi alls skipulags. Í þessu tilviki er ekki krafist verkefnatengils. Þessi sveigjanleiki gerir þér kleift að rekja margar gerðir af verkefnum í ítarlegu ferli.

Hægt er að úthluta verkefnum á ákveðinn starfskraft eða stöðu. Til dæmis verður stjórnandi launa og fríðinda alltaf sá sem annast yfirferð á tryggingaiðgjöldum.   Þegar verkefni er stofnað skal velja Stöðu fyrir Úthlutunargerðina og síðan velja Stjórnanda launa og fríðinda í Stöðulistanum. Þegar ferlið hefst verður verkefninu úthlutað á starfskraftinn sem hefur stöðuna Stjórnandi launa og fríðinda. Einnig er hægt að úthluta verkefninu á ákveðinn starfskraft með því að velja Starfskraftur í reitnum Úthlutunargerð og síðan velja viðeigandi manneskju.

Lokadagar verkefns ráðast af markdagsetningu sem var færð inn við upphaf ferlisins. Ljúka þarf sumum verkefnum fyrir markdagsetningu og öðrum má hugsanlega ljúka eftir markdagsetningu.  Þegar verkefni er skilgreint verður að færa inn lokadag sem tengist markdagsetningu í fráviki lokadags í reit markdagsetningar. Til dæmis má gera ráð fyrir að stjórnandi launa og fríðinda verði að framkvæma yfirferð á tryggingaiðgjöldum 10 dögum áður en mannauðsúttekt er lokið. Stofnað verkefni mun hafa lokadag sem tengist markdagsetningu upp á -10. Þess vegna, ef ferlið hefst 13. maí, verður verkefnið komið á tíma 3. maí. Athugið: Einnig er hægt að breyta lokadegi eftir að ferlið hefst.

Flókin verkefni gætu þurft mörg skref eða þurft á viðbótarupplýsingum frá einstaklingnum sem sinnir verkefnunum. Þú getur bætt við leiðbeiningum við verkefnið og einnig haft með RTF-snið fyrir leiðbeiningarnar. Leiðbeiningarnar geta veitt manneskjunni sem er úthlutað að ljúka verkefninu viðbótarupplýsingar um hvernig á að ljúka því.

## <a name="starting-a-process"></a>Að hefja ferli
Hægt er að hefja ferli innan sniðmáts viðskiptaferils með því að velja Hefja ferli.  Þegar ferli er hafið verða verkefni stofnuð fyrir valda starfskrafta og/eða stöður sem eru skilgreindar í verkefnunum sem eru innifaldar í sniðmát viðskiptaferlisins. Einnig verður úthlutað lokadegi fyrir hvert verkefni með því að bæta við eða draga frá fráviksdaga frá markdagsetningunni (sjá upplýsingar um fráviksdaga í verkefnakaflanum). Hægt er að skoða virka viðskiptaferla á vinnusvæði viðskiptaferla. 

## <a name="employee-self-service"></a>Sjálfsafgreiðsla starfsmanna
Þegar verkefni er úthlutað starfsmanni er hægt að skoða úthlutuð verkefni á sjálfsafgreiðslusíðu starfsmanna. Starfsmenn sem hafa verkefni viðskiptaferlis úthlutað geta séð verkefnið, lýsingu þess, leiðbeiningar um að ljúka því og nafn tengiliðar og þeir geta opnað tengda síðu eða vefsíðu Dynamics365 frá sjálfsafgreiðslusíðu starfsmanns. Verkefni geta verið merkt sem í gangi, hætt við eða lokið.

## <a name="business-process-workspace"></a>Vinnusvæði viðskiptaferlis
Starfsfólk mannauðsstjórnunar geta skoðað virka viðskiptaferla frá vinnusvæði viðskiptaferlis. Vinnusvæðið listar alla virka ferla og þau verkefni sem tengjast þeim. Hægt er að afmarka ítarlega verkefnalistann með lokadegi. Síðan sýnir einnig verkefni komin á tíma og verkefnum sem er sérstaklega úthlutað á mannauðsstjóra. Þeir geta einnig uppfært stöðu allra verkefna og, ef nauðsyn krefur, endurúthlutað verkefnum til að halda heildarviðskiptaferlinu gangandi.

## <a name="my-business-processes-workspace"></a>Mitt vinnusvæði viðskiptaferla
Ferileigendur geta skoðað virka viðskiptaferla sem þeim er úthlutað frá Mínu vinnusvæði viðskiptaferlis. Vinnusvæðið listar alla virka ferla og tengd verkefni sem þessi notandi á.  Hægt er að afmarka ítarlega verkefnalistann með lokadegi. Síðan sýnir einnig verkefni sem er sérstaklega úthlutað til ferileiganda. Ferileigandinn getur einnig uppfært stöðu allra verkefna ásamt því að endurúthluta verkefnum.

## <a name="navigating-business-processes"></a>Fletta í viðskiptaferlum
1. Til að bæta við sniðmáti viðskiptaferlis skaltu fara í Viðskiptaferlar- tenglar – Stjórnun viðskiptaferla.
   - a.   Nýtt mun stofna nýtt sniðmát.
   - b.   Afrit frá sniðmáti mun afrita valið sniðmát yfir í nýtt.
   - c.   Byrjunarferlið setur af stað valið viðskiptaferli, úthlutar verkefnum og reiknar út lokadaga.  
2. Til að skoða virka ferla og tengd verkefni skal fara á vinnusvæði Viðskiptaferla.

