---
title: Fyrirspurn um gögn með farsímaforriti vöruhúsakerfis
description: Í þessari grein er lýst hvernig á að stilla í valmyndaratriði gagnafyrirspurna í fartæki og nota þau sem hluta af hjáleiðum.
author: perlynne
ms.date: 08/09/2022
ms.topic: article
ms.search.form: WHSMobileAppFlowStepListPage, WHSMobileAppFlowStepAddDetour,WHSMobileAppFlowStepDetourSelectFields
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 39677ebfb9babeb7246ece4d27ab1813435ca12e
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427849"
---
# <a name="query-data-using-warehouse-management-mobile-app-detours"></a>Fyrirspurn um gögn með farsímaforriti vöruhúsakerfis

[!include [banner](../includes/banner.md)]

## <a name="feature-introduction"></a>Kynnning á eiginleika

Með því að bjóða upp á eiginleika til skönnunar strikamerkja gefur farsímaforrit vöruhúsakerfis þér auðvelda og nákvæma leið til að taka upp gögn sem hluta af vöruhúsaferlum þínum. Strikamerkin eru hins vegar stundum skemmd og ólæsileg eða nauðsynlegar upplýsingar um gögnin eru mögulega ekki til sem strikamerki í viðskiptaferlinu þínu. Í slíkum tilvikum getur handvirkur innsláttur gagnanna tekið langan tíma og jafnvel valdið því að rangar upplýsingar eru teknar upp. Niðurstöður kunna að vera minnkuð afköst og lægra þjónustustig.

Með því að nota sveigjanlegt fyrirspurnarferli gagna geta starfskraftar auðveldlega flett upp nauðsynlegum upplýsingum sem hluta af innbyggðu farsímaforrit vöruhúsakerfis og beitt síunarvalkostum þannig að aðeins viðeigandi gögn séu sýnd. Þar af leiðir er handvirkt val hraðvirkara og nákvæmara.

Til dæmis, í móttökuflæði innkaupapöntunar, þarf innkaupapöntunarnúmer til að passa við komandi birgðir. Í þessu ferli getur þú auðveldlega stillt valmyndaratriði til að veita kortayfirlit yfir viðeigandi innkaupapöntunarnúmer. Á þennan hátt er hægt að halda áfram að taka á móti flæði með því að nota fljótlega benda til að velja aðferð. Þessi grein gefur dæmi um aðstæður, en einnig er hægt að nota eiginleikann innan hvers farsímaforrits sem er eða í öllum farsímaforritum vöruhúsakerfis.

## <a name="turn-on-the-data-inquiry-flow-feature-and-its-prerequisites"></a>Kveikja á eiginleikanum flæði gagnafyrirspurnar og skilyrðum hans

Áður en hægt er að nota eiginleikann sem lýst er í þessari grein verður að ljúka við eftirfarandi ferli til að kveikja á nauðsynlegum eiginleikum.

1. Opna skal **Kerfisstjórnun \> Vinnusvæði \> Eiginleikastjórnun**. (Nánari upplýsingar um notkun vinnusvæðisins **Eiginleikastjórnun** er að finna í [Eiginleikastjórnunaryfirlit](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).)
1. Ef þú ert að keyra útgáfu 10.0.28 eða fyrr af Supply Chain Management skaltu kveikja á eiginleikanum sem er skráður á eftirfarandi hátt:

    - **Eining:** *Vöruhúsakerfi*
    - **Heiti eiginleika:** *Leiðbeiningar fyrir skref vöruhúsaforrits*

    Þessi eiginleiki er skilyrði fyrir eiginleikann *Flæði gagnafyrirspurnar forritsins Warehouse Management*. Frá og með útgáfu 10.0.29 af Supply Chain Management er þetta áskilið og ekki er hægt að slökkva á því. Frekar upplýsingar um eiginleikann *Leiðbeiningar fyrir skref vöruhúsaforrits* er að finna í [Sérsníða þrepatitla og leiðbeiningar fyrir farsímaforrit Warehouse Management ](mobile-app-titles-instructions.md).

1. Virkjaðu eiginleikann sem er sýndur á eftirfarandi hátt:

    - **Eining:** *Vöruhúsakerfi*
    - **Heiti eiginleika:** *Hjáleiðir forrits vöruhúsakerfis*

    Þessi eiginleiki er skilyrði fyrir eiginleikann *Flæði gagnafyrirspurnar forritsins Warehouse Management*. Sem hluti af Supply Chain Management, útgáfa 10.0.29, er sjálfgefið kveikt á því. Frekari upplýsingar um eiginleikann *Hjáleiðir forrits vöruhúsakerfis* sjá [Skilgreina hjáleiðir fyrir skref í valmyndaratriðum fartækis](warehouse-app-detours.md).

1. Ef ekki var þegar kveikt á eiginleikanum *Hjáleiðir forrits vöruhúsakerfis* skaltu uppfærða heiti reita í farsímaforriti Warehouse Management með því að fara í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Reitarheiti vöruhúsaforrits** og veldu **Búa til sjálfgefna uppsetningu**. Endurtaktu þetta skref fyrir hvern lögaðila (fyrirtæki) þar sem þú notar farsímaforrit Warehouse Management. Frekari upplýsingar eru í [Skilgreina reiti fyrir farsímaforrit vöruhúsakerfis](configure-app-field-names-priorities-warehouse.md).
1. Virkjaðu eiginleikann sem er sýndur á eftirfarandi hátt:

    - **Eining:** *Vöruhúsakerfi*
    - **Heiti eiginleika:** *Flæði gagnafyrirspurnar forritsins Warehouse Management*

    Þessi eiginleiki er eiginleikinn sem lýst er í þessari grein.

## <a name="example-scenarios"></a>Dæmi um aðstæður

Þessi grein notar dæmi um aðstæður til að sýna hvernig hægt er *Flæði gagnafyrirspurnar forritsins Warehouse Management* til að bæta flæði innkaupakvittunar. Aðstæðurnar nota hefðbundin sýnisgögn, sem innihalda flæði sem er nefnt *Innkaup móttekin*. Þetta flæði hefst með því að hvetja starfskrafta til að auðkenna innkaupapöntunarnúmer sem þeir jafna við. Til að auðvelda starfskröftum að bera kennsl á innkaupapöntunina bætir þú við fyrstu síðu flæðisins með því að bæta við eftirfarandi nýjum fyrirspurnarmöguleikum sem [Hjáleiðum](warehouse-app-detours.md):

- **Flettu upp framleiðslupöntunum eftir lánardrottni** – Opnaðu síðu sem biður starfskrafta um að slá inn nafn lánardrottins eða hluta af nafni lánadrottins. Hægt er að nota algildisstafi. Til dæmis, ef starfskraftur á von á afhendingu á innleið í dag frá lánardrottni sem er með *Tailspin* í nafninu sínu, getur hann slegið inn **Tail\*** til að skoða spjald yfir opnar innkaupapantanir með þessum texta. Á hverju spjaldi eru nokkrir reitir sem gefa upplýsingar um hverja innkaupapöntun. Auk nafns lánardrottins getur þú hannað spjöldin þannig að þau sýni reikningsnúmer lánardrottnins, afhendingardag og stöðu skjalsins.
- **Fletta upp innkaupapöntunum fyrir daginn í dag** – Opnaðu síðu sem hvetur starfsmenn ekki til að slá inn gögn en sýnir í staðinn forstilltar síur (eins og dagsetningin í dag). Síðan sýnir síðan spjöld sem passa við síuna. Starfskraftar halda áfram með því að velja spjald fyrir innkaupapöntunina sem þeir vilja skrá birgðavörur á móti.
- **Fletta upp innkaupapöntunum eftir vöru** – Opnaðu síðu sem biður starfskrafta um að skanna strikamerki hvaða vöru sem er í birgðunum sem komu. Flæðið skráir svo allar opnar innkaupapantanir sem innihalda línur fyrir skannaða vörunúmerið. Til að fjalla um aðstæður þar sem ekki er hægt að lesa strikamerki er hægt að bæta annarri uppflettingu hjáleiðar við þessa síðu sem gerir starfskröftum kleift að leita að vörunúmerum í tiltekinni innkaupapöntun.

Í hverju tilviki auðkennir starfskraftur innkaupapöntun með því að velja spjald og síðan er farið aftur á fyrstu síðu, sem sýnir valið innkaupapöntunarnúmer. Starfskraftur getur þá haldið áfram skráningarflæði birgðavöru á innleið.

## <a name="enable-sample-data"></a>Virkja gögn sýnishorna

Til að vinna í gegnum sýniaðstæðurnar sem eru kynnt í þessu efnisatriði verður þú að vinna á kerfi þar sem venjulegu [sýnigögnin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) eru sett upp. Þar að auki verður þú að velja *USMF*-lögaðila (fyrirtæki) áður en þú byrjar.

## <a name="configure-the-mobile-device-menu-items"></a>Grunnstilling valmyndaatriði fartækisins

Til að búa til hverja nýja fyrirspurnarvalkosti sem þú þarft að bæta við fyrstu síðu flæðisins verður þú að setja hana upp sem valmyndaratriði fartækis. Síðar verður hægt að gera fyrirspurnarvalkostina aðgengilega sem hjáleið frá flæðinu *Innkaup móttekin*.

### <a name="create-the-look-up-pos-by-vendor-menu-item"></a>Stofna valmyndaratriðið „Fletta upp innkaupapöntunum eftir lánardrottni“

Stofna valmyndaratriðið **Fletta upp innkaupapöntunum eftir lánardrottni** með því að fylgja þessum skrefum.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Á aðgerðasvæðinu skal velja **Nýtt** til að bæta valmyndaratriði fartæki við hnitanetið.
1. Stillið eftirfarandi gildi fyrir nýju valmyndaratriði:

    - **Heiti valmyndaratriðis:** *Fletta upp innkaupapöntunum eftir lánardrottnum*
    - **Titill:** *Flettu upp innkaupapöntunum eftir lánardrottni*
    - **Stilling:** *Óbein*

1. Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:

    - **Aðgerðarkóði:** *Fyrirspurn um gögn*
    - **Nota leiðbeiningar fyrir ferli:** *Já* (Þetta gildi er valið sjálfkrafa.)
    - **Töfluheiti:** *PurchTable* (Þú munt fletta innkaupapöntunarnúmerum úr þessari töflu).

1. Í aðgerðasvæði velurðu **Breyta fyrirspurn** til að skilgreina fyrirspurn sem er byggð á valinni grunntöflu (í þessu tilviki töflu innkaupapöntunar).
1. Í fyrirspurnarritlinum, á flipanum **Svið**, bætið eftirfarandi línum við hnitanetið.

    | Tafla | Afleidd tafla | Svæði | Skilyrði |
    |---|---|---|---|
    | Innkaupapantanir | Innkaupapantanir | Staða innkaupapöntunar | Opin pöntun |
    | Innkaupapantanir | Innkaupapantanir | Afhendingardagur | (dayRange(-10,10)) |
    | Innkaupapantanir | Innkaupapantanir | Nafn lánardrottins | |

1. Veldu **Í lagi**.

    Í þessu dæmi er nýi valmyndaratriðið stilltur til að finna opnar innkaupapantanir sem eru væntanlegar hvenær sem er á milli 10 daga í fortíðinni og 10 daga í framtíðinni.

    Í fyrirspurninni hefur dálkurinn **Skilyrði** fyrir *Nafn lánardrottins* verið skilinn eftir auður. Því munu starfskraftar geta tilgreint þetta gildi á meðan þeir nota farsímaforrit vöruhúsakerfis.

    Ef þú vilt tilgreina hvernig listanum verður raðað getur þú sett upp röðunina á flipanum **Flokkun**.

1. Auk þess að skilgreina fyrirspurnina verður þú að velja hvaða reitir verða sýndir á spjöldum fyrirspurnarlistasíðunnar. Veljið því **Reitalisti** á aðgerðasvæðinu.
1. Á síðunni **Reitalisti** skal stilla eftirfarandi gildi:

    - **Birta reit 1:** *PurchId* (Þessi reitur verður birtur sem haus fyrir hvert spjald).
    - **Upplýsingasvæði 2:** *PurchStatus*
    - **Upplýsingasvæði 3:** *PurchName*
    - **Upplýsingasvæði 4:** *OrderAccount*
    - **Upplýsingasvæði 5:** *DeliveryDate*
    - **Sýna reit 6:** *displayDocumentStatus()* (Þetta gildi er birtingaraðferð, eins og "()" í lokin gefur til kynna.)

1. Í aðgerðarúðunni skal velja **Vista**. Því næst skal loka síðunni.

### <a name="create-the-look-up-pos-for-today-menu-item"></a>Stofna valmyndaratriðið „Flettu upp innkaupapöntunum fyrir daginn í dag“

Stofna valmyndaratriðið **Flettu upp innkaupapöntunum fyrir daginn í dag** með því að fylgja þessum skrefum.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Á aðgerðasvæðinu skal velja **Nýtt** til að bæta valmyndaratriði fartæki við hnitanetið.
1. Stillið eftirfarandi gildi fyrir nýju vöruna:

    - **Heiti valmyndaratriðis:** *Flettu upp innkaupapöntunum fyrir daginn í dag*
    - **Titill:** *Flettu upp innkaupapöntunum fyrir daginn í dag*
    - **Stilling:** *Óbein*

1. Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:

    - **Aðgerðarkóði:** *Fyrirspurn um gögn*
    - **Nota leiðbeiningar fyrir ferli:** *Já* (Þetta gildi er valið sjálfkrafa.)
    - **Töfluheiti:** *PurchTable* (Þú munt fletta innkaupapöntunarnúmerum úr þessari töflu).

1. Í aðgerðasvæði velurðu **Breyta fyrirspurn** til að skilgreina fyrirspurn sem er byggð á valinni grunntöflu (í þessu tilviki töflu innkaupapöntunar).
1. Í fyrirspurnarritlinum, á flipanum **Svið**, bætið eftirfarandi línum við hnitanetið.

    | Tafla | Afleidd tafla | Svæði | Skilyrði |
    |---|---|---|---|
    | Innkaupapöntun | Innkaupapöntun | Staða innkaupapöntunar | Opin pöntun |
    | Innkaupapöntun | Innkaupapöntun | Afhendingardagur | (Dagur(0)) |

1. Veldu **Í lagi**.

    Í þessu dæmi er nýi valmyndaratriðið stilltur til að finna opnar innkaupapantanir sem eru væntanlegar í dag.

    Ef þú vilt tilgreina hvernig listanum verður raðað getur þú sett upp röðunina á flipanum **Flokkun**.

1. Auk þess að skilgreina fyrirspurnina verður þú að velja hvaða reitir verða sýndir á spjöldum fyrirspurnarlistasíðunnar. Veljið því **Reitalisti** á aðgerðasvæðinu.
1. Á síðunni **Reitalisti** skal stilla eftirfarandi gildi:

    - **Birta reit 1** *PurchName* (Þessi reitur verður birtur sem haus fyrir hvert spjald).
    - **Upplýsingasvæði 2:** *PurchId*
    - **Upplýsingasvæði 3:** *PurchStatus*
    - **Upplýsingasvæði 4:** *DlvMode*
    - **Upplýsingasvæði 5:** *DlvTerm*
    - **Sýna reit 6:** *OrderAccount*
    - **Sýna reit 7:** *VendorName()* (Þetta gildi er birtingaraðferð, eins og "()" í lokin gefur til kynna.)

1. Í aðgerðarúðunni skal velja **Vista**. Því næst skal loka síðunni.

### <a name="create-the-look-up-pos-by-item-menu-item"></a>Stofna valmyndaratriðið „Fletta upp innkaupapöntunum eftir vörum“

Stofna valmyndaratriðið **Fletta upp innkaupapöntunum eftir vörum** með því að fylgja þessum skrefum.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Á aðgerðasvæðinu skal velja **Nýtt** til að bæta valmyndaratriði fartæki við hnitanetið.
1. Stillið eftirfarandi gildi fyrir nýju vöruna:

    - **Heiti valmyndaratriðis:** *Flettu upp stöðlum eftir atriðum*
    - **Titill:** *Fletta upp innkaupapöntunum eftir vörum*
    - **Stilling:** *Óbein*

1. Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:

    - **Aðgerðarkóði:** *Fyrirspurn um gögn*
    - **Nota leiðbeiningar fyrir ferli:** *Já* (Þetta gildi er valið sjálfkrafa.)
    - **Töfluheiti:** *PurchLine* (Þú vilt fletta upp innkaupapöntunarnúmerum miðað við vörunúmer í gegnum línugögnin).

1. Í aðgerðasvæði velurðu **Breyta fyrirspurn** til að skilgreina fyrirspurn sem er byggð á valinni grunntöflu (í þessu tilviki töflu innkaupapöntunarlínu, en hægt er að nota hvaða gildi sem er tengt hausnum með því að tengjast *PurchTable*).
1. Í fyrirspurnarritlinum, á flipanum **Svið**, bætið eftirfarandi línum við hnitanetið.

    | Tafla | Afleidd tafla | Svæði | Skilyrði |
    |---|---|---|---|
    | Innkaupapöntunarlínur | Innkaupapöntunarlínur | Staða línu | Opin pöntun |
    | Innkaupapöntunarlínur | Innkaupapöntunarlínur | Afhendingardagur | (dayRange(-10,10)) |
    | Innkaupapöntunarlínur | Innkaupapöntunarlínur | Vörunúmer | |

1. Veldu **Í lagi**.

    Í þessu dæmi er nýi valmyndaratriðið stilltur til að finna opnar innkaupapantanalínur sem eru væntanlegar hvenær sem er á milli 10 daga í fortíðinni og 10 daga í framtíðinni.

    Í fyrirspurninni hefur dálkurinn **Skilyrði** fyrir *Vörunúmer* verið skilinn eftir auður. Því munu starfskraftar geta tilgreint gildið á meðan þeir nota farsímaforrit vöruhúsakerfis.

    Ef þú vilt tilgreina hvernig listanum verður raðað getur þú sett upp röðunina á flipanum **Flokkun**.

1. Auk þess að skilgreina fyrirspurnina verður þú að velja hvaða reitir verða sýndir á spjöldum fyrirspurnarlistasíðunnar. Veljið því **Reitalisti** á aðgerðasvæðinu.
1. Á síðunni **Reitalisti** skal stilla eftirfarandi gildi:

    - **Sýna reit 1** *:* PurchId (Þetta reitagildi verður notað sem haus fyrir hvert spjald).
    - **Upplýsingasvæði 2:** *VendAccount*
    - **Upplýsingasvæði 3:** *PurchQty*
    - **Upplýsingasvæði 4:** *PurchUnit*
    - **Upplýsingasvæði 5:** *PurchStatus*

1. Í aðgerðarúðunni skal velja **Vista**. Því næst skal loka síðunni.

## <a name="add-the-new-mobile-device-menu-items-to-a-menu"></a>Bæta nýjum valmyndaratriði fartækis við valmynd

Nú er hægt að bæta þremur nýjum valmyndaratriðum fyrir fartæki við valmyndina fyrir fartæki. Þessu verki verður að ljúka áður en hægt er að nota valmyndaratriðin sem hluta af ferli hjáleiðar. Í þessu dæmi býrðu til nýja undirvalmynd og bætir nýju valmyndaratriðunum við hana.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmynd fartækis**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Í haus nýju færslunnar skal stilla eftirfarandi gildi:

    - **Nafn:** *Senda fyrirspurn*
    - **Lýsing:** *Senda fyrirspurn*

1. Á listanum **Tiltækar valmyndir og valmyndaratriði** skal finna og velja fyrsta valmyndaratriði fartækis sem var búið til. Smellið á hægri örvarhnappinn til að færa vöruna í yfir á listann **Valmyndarskipan**.
1. Endurtaka skal fyrri skref fyrir hina tvo nýju valmyndina.
1. Veljið **Aðalvalmyndina** á listasvæðinu vinstra megin.
1. Á listanum **Tiltækar valmyndir og valmyndaratriði** flettirðu niður að hlutanum **Valmyndir** og veljið nýja valmynd **Fyrirspurn**. Smellið á hægri örvarhnappinn til að færa vöruna í yfir á listann **Valmyndarskipan**.

## <a name="configure-detours-in-your-mobile-device-steps"></a>Stilla hjáleiðir í skrefum fartækisins

Til að ljúka uppsetningunni verður þú nú að nota stillingar hjáleiða á síðu **Skref fartækis** til að bæta þremur nýjum valmyndaratriðum í valmynd fartækis við fyrirliggjandi auðkenningarskref fyrir flæðið *Innkaup móttekin*.

1. Farðu í **Warehouse Management \> Uppsetning > Fartæki \> Skref fartækis**.
1. Í reitnum **Sía** slærðu inn *PONum*. Veljið svo *Skrefakennið: „PONum“* í fellilistanum.
1. Meðan færslan sem finnst er valin í hnitanetinu skal velja **Bæta við skilgreiningu skrefa** á Aðgerðasvæði. Í fellilista svargluggans sem birtist, skal stilla reitinn **Valmyndaratriði** á *Móttaka innkaupa*. Veldu svo **Í lagi** til að loka svarglugganum.
1. Á upplýsingasíðu nýju skilgreiningu skrefs (**Móttaka innkaupa: PONum**) á flýtiflipanum **Hjáleiðir í boði (valmyndaratriði)** skal velja **Bæta við** á tækjastikunni.
1. Í svarglugganum **Bæta við hjáleið** skaltu finna og velja valmyndaratriðið **Leita að innkaupapöntunum eftir lánardrottni** sem þú bjóst áður til.
1. Veldu **Í lagi** til að loka svarglugganum og bæta valda valmyndaratriði á hjáleiðalistann.
1. Veljið nýju hjáleiðina og veljið svo **Velja reiti til að senda** á tækjastikunni.
1. Í reitnum **Velja reiti til að senda** skaltu ekki bæta neinu við í hlutann **Senda frá innkaup móttekin** því þú vilt ekki senda nein gildi í valmyndaratriði hjáleiðarinnar. Hins vegar í hlutanum **Sækja í uppflettingu innkaupapantana eftir lánardrottni** skaltu stilla eftirfarandi gildi í auðu línunni sem þegar hefur verið bætt við þar:

    - **Afrit úr Flettu upp innkaupapöntunum eftir lánardrottni:** *Innkaupapöntun*
    - **Líma í Móttaka innkaupa:** *Innkaupapöntun*

1. Veldu **Í lagi** til að loka svarglugganum.
1. Endurtakið skref 4 til 9 fyrir hin tvö nýju valmyndaratriðin (**Flettið upp innkaupapöntunum fyrir daginn í dag** og **flettið upp innkaupapöntunum eftir vörum**). Eins og á við um valmyndaratriðið **Fletta upp innkaupapöntunum eftir lánardrottni** þá viltu ekki senda nein gögn til þessara hjáleiða, en þú vilt skila inn innkaupapöntunarnúmeri.
1. Lokið síðunni.

## <a name="try-a-purchase-receiving-flow-that-has-a-data-inquiry-as-part-of-a-detour"></a>Prófaðu að kaupa móttökuflæði sem er með gagnafyrirspurn sem hjáleið

Fylgdu eftirfarandi skrefum til að prófa nýju uppsetninguna á farsímaforritinu þínu.

1. Stofna nokkrar innkaupapantanir sem hafa línur fyrir vöruhús 51.
1. Farðu í fartæki eða hermi sem keyrir farsímaforrit vöruhúsakerfis og skráðu þig inn í vöruhús 51 með því að nota *51* sem notandakenni og *1* sem aðgangsorð.
1. Á valmynd farsímaforritsins velurðu **Á innleið** og síðan **Innkaup móttekin**.

    Þú ættir að sjá eftirfarandi síðu sem inniheldur þrjú ný valmyndaratriði.

    ![Móttaka innkaupa með innkaupapöntunarnúmeri.](media/wma-purchase-receive-po-num-with-detours.png "Móttaka innkaupa með innkaupapöntunarnúmeri")

1. Prófaðu mismunandi eiginleika og taktu eftir að þú getur sent innkaupapöntunarnúmer til baka með því að velja eitt af spjöldunum í listanum.

    ![Móttaka innkaupa með því að nota uppflettingu sölupantana eftir lánardrottni, dæmi 1.](media/wma-purchase-receive-lookup-po-vendor-keyin-detours.png "Móttaka innkaupa með því að nota uppflettingu sölupantana eftir lánardrottni, dæmi 1")

    ![Móttaka innkaupa með því að nota uppflettingu sölupantana eftir lánardrottni, dæmi 2.](media/wma-purchase-receive-lookup-po-vendor-detours.png "Móttaka innkaupa með því að nota uppflettingu sölupantana eftir lánardrottni, dæmi 2")

> [!TIP]
> Í stað þess að keyra móttökuflæðið með uppflettingu á valmyndaratriðinu **Innkaup móttekin** getur þú byrjað á fyrirspurnarflæði (**Aðal \> Fyrirspurn \> Leita að innkaupapöntunum eftir lánardrottni**) og kallað fram hjáleið til að keyra viðkomandi flæði með því að velja spjald á listanum. Til að nota þessa aðferð er hægt að skilgreina hjáleið á síðunni **Skref fyrir fartæki** fyrir skrefið sem hefur gildið **Skrefakenni** fyrir *GenericDataInquiryList*. Að því tilskildu að kveikt sé á eiginleikanum [*Fjölþrepa hjáleiðir fyrir fartækjaforrit Warehouse Management*](warehouse-app-detours.md) fyrir kerfið þitt getur þú einnig bætt við viðbótarhjáleið ef þörf krefur (þessi eiginleiki bætir við stuðningi við allt að tvö stig hjáleiða og má sérsníða hann til að styðja við fleiri stig).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
