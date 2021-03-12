---
title: Staðsetningarstaða vöruhúss
description: Þetta efnisatriði veitir yfirlit yfir eiginleikann staðsetningastaða vöruhúss.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationProfile,WHSLocation
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 29815abc2892aecb080a9b673f2336f5368821ce
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993779"
---
# <a name="warehouse-location-status"></a>Staðsetningarstaða vöruhúss

[!include [banner](../includes/banner.md)]

Microsoft Dynamics 365 Supply Chain Management inniheldur nokkur staðsetningarsvæði sem veita þér sveigjanleika þegar þú vinnur með og viðheldur staðsetningum. Þú getur haft staðsetningarstöður með í fyrirspurninni um staðsetningarleiðbeiningar til að veita betri stjórn á flæði vöruhúsa.

Eftirfarandi fjögur svæði á síðunni **Staðsetningar** rekja upplýsingar um núverandi stöðu tiltekinnar staðsetningar. Þessi svæði gefa stjórnendum vöruhúsa yfirsýn yfir stöðu staðsetninganna í vöruhúsinu. Þau bjóða einnig upp á háþróaða skýrslugerð og síun.

- **Vörunúmer** – Varan sem er núna í staðsetningunni. Ef staðsetningin inniheldur margar vörur er þessi reitur auður.
- **Dagsetning og tími síðustu virkni** – Tímastimpill síðustu færslu vöruhúss sem var framkvæmd á staðsetningunni.
- **Aldursdagsetning** –Dagsetningin sem birgðir í staðsetningu voru færðar inn í vöruhúsið. Þetta gildi er reiknað út frá aldursdagsetningu númeraplötunnar. Það er nákvæmt fyrir staðsetningar sem er raktar með númeraplötu, en er hugsanlega ekki nákvæmt fyrir staðsetningar sem eru ekki raktar með númeraplötu.
- **Staðsetningarstaða** – Staða staðsetningarinnar. Fjögur gildi eru möguleg:

    - **Óákveðið** – Staðsetningarforstillingin getur ekki rakið stöðuna. Þar af leiðandi er núverandi staða óþekkt.
    - **Tómt** – Það eru engar birgðir í staðsetningunni eins og stendur.
    - **Tiltekt** – Færslur á útleið hafa verið framkvæmdar á staðsetningunni Frá að hún var síðast tóm.
    - **Geymsla** – Aðeins færslur á innleið hafa verið framkvæmdar frá því að staðsetningin var síðast tóm.

## <a name="turn-on-the-warehouse-location-status-feature"></a>Kveiktu á eiginleikanum staðsetningarstaða vöruhúss

Áður en þú getur notað eiginleikann *staðsetningarstaða vöruhúss* verður að vera kveikt á henni í kerfinu þínu. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Heiti eiginleika:** *Staðsetningarstaða vöruhúss*

## <a name="set-up-warehouse-location-status"></a>Setja upp staðsetningarstöðu vöruhúss

### <a name="prepare-the-sample-data-that-is-required-for-the-example-scenario"></a>Undirbúið áskilin lýsigögn fyrir sýniaðstæðurnar

Áður en byrjað er að vinna í gegnum aðstæðurnar verður þú að virkja sýnigögn og setja upp eiginleikann eins og lýst er í þessum kafla. Til að klára sýniaðstæðurnar verðurðu að nota annað hvort vöruhúsaforritið eða hermiforritið í vafranum. Í skrefunum hér á eftir er notast við vöruhúsaforritið. Skrefin fyrir hermiforritið í vafranum eru svipuð.

#### <a name="use-the-usmf-legal-entity"></a>Nota USMF-lögaðilann

Til að vinna í gegnum sýniaðstæðurnar með því að nota sýnskrárnar og sýnigildin sem eru kynnt í þessu efnisatriði verður þú að vinna á kerfi þar sem venjulegu [sýnigögnin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) eru sett upp. Þar að auki verður þú að velja **USMF**-lögaðila áður en þú byrjar.

#### <a name="set-up-location-profiles"></a>Setja upp forstillingar staðsetningar

Sýniaðstæðurnar krefjast þess að þú búir til tvær staðsetningarforstillingar.

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Forstillingar staðsetningar**.
1. Veldu **Breyta** til að setja síðuna í breytingastillingu.
1. Veldu **BULK-06** forstillinguna.
1. Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:

    - **Virkja vöru á staðsetningu:** Stilltu þennan valkost á _Já_.
    - **Virkja dagsetningu og tíma staðsetningarvirkni:** Stilltu þennan valkost á _Já_.
    - **Virkja staðsetningarstöðu:** Stilltu þennan valkost á _Já_.

    Þessir valkostir stjórna því hvort viðmiðunarsvæði staðsetningarinnar séu virkir.

1. Endurtakið skref 3 til 4 fyrir **PICK-06** forstillinguna.

> [!NOTE]
> Þegar færibreyturnar á staðsetningarforstillingunni (**Virkja vöru á staðsetningu**, **Virkja staðsetningarvirkni**, **Virkja staðsetningarstöðu**) eru stilltar á *Já* uppfærir kerfið umsvifalaust staðsetningarnar sem eiga við með því að keyra *Samræmisathugun fyrir stöðu vöruhúsastaðsetningar* verkið.

### <a name="scenario"></a>Aðstæður

1. Farðu í **Innkaup og aðföng \> Innkaupapantanir \> Allar innkaupapantanir**.
1. Veljið **Nýtt**.
1. Í svarglugganum **Búa til innkaupapöntun** á flýtiflipanum **Lánardrottinn** á svæðinu **Lánardrottinslykill** skaltu velja *104*.
1. Á flýtiflipanum **Almennt**, í reitnum **Vöruhús**, er valið *61*.
1. Veljið **Í lagi**.
1. Nýja innkaupapöntunin þín opnast. Það felur í sér tóma línu í hnitaneti **Innkaupapöntunarlína**. Stilltu eftirfarandi gildi á þessari línu:

    - **Vörunúmer:** _A0002_
    - **Magn:** _5_

1. Á aðgerðasvæðinu, á flipanum **Innkaup** í hópnum **Aðgerðir** skaltu velja **Staðfesta** til að staðfesta innkaupapöntunina.
1. Opnaðu **Á innleið \> Móttaka innkaupa** í fartækinu.
1. Veldu reitinn **PONUM**, sláðu inn númer innkaupapöntunar og staðfestu.
1. Veldu svæðið **VARA** sláðu inn *A0002* sem vörunúmer og staðfestu.
1. Á síðunni **MAGN** sláðu inn *5* sem magnið og staðfestu.

    Hægt er að slá inn magnið á tvo vegu:

    - Ýttu á hnappinn með plúsmerki (**+**) eða mínusmerki (**–**) til að bæta við eða draga frá tölugildi.
    - Veldu auða reitinn milli hnappa plúsmerkisins (**+**) og mínusmerkisins (**–**) til að opna talnaborðið.

1. Staðfestu val þitt á vörunúmer *A0002* og magnið *5*. Skilaboðin „Vinnu er lokið“ birtast neðst á síðunni.
1. Veldu valmyndarhnappinn (stundum kallaður hamborgari eða hamborgarahnappur) efst í hægra horninu og veldu síðan **Hætta við** til að loka **Móttaka innkaupa** og fara aftur í valmyndina **Á innleið**.
1. Á síðu innkaupapöntunar velur þú **Upplýsingar um vinnu** fyrir ofan hnitanet **Innkaupapöntunarlína**.
1. Á flipanum **Almennt** skaltu skoða gildi **Vinnuauðkennisins** og **Auðkenni marknúmeraplötu** sem voru búin til.
1. Athugaðu í hlutanum **Línur** gildi **Staðsetningar** fyrir vinnugerðirnar *Tiltekt* og *Frágangur*.
1. Opnaðu **Á innleið \> Frágangur innkaupa** í fartækinu.
1. Veldu svæðið **Auðkenni**, sláðu inn vinnuauðkennið og staðfestu.
1. Staðfestu einu sinni enn til að ljúka færslunni *Tiltekt*.
1. Veldu valmyndarhnappinn efst í hægra horninu og veldu síðan **Lokið** til að ljúka vinnunni við *Tiltekt*.
1. Skráðu niður staðsetningu frágangs og staðfestu. Skilaboðin „Vinnu er lokið“ birtast neðst á síðunni.
1. Veldu valmyndarhnappinnefst í hægra horninu og veldu síðan **Hætta við** til að loka **Frágangur innkaupa** og fara aftur í valmyndina **Á innleið**.
1. Veldu **Til baka** til að fara til baka í aðalvalmyndina.
1. Í Dynamics 365 Supply Chain Management opnar þú **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Staðsetningar**.
1. Síaðu eftir **Staðsetningu** og sláðu inn staðsetningu frágangs úr vinnu innkaupapöntunar. Þú ættir að sjá eftirfarandi niðurstöður:

    - Dálkurinn **Staðsetningarstaða** sýnir gildið *Geymsla*, vegna þess að síðusta færsla á þessari staðsetningu var frágangur.
    - Dálkurinn **Vörunúmer** sýnir gildi *A0002*,, vegna þess að varan var móttekin og gengið frá henni á staðsetningunni.
    - Dálkurinn **Dagsetning og tími síðustu virkni** sýnir tímastimpil dagsetningar og tíma þegar vinnu var lokið á staðsetningunni.

1. Opnaðu **Gæði \> Hreyfingar** í fartækinu.
1. Veldu reitinn **LOC/LP** og sláðu inn staðsetninguna sem þú skráðir niður í skrefunum hér á undan.
1. Staðfestu upplýsingarnar sem eru sýndar. Skráið niður númeraplötunúmerið sem birtist.
1. Á skjámyndinni **Upplýsingar um færslu til** skaltu velja svæðið **LOC/LP** og slá inn *06A07R2S1B* sem staðsetninguna sem skal færa vöruna til.
1. Á skjánum **Upplýsingar um færslu til** skaltu staðfesta gildi **LP** (auðkenni marknúmeraplötunnar) sem er búið til sjálfkrafa. Skilaboðin „Vinnu er lokið“ birtast neðst á síðunni.
1. Veldu valmyndarhnappinnefst í hægra horninu og veldu síðan **Hætta við** til að loka **Hreyfingu** og fara aftur í valmyndina **Gæðastjórnun**.
1. Veldu **Til baka** til að fara til baka í aðalvalmyndina.
1. Í Dynamics 365 Supply Chain Management opnar þú **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Staðsetningar**.
1. Endurhladdu síðuna **Staðsetningar** og skoðaðu upprunalegu staðsetningu frágangsins á ný. Taktu eftir að svæðið **Staðsetningarstaða** er núna stillt á *Tómt* og dálkurinn **Vörunúmer** er auður.
1. Skoðaðu skrána fyrir staðsetningu *06A07R2S1B* og taktu eftir að gildi **Stöðu** hefur breyst í *Geymslu* og **Vörunúmerið** og svæðin **Dagsetning og tími síðustu virkni** hafa verið uppfærð.
1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Veljið **Nýtt**.
1. Í svarglugganum **Búa til sölupöntun** í svæðinu **Viðskiptavinalykill** skaltu velja *US-002*.
1. Í reitnum **Vöruhús** skal velja *61*.
1. Veljið **Í lagi**.
1. Nýja sölupöntunin þín opnast. Hún inniheldur tóma línu í hnitaneti **Sölupöntunarlína**. Stilltu eftirfarandi gildi á þessari línu:

    - **Vörunúmer:** _A0002_
    - **Magn:** _1_

1. Á flýtiflipanum **Sölupöntunarlínur** á valmyndinni **Birgðir** velur þú **Frátekning**.
1. Í síðunni **Frátekning** skal velja **Frátektarlota** til að taka frá pöntunarlínu. Loka skal síðunni með því að smella á hnappinn **Loka** (**X**) efst í hægra horninu.
1. Á aðgerðarrúðunni, á flipanum **Vöruhús**, í hópnum **Aðgerðir**, velurðu **Losa í vöruhús**.
1. Í hlutanum **Sölupöntunarlínur** á valmyndinni **Vöruhús** skaltu velja **Upplýsingar um vinnu**.
1. Afritaðu gildi **Vinnuauðkennisins** sem var búið til.
1. Opnaðu **Á útleið \> Sölutiltekt** í fartækinu.
1. Veldu svæðið **Auðkenni**, sláðu inn vinnuauðkennið sem þú afritaðir áður og staðfestu.
1. Á síðunni **Sölupantanir: Tiltekt** leggur svæðið **STAÐSETNING** til tiltektarstaðsetninguna sem frágangsstaðsetninguna sem var búin til áður. Skráið niður staðsetninguna.
1. Veldu svæðið **STAÐSETNING**, sláðu inn staðsetninguna og staðfestu.
1. Veldu reitinn **NÚMERAPLATA** og sláðu inn númeraplötunúmerið sem þú skráðir niður á meðan á hreyfingu stóð og staðfestu.
1. Veldu svæðið **Vara** sláðu inn *A0002* sem vörunúmerið og staðfestu.
1. Á síðunni **MAGN** sláðu inn *1* sem magnið og staðfestu.

    Hægt er að slá inn magnið á tvo vegu:

    - Ýttu á hnappinn með plúsmerki (**+**) eða mínusmerki (**–**) til að bæta við eða draga frá tölugildi.
    - Veldu auða reitinn milli hnappa plúsmerkisins (**+**) og mínusmerkisins (**–**) til að opna talnaborðið.

1. Veldu svæðið **MARKNÚMERAPLATA**, sláðu inn auðkenni marknúmeraplötunnar skilgreint af notanda og staðfestu.
1. Staðfestu enn og aftur til að klára tiltektarvinnuna. Skilaboðin „Vinnu er lokið“ birtast neðst á síðunni.
1. Veldu valmyndarhnappinnefst í hægra horninu og veldu síðan **Hætta við** til að ljúka tiltektarvinnunni og fara aftur í valmyndina **Á útleið**.
1. Í Dynamics 365 Supply Chain Management opnar þú **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Staðsetningar**.
1. Síaðu eftir **Staðsetningu** og sláðu inn staðsetningu tiltektar úr vinnu sölupöntunar.
1. Taktu eftir að svæðið **Staðsetningarstaða** sem sölupöntunarvinnan sem valin var úr er nú stillt *Tiltekt* og svæðið **Dagsetning og tími síðustu virkni** hefur verið uppfært.

> [!NOTE]
> Staðsetningarreitirnir eru aðeins uppfærðir með vöruhúsafærslum. Svæðin uppfærast ekki ef þú notar færslubók eða aðra ferla sem eru ekki vöruhúsakerfi til að færa birgðir.
