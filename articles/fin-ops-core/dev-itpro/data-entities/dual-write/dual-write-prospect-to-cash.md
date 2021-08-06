---
title: Viðfang til sjóðstreymis í tvískiptingu
description: Þetta efni veitir upplýsingar um viðfang til sjóðstreymis í tvískiptri skrifun.
author: RamaKrishnamoorthy
ms.date: 01/07/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 0fcbc5b0f571e9f2cf7f1ad7c1e976d022199b47
ms.sourcegitcommit: f65bde9ab0bf4c12a3250e7c9b2abb1555cd7931
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/13/2021
ms.locfileid: "6542272"
---
# <a name="prospect-to-cash-in-dual-write"></a>Viðfang til sjóðstreymis í tvískiptingu

[!include [banner](../../includes/banner.md)]

Mikilvægt markmið flestra fyrirtækja er að umbreyta viðföngum í viðskiptavini og halda síðan áframhaldandi viðskiptasambandi við þá viðskiptavini. Í forritum Microsoft Dynamics 365 verður ferli viðfanga til sjóðstreymis með tilboðum eða verkflæði pöntunarvinnslu og fjárhagurinn er afstemmdur og viðurkenndur. Samþætting möguleika á peningum með tvískiptri skrifun skapar verkflæði sem tekur tilvitnun og pöntun sem er upprunnin í annaðhvort Dynamics 365 Sales eða Dynamics 365 Supply Chain Management, og gerir tilboðið og pöntunina aðgengileg í báðum forritunum.

Í viðmótum forritsins geturðu fengið aðgang að vinnslustöðum og reikningsupplýsingum í rauntíma. Þess vegna geturðu auðveldlega stjórnað aðgerðum eins og afurðabirgðum, meðhöndlun birgða og uppfyllingu í Supply Chain Management, án þess að þurfa að endurstofna tilboð og pantanir.

![Tvískipt gagnaflæði í viðfang til sjóðstreymis.](../dual-write/media/dual-write-prospect-to-cash[1].png)

Frekari upplýsingar um samþættingu viðskiptavinar og tengiliðar er að finna í [Samþætt aðalsniðmát viðskiptavinar](customer-mapping.md). Frekari upplýsingar um samþættingu afurðar er að finna í [Samræmd afurðarupplifun](product-mapping.md).

> [!NOTE]
> Í Dynamics 365 Sales vísa bæði viðfang og viðskiptavinur í færslu í töflunni **Reikningur** þar sem dálkurinn **RelationshipType** er annaðhvort **Viðfang** eða **Viðskiptavinur**. Ef viðskiptagrunnurinn felur í sér hæfnisferilinn **Reikningur** þar sem færslan **Reikningur** er stofnuð og telst hæf sem viðfang fyrst og síðan sem viðskiptavinur mun sú færsla samstillast við Finance and Operations-forritið þegar hún er viðskiptavinur (`RelationshipType=Customer`). Ef ætlunin er að línan **Reikningur** samstillist sem viðfang þarf að sérstillta vörpun til að samþætta viðfangsgögnin.

## <a name="prerequisites-and-mapping-setup"></a>Skilyrði og vörpunaruppsetning

Áður en þú getur samstillt sölutilboð verður þú að uppfæra eftirfarandi stillingar.

### <a name="setup-in-sales"></a>Uppsetning í Sales

Í Sölu ferðu í **Stillingar \> Stjórnun \> Kerfisstillingar \> Sala** og gangið úr skugga um að eftirfarandi stillingar séu notaðar:

- Kerfisvalkosturinn **Nota verðútreikning kerfis** er stilltur á **Já**.
- **Reikningsaðferð reikningsafslátta** dálkurinn er stilltur á **Línuatriði**.

### <a name="sites-and-warehouses"></a>Svæði og vöruhús

Í Supply Chain Management eru dálkarnir **Vefsvæði** og **vörugeymsla** nauðsynlegir fyrir tilboðslínur og pöntunarlínur. Ef þú stillir vefinn og vöruhúsið í sjálfgefnum pöntunarstillingum verða þessir dálkar sjálfkrafa stilltir þegar þú bætir vöru við tilboðslínu eða pöntunarlínu. 

### <a name="number-sequences-for-quotations-and-orders"></a>Númeraröð fyrir tilboð og pantanir

Númeraraðirnar fyrir Supply Chain Management og Sölu eru ekki tengdir þegar tilboð og pantanir eru búnar til og samstilltar í sölu- og Supply Chain Management. Ef sölupöntun sem er búin til í Sölu er samstillt við Supply Chain Management hefur hún sama sölupöntunarnúmer í Supply Chain Management. Til að tryggja að sölupöntunarnúmerið sé ekki tvítekið verður þú að nota mismunandi númeraraðakerfi í forritunum tveimur.

Til dæmis er númeraröðin í Supply Chain Management **1, 2, 3, 4, 5, ...** og númeraröðin í Sölu er **100, 99, 98, ...**. Ef þú býrð til 100 sölupantanir í Sölu verður að lokum búið til pöntunarnúmer sem þegar er til í Supply Chain Management. Með öðrum orðum munu númeraraðirnar tvær að lokum skarast þar sem sölupantanir eru búnar til í Supply Chain Management og Sölu. Í staðinn gætirðu notað talaröð eins og **F1, F2, F3, ...** í Supply Chain Management og númeraröð eins og **C1, C2, C3, ...** í sölu. Þessar númeraraðir munu aldrei framleiða afrituð sölupöntunarnúmer.

## <a name="sales-quotations"></a>Sölutilboð

Sölutilboð má stofna í annaðhvort Sales eða Supply Chain Management. Ef þú býrð til tilvitnun í Sales er það samstillt við Supply Chain Management í rauntíma. Eins, ef þú býrð til tilboð í Supply Chain Management er það samstillt við Sales í rauntíma. Athugið eftirfarandi stig:

+ Þú getur bætt afslátt við vöruna í tilboðinu. Í þessu tilfelli verður afslátturinn samstilltur við Supply Chain Management. Dálkarnir **Afsláttur**, **Gjöld** og **Skattur** á hausnum er stjórnað af uppsetningu í Supply Chain Management. Þessi uppsetning styður ekki samþættingarvörpun. Þess í stað er dálkunum **Verð**, **Afsláttur**, **Gjöld** og **Skattur** viðhaldið og þeir meðhöndlaðir í Supply Chain Management.
+ Dálkarnir **Afsláttur %**, **Afsláttur** og **Flutningsupphæð** í sölutilboðshausnum eru skrifvarðir.
+ Dálkarnir **Flutningsskilmálar**, **Afhendingarskilmálar**, **Sendingaraðferð** og **Afhendingarmáti** eru ekki hluti af sjálfgefnum vörpunum. Til að varpa þessum dálkum, verður þú að setja upp gildisvörpun sem er bundin við gögnin í þeim fyrirtækjum sem taflan er samstillt á milli.

Ef þú notar líka Field Service-lausnina skaltu vertu viss um að virkja færibreytuna **Flýtistofnun tilboðslínu**. Með því að virkja breytuna aftur geturðu haldið áfram að búa til tilboðslínur með flýtiaðgerðinni.

1. Farðu í Dynamics 365 Sales forritið.
2. Veldu stillingartáknið efst í yfirlitsstikunni.
3. Veljið **Ítarlegar stillingar**.
4. Veldu valkostinn **Sérsníða kerfið**.
5. Veldu valmyndaratriðið **Tilboðslína**.
6. Farðu í hlutann **Gagnaþjónusta** og veldu gátreitinn **Leyfa flýtistofnun**.

## <a name="sales-orders"></a>Sölupantanir

Sölupantanir má stofna í annaðhvort Sales eða Supply Chain Management. Ef þú býrð til sölupöntun í Sales er það samstillt við Supply Chain Management í rauntíma. Eins ef þú býrð til sölupöntun í Supply Chain Management er hún samstillt við Sales í rauntíma. Athugið eftirfarandi stig:

+ Skráningarvörur á Dynamics 365 Sales munu birtast sem vöruflokkar í Dynamics 365 Supply Chain Management.
+ Afsláttarútreikningur og sléttun:

    - Útreikningur útreikningslíkansins í Sales er frábrugðin útreikningslíkaninu í Supply Chain Management. Í Supply Chain Management má endanlega afsláttarverð á sölulínu vera niðurstaða af samsetningu af afslætti og afsláttarhlutföllum. Ef lokaafsláttarupphæð er skipt eftir magni sem er á línunni, getur sléttun átt sér stað. Hins vegar er sléttunin ekki talin með ef afsláttarupphæð á einingu er samstillt við Sales. Til að tryggja að öll afsláttarupphæðin úr sölulínu í Supply Chain Management sé rétt samstillt við Sales verður heildarupphæðin að vera samstillt án þess að vera skipt eftir líumagni. Þess vegna verður þú að skilgreina afsláttarreikningsaðferðina sem **Línuvara** í Sales.
    - Þegar sölupöntunarlína er samstillt úr Sales í Supply Chain Management er heildarlínuafsláttarupphæðin notuð. Vegna þess að Supply Chain Management hefur engan dálk sem geymir heildarfjárhæðina fyrir línu, er upphæðinni skipt niður með magni og geymt á dálkinum **Línuafsláttur**. Öll frávik sem eiga sér stað eru vistuð í dálkinum **Sölulaun** á sölulínunni.

### <a name="example-synchronization-from-sales-to-supply-chain-management"></a>Dæmi: Samstilling úr Sales við Supply Chain Management

Þú ert með eftirfarandi sölupöntun:

+ **Sala:** Magn= 3, línuafsláttur = $10,00
+ **Supply Chain Management:** Magn = 3, línuafsláttarupphæð = $3,33, sölugjald = -$ 0,01

Ef þú samstillir úr Supply Chain Management í sölu færðu eftirfarandi niðurstöðu:

+ **Supply Chain Management:** Magn = 3, línuafsláttarupphæð = $3,33, sölugjald = -$ 0,01
+ **Sala:** magn = 3, línuafsláttur = (3 × $3,33) + $0,01 = $10,00

## <a name="dual-write-solution-for-sales"></a>Tvöfaldur skrifa lausn fyrir sölu

Nýjum dálkum hefur verið bætt við töfluna **Pöntun** og birtast á síðunni. Flestir þessir da´lkar birtast á flipanum **Samþætting** í Sales. Frekari upplýsingar um hvernig stöðudálkum er varpað er að finna í [Setja upp vörpun fyrir stöðudálka sölupantana](sales-status-map.md).

+ Hnapparnir **Stofna reikning** og **Hætta við pöntun** á síðunni **Sölupöntun** eru faldir í Sales.
+ Gildið **Staða sölupöntunar** verður áfram **Virk** til að tryggja að gjöld úr Supply Chain Management geti flætt í sölupöntun í Sales. Til að stjórna þessu er sjálfgefið **Statecode \[Status\]** stillt á **Virkt**.

## <a name="invoices"></a>Reikningar

Sölureikningar eru búnir til í Supply Chain Management og samstilltir við Sales. Athugið eftirfarandi stig:

+ Dálkinum **Reikningsnúmer** hefur verið bætt við töfluna **Reikningur** og birtist á síðunni.
+ Hnappurinn **Stofna reikning** á síðunni **Sölupöntun** er falinn vegna þess að reikningar verða búnir til í Supply Chain Management og samstilltir við Sales. Ekki er hægt að breyta síðunni **Reikningur** vegna þess að reikningar verða samstilltir úr Supply Chain Management.
+ **Staða sölupöntunar** breytist sjálfkrafa í **Reikningsfært** þegar tengdur reikningur úr Supply Chain Management hefur verið samstilltur við Sales. Einnig var eiganda sölupöntunar sem reikningurinn var búinn til úr úthlutað sem eiganda reikningsins. Því getur eigandi sölurekningsins skoðað reikninginn.
+ Dálkarnir **Flutningsskilmálar**, **Afhendingarskilmálar** og **Afhendingarmáti** eru ekki hluti af sjálfgefnum vörpunum. Til að varpa þessum dálkum, verður þú að setja upp gildisvörpun sem er bundin við gögnin í þeim fyrirtækjum sem taflan er samstillt á milli.

## <a name="templates"></a>Sniðmát

Viðfang til sjóðstreymis innihalda safn af kjarnatöflukortum sem vinna saman í gagnasamskiptum, eins og sýnt er í eftirfarandi töflu.

| Finance and Operations-smáforrit | Forrit viðskiptavinatengsla | lýsing |
|-----------------------------|-----------------------------------|-------------|
[Allar afurðir](mapping-reference.md#138) | msdyn_globalproducts | |
[Viðskiptavinir V3](mapping-reference.md#101) | lyklar | |
[Viðskiptavinir V3](mapping-reference.md#116) | tengiliðir | |
[Tengiliðir V2](mapping-reference.md#221) | msdyn_contactforparties | |
[Hausar CDS-sölupöntunar](mapping-reference.md#217) | salesorders | |
[CDS sölupöntunarlínur](mapping-reference.md#216) | salesorderdetails | |
[CDS-sölutilboðshaus](mapping-reference.md#215) | tilboð | |
[CDS-sölutilboðslínur](mapping-reference.md#214) | quotedetails | |
[Útgefnar afurðir V2](mapping-reference.md#189) | msdyn_sharedproductdetails | |
[Sölureikningshausar V2](mapping-reference.md#118) | reikningar | Sölureikningshausar V2 í töflu í Finance and Operations-forritinu innihalda reikninga fyrir sölupantanir og reikninga með frjálsum texta. Sía er notuð í Dataverse fyrir tvöfalda skráningu sem mun sía út öll skjöl reikninga með frjálsum texta. |
[Sölureikningslínur V2](mapping-reference.md#117) | invoicedetails | |
[Upprunakóðar sölupantana](mapping-reference.md#186) | msdyn_salesorderorigins | |

Frekari upplýsingar um verðlista er að finna í [Samræmd afurðaupplifun](product-mapping.md).

## <a name="limitations"></a>Takmarkanir

- Skilapantanir eru ekki studdar.
- Kreditnótur eru ekki studdar.
- Stilla verður fjárhagsvíddir fyrir aðalgögnin, til dæmis viðskiptavin og lánardrottin. Þegar viðskiptavini er bætt við tilboð eða sölupöntun flæða fjárhagsvíddirnar sem tengjast viðskiptavinafærslunni til pöntunarinnar sjálfkrafa. Sem stendur inniheldur tvöföld skráning ekki gögn fjárhagsvídda fyrir aðalgögn.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
