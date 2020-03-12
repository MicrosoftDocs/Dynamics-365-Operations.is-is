---
title: Hnitanetsgeta
description: Þetta efni lýsir nokkrum kröftugum eiginleikum netstýringar. Það verður að gera nýja hnitanetsaðgerðina kleift að hafa aðgang að þessum möguleikum.
author: jasongre
manager: AnnBe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 7136edba828bf97b6e0c8d2a698b884640d680e5
ms.sourcegitcommit: 880f617d1d6e95eccbed762c7ea04398553c2ec0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/11/2020
ms.locfileid: "3036266"
---
# <a name="grid-capabilities"></a>Hnitanetsgeta

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Nýja netstýringin veitir fjölda gagnlegra og öflugra getu sem hægt er að nota til að auka framleiðni notenda, smíða áhugaverðari sýn á gögnin þín og fá þroskandi innsýn í gögnin þín. Þessi grein mun fjalla um eftirfarandi getu: 

-  Reiknar samtölur
-  Flokkun gagna
-  Vélritun á undan kerfinu
-  Mat á stærðfræðisegðum 

## <a name="calculating-totals"></a>Reiknar samtölur
Í forritum Finance and Operations geta notendur séð heildartölur neðst í töludálkum í hnitanetum. Þessar samtölur eru sýndar í síðufótarhluta neðst á töflunni. 

### <a name="showing-the-grid-footer"></a>Sýni síðufót hnitanetsins
Það er neðanmálssvæði neðst í hverju töflukerfi í forritum Finance and Operations. Neðanmálið getur sýnt mikilvægar upplýsingar sem tengjast gögnum sem birtast í reitunum. Hér eru nokkur dæmi um þessar upplýsingar:

- Fjöldi valda lína í töflunni (þegar fleiri en ein skrá er valin)
- Stórt heildartölur neðst í samstilltu töludálkunum
- Fjöldi raða í gagnasafninu 

Þessi fótur er sjálfgefið falinn en auðvelt er að kveikja á honum. Til að sýna fót fyrir rist, hægrismellt er á dálkhaus í töflunni og valið valkosturinn **Sýna fót**. Þegar búið er að kveikja á fótfótum fyrir tiltekið rist mun sú stilling muna þar til notandinn kýs að fela fótfótinn, það er hægt að gera með því að hægrismella á dálkhaus og velja **Fela fót**.  Athugið staðsetningu staðsetningu **Sýna fót / Fela fót** Búist er við að aðgerð verði staðsett aftur í framtíðaruppfærslu. 

### <a name="specifying-columns-with-totals"></a>Tilgreina dálka með samtölum
Sem stendur er enginn dálkur stilltur til að sýna samtöl sem sjálfgefið. Þess í stað er þetta talið einskiptisvirkni, svipað og að laga breidd dálka í ristum. Þegar þú hefur tilgreint að þú viljir sjá samtölur fyrir dálk, þá munst þessi stilling næst þegar þú heimsækir síðuna.  

Það eru tvær leiðir til að stilla dálk til að sýna samtals: 

- Hægrismelltu á dálkinn sem þú vilt sjá samtölu fyrir og veldu síðan **Samtals þennan dálk**. Þessi aðgerð veldur því að þrír atburðir eiga sér stað:

    1. Neðanmálið verður sýnilegt. 
    2. Kjörstillingar þínar um að sjá samtölu í þessum dálki eru vistaðar. 
    3. Útreikningur á heildartölum er hafinn fyrir þennan dálk og alla aðra dálka sem þú hefur áður stillt til að sjá heildartölur fyrir. Tíminn sem þarf til að sýna heildartölu fer eftir stærð gagnapakkans sem þú ert að leggja saman heildartölu fyrir.

- Eftir að neðanmálið er sjáanlegt velurðu **Sýna samtölu** á neðanmálssvæðinu neðst í dálkinum sem þú vilt sjá heildartölu fyrir. Ef það eru engar stilltir dálkar verður hnappurinn **Sýna samtals** tiltækur fyrir alla talnardálka. 

    Þegar að minnsta kosti einn dálkur er stilltur fyrir samtölur verða hnapparnirnir **Sýna samtals** aðeins fáanlegir á sveimi eða fókus. Aðgerðin við að velja **Sýna samtals** vistar bara kjörstillingu þína um að sjá samtölu í þessum dálki, þannig að kjörstillingunni er beitt við síðari heimsóknir á síðuna. Í neðanmálinu er þessi staða gefin til kynna með bandstriki sem birtist í dálkinum. (Að öðrum kosti, ef gagnasafnið er nógu lítið, birtist samtalan strax.)

Ef þú gerir mistök og vilt ekki lengur sjá samtals í tilteknum dálki, hægrismellt á dálkinn og veldu **Fela samtals** eða veldu **Fela samtals** hnappinn í síðufætinum í þeim dálki. Þessi valkostur verður einnig vistaður fyrir framtíðarheimsóknir á síðunni. 

### <a name="calculating-totals"></a>Reiknar samtölur
Þegar þú kemur á síðu þar sem fótstigið er sýnilegt og dálkar nú þegar stilltir fyrir heildartölur, eru heildartölur mögulega eða ekki sýndar í fótfætinum. Hegðunin er háð stærð gagnapakkans á síðunni. Ef gagnapakkinn er nægjanlega lítill, birtast samtöl sjálfkrafa ásamt fjölda lína í gagnapakkanum. Ef það eru bandstrik í fótfótum undir dálkunum sem þú stilltir fyrir heildartölur, þá er gagnapakkinn of stór til að kerfið geti sýnt heildartölur strax og þörf er á skýrum aðgerðum til að reikna heildartölurnar. Til að gera þetta, smelltu á **Reikna** hnappinn í fótfótinum, eða hægrismelltu á dálkinn sem þú vilt hafa samtals fyrir og veldu **Samtals þennan dálk**.  

Ef útreikningurinn tekur of langan tíma geturðu hætt við aðgerðina með því að velja **Hætta við** takki. Stundum verður gagnapakkinn þó of stór til að reikna út heildartölur (takmörk sett af fyrirtækinu) og þér verður tilkynnt að sía gögnin þín meira.

Heildartölur munu uppfærast sjálfkrafa þegar þú uppfærir, eyðir eða býrð til línur í gagnapakkanum.  

## <a name="grouping-data"></a>Flokkun gagna
Notendur fyrirtækja þurfa oft að framkvæma sértækar greiningar á gögnum. Þó að þetta sé hægt að gera með því að flytja gögn út til Microsoft Excel og nota pivot töflur, the **Flokkun** getu í töflum ristum gerir notendum kleift að skipuleggja gögn sín á áhugaverðan hátt innan Finance and Operations smáforrit. Eins og þessi aðgerð nær til **Heildartölur** lögun, **Flokkun** gerir þér einnig kleift að fá þroskandi innsýn í gögnin með því að gefa undirstig á hópsstigi.

Til að nota þennan eiginleika skaltu hægrismella á dálkinn sem þú vilt flokka eftir og velja **Flokkaðu eftir þessum dálki**. Þessi aðgerð mun raða gögnum eftir völdum dálki, bæta við nýjum hóp eftir dálki í byrjun í ristina og setja „hausraðir“ í byrjun hvers hóps. Þessar hausraðir veita eftirfarandi upplýsingar um hvern hóp: 
-  Gagnagildi fyrir hópinn 
-  Dálkamerki (Þessar upplýsingar verða sérstaklega gagnlegar eftir að mörg stig af flokkun eru studd.)
-  Fjöldi gagnalína í þessum hópi
-  Undirmál fyrir hvaða dálk sem er stilltur til að sýna samtölur

Með [Vistaðar skoðanir](saved-views.md) virkt, þá er hægt að vista þennan flokkun með sérstillingu sem hluta af útsýni til að fá skjótan aðgang næst þegar þú heimsækir síðuna.  

Ef þú velur **Flokka eftir þessum dálki** í öðrum dálki er upprunalegri flokkun skipt út, þar sem aðeins eitt stig flokkunar er stutt í útgáfu 10.0.9 með verkvangsuppfærslu 33.

Til að afturkalla flokkun í rist skaltu hægrismella á flokkunarsúluna og velja **Taka saman hóp**.  


## <a name="evaluating-math-expressions"></a>Mat á stærðfræðisegðum
Sem framleiðniörvun geta notendur slegið inn stærðfræðiformúlur í tölureiti í töflu. Þeir þurfa ekki að gera útreikninginn í forriti utan kerfisins. Til dæmis ef þú slærð inn **=15\*4** og ýttu síðan á lykilinn **Flipi** til að fara út úr reitnum, mun kerfið meta segðina og vista gildi upp á **60** fyrir reitinn.

Til að gera kerfið að viðurkenna gildi sem tjáningu, byrjaðu gildið með jöfnu merki (**=**). Nánari upplýsingar um rekstraraðila sem studd er og setningafræði, sjá [Studd stærðfræðitákn](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).  
