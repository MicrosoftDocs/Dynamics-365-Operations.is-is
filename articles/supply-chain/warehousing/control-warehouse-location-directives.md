---
title: Stýra vöruhúsavinnu með vinnusniðmát og staðsetningarleiðbeiningar
description: Þetta efnisatriði lýsir hvernig eigi að nota vinnusniðmát og staðsetningarleiðbeiningar til að ákvarða hvernig og hvar vinna verður framkvæmd í vöruhúsinu.
author: perlynne
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLocDirFailure, WHSLocDirHint, WHSLocDirTable, WHSLocDirTableUOM, WHSRFMenuItem, WHSWork, WHSWorkClass, WHSWorkPool, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72921
ms.assetid: 377ab8af-5b0c-4b5e-a387-06ac1e1820c0
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-09
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7e955fba12e963a443c0304f0a8a0e395c46909dd34de12cd51fa9788491786
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6770145"
---
# <a name="control-warehouse-work-by-using-work-templates-and-location-directives"></a>Stýra vöruhúsavinnu með vinnusniðmát og staðsetningarleiðbeiningar

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir hvernig eigi að nota vinnusniðmát og staðsetningarleiðbeiningar til að ákvarða hvernig og hvar vinna verður framkvæmd í vöruhúsinu.

Leiðbeiningar sem starfsmenn vöruhúss fá í farsíma ákvarðast af sniðmáti vinnu sem er sett upp í Microsoft Dynamics 365 Supply Chain Management til að skilgreina hin ýmsu vöruhúsaferli og verkefni. Vinnusniðmát ákvarða vinnuna fyrir hvert vöruhúsaferli. Með því að tengja staðsetningarleiðbeiningar við vinnusniðmát getur hjálpað að tryggja að vinna á sér stað á ákveðnum efnislegum svæðum vöruhúss.

## <a name="work-templates"></a>Vinnusniðmát

**Vinnusniðmát** síðu gerir það mögulegt að skilgreina vinnsluaðgerðir sem þarf að framkvæma í vöruhúsinu. Yfirleitt samanstanda vinnsluaðgerðir vöruhúss af aðgerðarpari: starfsmanns í vöruhúsi tekur til lagerbirgðir á einni staðsetningu og setur síðan tíndu birgðirnar niður á annarri staðsetningu. 

Vinnusniðmát samanstendur af haus og tengdar línur Hvert vinnusniðmát er fyrir tiltekna *gerð vinnupöntunar*. Margar gerðir vinnupöntunar tengjast upprunaskjöl, eins og innkaupa- eða sölupantanir. Hins vegar, aðrar gerðir vinnupöntunar standa fyrir aðskilin vöruhúsaferli, eins og reglulega talningu. *kenni vinnuhópa* leyfir þér að skipuleggja vinnu í flokka. 

Nota skal stillingarnar í skilgreiningu vinnuhauss til að ákvarða þegar á að stofna nýja vinnu. Til dæmis er hægt að setja inn hámarksfjölda tiltektarlína og hámark áætlaðs tínslutíma. Svo ef vinnu fyrir tiltektarferli sölupöntunar fer fram yfir annaðhvort þessara gilda, er þeirri vinnu skipt í tvær einingar vinnu.

Notið **Vinnuhausaskil** hnappinn til að skilgreina hvenær kerfið á að búa til nýja vinnuhausa. Til að búa til dæmis til vinnuhaus fyrir hvert _pöntunarnúmer_ skal velja **Breyta fyrirspurn** á aðgerðasvæði og bæta síðan reitnum **Pöntunarnúmer** við flipann **Flokkun** í fyrirspurnarritli. Hægt er að velja reiti sem bætt er við flipann **Flokkun** sem *flokkunarreiti*. Til að stilla flokkunarreiti skal velja **Vinnuhausaskil** á aðgerðasvæði og síðan, fyrir hvern reit sem á að nota sem flokkunarsvæði, Veljið gátreitinn í dálkinum **Flokka eftir þessum reit**.

Vinnulínum tákna efnislega verkin sem nauðsynleg eru til að vinna úr vinnunni. Til dæmis, fyrir vöruhúsaferli á útleið, gæti verið ein lína til að taka til vörur innan vöruhús og aðra línu til að setja þær vörur yfir í sviðsetningarsvæðið. Svo getur verið til viðbótar lína til að taka til vörur frá sviðsetningu, og aðra línu fyrir setja vörurnar í vörubíl sem hluti af ferlinu við að hlaða. Hægt er að setja inn *leiðbeiningarkóði* á línum vinnusniðmáts. Leiðbeiningakóða er tengd staðsetningarleiðbeiningar og þar af leiðandi hjálpar til við að tryggja að vöruhúsavinna sé unnin á réttum stað í vöruhúsinu.

Hægt er að setja upp fyrirspurn til að stýra hvenær tiltekna vinnusniðmátið er notað. Til dæmis er hægt að setja takmörkun þannig að hægt er að nota tiltekið sniðmát fyrir vinnu eingöngu í ákveðnu vöruhúsi. Einnig gætirðu haft nokkur sniðmát sem stofna vinnu sölupöntunarferli á útleið, eftir uppruna sölu. Kerfið notar **Raðnúmer** svæði til að ákvarða röð tiltæk vinnusniðmát eru metin í. Þess vegna, ef þú ert með mjög nákvæma fyrirspurn fyrir tiltekið vinnusniðmát , ætti að gefa því lágt raðnúmer. Sú fyrirspurn verður síðan metin á undan öðrum, almennari fyrirspurnum.

> [!NOTE]
> Til að koma í veg fyrir að kerfið skrifi sjálfkrafa yfir vinnusniðmátið *raðnúmer* eftir að sniðmáti hefur verið eytt skal kveikja á *Varðveita raðnúmer vinnusniðmáts þegar eytt* eiginleikanum í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Til að stöðva eða gera hlé á vinnuferli, geturðu notað að **Stöðva vinnu** stillingu á vinnulínunni. Í því tilfelli fær starfsmaður sem framkvæmir vinnuna ekki beiðnir um að framkvæma næsta vinnulínuskref. Til að fara í næsta skref, þarf sá starfsmaður eða annars starfsmanns að velja vinnuna aftur. Hægt er að aðskilja verk innan með vinnueiningar með því að nota annað *kenni vinnuklasa* á línum vinnusniðmáts.

## <a name="location-directives"></a>Staðsetningarleiðbeiningar

Staðsetningarleiðbeiningar eru reglur sem hjálpa við auðkenningu tiltektar- og frágangsstaðsetninga fyrir birgðahreyfingar. Til dæmis, í sölupöntunarfærslu, ákvarða staðsetningarleiðbeiningar hvar vörurnar verða teknar til og hvar tilteknar vörur verða að setja. Staðsetningarleiðbeiningar samanstanda af haus tengdar línur, og þær eru stofnaðar á **staðsetningarleiðbeiningar** síðu.

Í haus verður hver staðsetningarleiðbeining að vera tengd við *gerð verkpöntunar* sem tilgreinir gerð birgðafærslu sem leiðbeiningarnar verður notuð fyrir, eins og sölupantanir, áfyllingu eða tiltekt hráefnis. *vinnutegund* tilgreinir hvort staðsetningarleiðbeininga verður notuð fyrir tiltekt eða setja, eða fyrir eitthvað annað vöruhúsaferli, eins og talningu eða birgðastöðubreytingu. Einnig þarf að tilgreina *svæði* og *vöruhús*. *leiðbeiningarkóði* sem þú tilgreina í haus er hægt að nota til að tengja staðsetningarleiðbeiningu við eitt eða fleiri vinnusniðmát . 

Eins og fyrir Vinnusniðmát, er hægt er að setja upp fyrirspurn til að ákvarða hvenær tiltekna staðsetningarleiðbeiningar er notað. Til dæmis er hægt að tilgreina að þegar e-commerce er uppruni sölupöntunar, verður að taka birgðir frá sérstöku svæði í vöruhúsinu. Kerfið notar **Raðnúmer** svæði til að ákvarða röð tiltækar staðsetningarleiðbeiningar eru metnar í.

Línur staðsetningarleiðbeiningar setja frekari takmarkanir á notkun staðsetningaleitarreglna. Hægt er að tilgreina lágmarksmagn og hámarksmagnið sem á við leiðbeiningarnar eiga að gilda um, og hægt er að tilgreina að leiðbeiningarnar eigi að vera fyrir tiltekna birgðaeiningu. Til dæmis, ef mælieiningin er bretti þá er hægt að setja vörur í brettum á tilteknum stað. Einnig er hægt að tilgreina hvort magnið sé hægt að skipta á mörgum staðsetningar. Líkt og staðsetningarleiðbeiningar haus, hver lína staðsetningarleiðbeiningar hefur raðnúmer sem ákvarðar röð sem línurnar eru metnar í.

Staðsetningarleiðbeiningar hafa eina viðbótar upplýsingastig: *aðgerðir í staðsetningarleiðbeiningum*. Hægt er að skilgreina margar aðgerðir í staðsetningarleiðbeiningum fyrir hverja línu. Einu sinni enn, númeraröð er notuð til að ákvarða röðun sem aðgerðir eru metnar í. Á þessu stigi er hægt að setja upp fyrirspurn til að skilgreina hvernig á að finna bestu staðsetningu í vöruhúsinu. Einnig er hægt að nota forskilgreint **Stjórnunarstefnu** stillingar til að finna bestu staðsetningu.

Frekari upplýsingar um hvernig á að stofna og skilgreina staðsetningarleiðbeiningar er að finna í [Stofna staðsetningarleiðbeiningu](create-location-directive.md).

### <a name="how-location-directives-work"></a>Hvernig staðsetningarleiðbeiningar virka

Staðsetningarleiðbeiningar ákvarða *hvar* vörur eru teknar til og *hvar* á að setja þær. Kerfið metur staðsetningarleiðbeiningar gagnvart hverri vinnulínu og velur síðan staðsetningu, samkvæmt upplýsingum vinnulínunnar. Kerfið finnur fyrst allar staðsetningartilskipanir sem samsvara tiltekinni vinnulínu (til dæmis að þær séu fyrir rétt vöruhús og samsvara fyrirspurninni). Það metur síðan þær tilskipanir sem það fann.

> [!NOTE]
> Sérstök tilvik eru til staðar þar sem staðsetning tiltektar eða frágangsstaðsetning er forvalin. Til dæmis, á _innkaupaskráning_ er fyrsta tiltekt til dæmis alltaf frá staðsetningu þar sem skráningin á sér stað. Annað dæmi er *birgðahreyfing eftir sniðmáti*, þar sem starfskraftur í vöruhúsi velur staðsetningu tiltektar og aðeins er hægt að finna frágangsstaðsetningar í gegnum staðsetningartilskipanir.

## <a name="additional-resources"></a>Frekari upplýsingar

- Myndskeið: [Ítarleg greining á grunnstillingum vöruhúsastjórnunar](https://community.dynamics.com/365/b/techtalks/posts/warehouse-management-configuration-deep-dive-october-14-2020)
- Hjálparefni: [Vinna með staðsetningarleiðbeiningar](create-location-directive.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]