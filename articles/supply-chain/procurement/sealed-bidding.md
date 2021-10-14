---
title: Lokuð tilboð fyrir tilboðsbeiðnir
description: Í þessu efnisatriði er lýst hvernig setja skal upp innsiglað tilboð til að halda svörum við tilboði söluaðila leyndum þar til þau eru óinnsigluð af starfsfólki kaupanda.
author: Henrikan
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 96549b6053ba75f2d5b9a85bcd5b7feb006f0f1b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7578081"
---
# <a name="sealed-bidding-for-rfqs"></a>Lokuð tilboð fyrir tilboðsbeiðnir

[!include [banner](../includes/banner.md)]

Innsigluð tilboð heldur boðsvörum leyndum þar til þau eru óinnsigluð af starfsfólki kaupanda. Öll tilboð sem tengjast tilboðsbeiðni verður fyrst hægt að rjúfa innsiglið á þegar tilboðsglugginn rennur út. Áður en tilboð er óinnsiglað geta aðeins notendur sem hafa sérstök notandahlutverk og eru fulltrúar lánardrottins fengið aðgang að því.

> [!IMPORTANT]
> Að breyta eða stækka skjámyndir eða búa til nýjar skjámyndir eða viðskiptagrunn getur grafið undan vörnum sem Microsoft býður upp á fyrir innsigluð tilboð. Þú tekur áhættuna á að nota breytingar, viðbætur, nýjar skjámyndir eða viðskiptagrunn eða að geta ekki notað eiginleika innsiglaðs tilboðs vegna slíkra breytinga, viðbóta, nýrr skjámynda eða viðskiptagrunns.  Microsoft ber ekki ábyrgð á neinum skemmdum sem kunna að verða vegna breytinga eða viðbóta á skjámyndum, eða nýjum skjámyndum eða viðskiptagrunni sem þú býrð til eða einhver þriðji aðili býr til fyrir þig. Microsoft veitir hvorki tæknilegan stuðning né annan stuðning vegna breytinga, viðbóta, nýrra skjámynda eða viðskiptagrunns sem þú eða þriðji aðili hefur gert fyrir þína hönd. Þú berð alla ábyrgð á að fylgja öllum viðeigandi lögum og reglugerðum varðandi innsiglað boð.

## <a name="how-bids-are-kept-secure"></a>Hvernig tilboðum er haldið öruggum

Innsigluð boð nota ósamhverfa dulkóðun til að dulkóða dulkóðunarlykil tilboðs (KEK) og samhverfa dulkóðun til að dulkóða raunverulegt boð. Kerfið samþættist við Microsoft Azure lyklageymslu til að mynda og stjórna dulritunarlyklum sem eru notaðir til að dulkóða innsigluð kauptilboð. Hvert boð hefur sinn eigin dulritunarlykil. Þessi dulkóðun er geymd örugg í lyklageymslu sem er í eigu fyrirtækisins sem keyrir Dynamics 365 Supply Chain Management. Kerfið fær aðgang að lyklageymslunni eftir þörfum, þegar krafist er dulkóðunar og afkóðunar.

## <a name="setup-and-configuration"></a>Uppsetning og skilgreining

Í þessum hluta er lýst forsendum sem verða að vera til staðar áður en hægt er að senda út beiðni um tilboð sem krefjast innsiglaðs útboðs.

### <a name="step-1-set-up-user-access-to-sealed-bidding"></a>Skref 1: Settu upp aðgang notenda að innsigluðum tilboðum

Þegar þú notar innsiglað tilboð geta aðeins notendur sem eru tengiliðir lánardrottins skoðað, breytt og lagt fram tilboð fyrir þann lánardrottinn þar til tilboðstímabilið rennur út. Þessir notendur verða að hafa hlutverkið **Lánardrottinn (ytri)** og þeir verða að vera stilltir sem tengiliður fyrir lánardrottnalykilinn. Tengiliður verður einnig að hafa leyfi til samstarfs við lánardrottna, eins og lýst er í [Uppsetning og viðhald samstarfs lánardrottna](set-up-maintain-vendor-collaboration.md).

Þar sem notendur sem hafa viðeigandi heimildir og eru settir upp sem tengiliðir lánardrottins geta fengið aðgang að innsigluðum tilboðum fyrir lánardrottins er mikilvægt að fylgjast með því hverjir þeir notendur eru. Kerfisstjóri sem setur upp notendur og sinnir öryggishlutverki ber ábyrgð á því að takmarka aðgang að lokuðum tilboðum við þá notendur sem hafa í raun leyfi til að skoða þau.

### <a name="step-2-enable-the-sealed-bidding-feature"></a>2. skref: Virkjaðu innsiglaða tilboðseiginleikann

Áður en hafist er handa við að setja upp eða nota þennan eiginleika þarf að ganga úr skugga um að hann sé í boði í kerfinu. Stjórnendur geta notað vinnusvæðið **[Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** til að athuga stöðu eiginleikans og kveikja á honum. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Innkaup og uppruni*
- **Heiti eiginleika:** *Innsiglað tilboð fyrir tilboðsbeiðni*

### <a name="step-3-set-up-azure-key-vault"></a>3. skref: Setja upp Azure-lyklageymslu

Supply Chain Management notar dulkóðunarlykla til að vernda öll innsigluð boð og halda þeim leyndum þar til viðeigandi tími er liðinn. Það nýtir sér eiginleika Key Vault til að mynda og stjórna nauðsynlegum lyklum. Því verður að setja upp tengingu frá Supply Chain Management til lyklageymslu til að virkja kerfið.

> [!IMPORTANT]
> Lyklageymslurnar sem þú notar fyrir innsigluð tilboð verða að uppfylla eftirfarandi kröfur:
>
> - Ef þú notar sandkassa til að þróa og prófa þá þarftu að vera með eina sérstaka lyklageymslu fyrir sandkassann og aðra fyrir vinnsluna.
> - Hverja lyklageymslu þarf að búa til í Azure-áskrift sem fyrirtækið þitt á (ekki áskriftin þar sem þú keyrir Supply Chain Management).
> - Hver lyklageymsla skal eingöngu vera notuð fyrir innsigluð tilboð. Þú mátt ekki nota lyklageymslur innsiglaðra tilboða í neinum öðrum tilgangi.

Hvert boð sækir sinn eigin leynilykil. Þessi lykill er notaður í hvert sinn sem notandi skoðar, uppfærir eða opnar tilboð.

Lyklageymsla býr til lykilinn sem er notaður til að sækja leynilykilinn þegar lánardrottinn velur **Kauptilboð** í viðmóti lánardrottnasamstarfs. Lykillinn rennur síðan út eftir ákveðinn tíma sem innkaupastjóri setur upp á síðunni **Færibreytur innkaupa og aðfanga** í Supply Chain Management. Eftir að lykillinn rennur út getur enginn skoðað, breytt eða opnað tilboðið. Því er mikilvægt að stilla gildistíma lykilsins þannig að nægur tími gefist til að ljúka tilboðsferlinu.

Í næstu þremur skrefum setur þú upp tenginguna við lyklageymsluna. Fyrst er lyklahvelfing sett upp sem nota á með innsigluðum boðum. Næst stillir þú stjórnun Supply Chain Management til að eiga samskipti við lykilhvelfinguna. Að lokum stillir þú gildistíma lykils.

### <a name="step-4-set-up-a-key-vault-to-use-with-sealed-bidding"></a>Skref 4: Settu upp lyklageymslu til að nota með innsigluðum boðum

Til að setja upp lyklageymsluna skal fylgja þessum skrefum. Röð skrefanna er mikilvæg.

1. Ef þú hefur ekki þegar sett upp Azure-áskrift sem er aðskilin frá áskriftinni þar sem þú stýrir Supply Chain Management skaltu setja hana upp.
1. Uppsetning lykilhvelfingar í sérstakri Azure geymslu. Frekari upplýsingar er að finna í [Stjórna Azure-lyklageymslu](https://support.microsoft.com/help/4040294/maintaining-azure-key-vault-storage).
1. Settu upp Supply Chain Management forritið þitt þannig að það virki sem biðlari fyrir lyklageymsluna þína. Frekari upplýsingar eru í [Biðlari Azure-lyklageymslu settur upp](https://support.microsoft.com/help/4040305/setting-up-azure-key-vault-client).

### <a name="step-5-configure-key-vault-parameters-in-supply-chain-management"></a>Skref 5: Stilla færibreytur lyklageymslu í Supply Chain Management

Til að stilla Supply Chain Management til að eiga samskipti við lyklageymsluna meðan á innsigluðu kauptilboði stendur skal fylgja þessum skrefum.

1. Skráðu þig inn í Supply Chain Management og farðu í **Kerfisstjórnun \> Uppsetning \> Færibreytur lyklageymslu**.
1. Veldu **Ný** til að búa til færslu og stilltu eftirfarandi reiti fyrir hana:

    - **Heiti** - Sláðu inn nafn.
    - **Lýsing** - Færið inn lýsingu.
    - **Vefslóð lyklageymslu** – Sláðu inn sjálfgefna vefslóð fyrir lyklageymsluna þína.
    - **Biðlari lyklageymslu** – Sláðu inn gagnvirkt biðlarakenni Active Directory forritsins sem tengist lyklageymslu vegna auðkenningar.
    - **Leynilykill lyklageymslu** – Sláðu inn leyninúmerið fyrir vottorðið.
    - **Virkt fyrir lokuð tilboð** - Stilltu þennan valkost á *Já*

![Færibreytusíða lyklageymslu](media/sealed-bidding-key-vault-param.png "Færibreytusíða lyklageymslu")

> [!NOTE]
> Aðeins er hægt að virkja eina skilgreiningu lyklageymslu í einu fyrir innsiglað kauptilboð. Áður en þú slekkur á núverandi skilgreiningu lyklageymslu verður þú að ganga úr skugga um að öll innsigluð kauptilboð sem nota hana séu óinnsigluð. Skoðaðu allar tilboðsbeiðnir af gerðinni *Innsiglað* og gakktu úr skugga um að öll svör fyrir hana séu óinnsigluð.

### <a name="step-6-set-the-key-expiration-time"></a>Skref 6: Stilla gildistíma lykils

Til að stilla gildistíma sem er notaður á lykilinn sem er búinn til fyrir hvert nýtt tilboð skal fylgja eftirfarandi skrefum.

1. Farðu í **Færibreytur innkaupa og aðfanga \> Uppsetning \> Færibreytur innkaupa og aðfanga**.
1. Í flipann **Tilboðsbeiðni**, í reitinn **Hliðrun daga**, skal færa inn fjölda daga sem tímabil tilboðsbeiðni á að endast. Þegar tilboðsbeiðni er stofnuð er dagafjöldanum sem þú slærð hér inn bætt við kerfisdagsetninguna til að skilgreina sjálfgefna lokadagsetningu fyrir tilboðsbeiðnina.
1. Í reitinn **Hliðrun á lokadegi dulritunarlykils** skal færa inn fjölda daga sem allir dulritunarlyklar eiga að gilda um eftir að þeir eru gefnir út. Eftir að dulritunarlykillinn rennur út getur enginn sem notar hann skoðað, breytt eða opnað innsiglað tilboðið.

> [!TIP]
> Gildi reitsins **Hliðrun á lokadegi dulritunarlykils** á ekki að vera minni en gildið í reitnum **Hliðrun daga**.

### <a name="step-7-set-the-default-bid-type"></a><a name="set-default-bid-type"></a>Skref 7: Stilla sjálfgefna tilboðsgerð

Allar tilboðsbeiðnir eru með tilboðsgerð. Tilboðsgerðin skilgreinir hvort tilboðsbeiðnin bjóði upp á opið eða innsiglað tilboð.

#### <a name="rfq-cases-that-dont-have-a-solicitation-type"></a>Tilboðsbeiðnir sem eru ekki með beiðnigerð

Til að stilla sjálfgefna tilboðsgerð sem er úthlutað nýjum tilboðsbeiðnum sem er ekki úthlutað beiðnigerð þegar þær eru stofnaðar skal fylgja þessum skrefum.

1. Farðu í **Færibreytur innkaupa og aðfanga \> Uppsetning \> Færibreytur innkaupa og aðfanga**.
1. Í flipanum **Tilboðsbeiðni** skal stilla reitinn **Gerð kauptilboðs** á *Innsiglað*.

#### <a name="rfq-cases-that-have-a-solicitation-type"></a>Tilboðsbeiðnir sem eru með beiðnigerð

Til að stilla sjálfgefna tilboðsgerð sem er úthlutað nýjum tilboðsbeiðnum sem er úthlutað beiðnigerð þegar þær eru stofnaðar skal fylgja þessum skrefum.

1. Farðu í **Innkaup og aðföng \> Uppsetning \> Tilboðsbeiðnir \> Gerð beiðni**.
1. Búðu til nýja beiðnigerð eða veldu núverandi beiðnigerð þar sem þú vilt nota tilboð af gerðinni *Innsiglað*.
1. Stilltu reitinn **Gerð kauptilboðs** á *Innsiglað*.
1. Skrefin eru endurtekin fyrir hverja tegund útboða þar sem óskað er eftir innsigluðum tilboðum.

> [!TIP]
> Ekki þarf að úthluta tegund tilboða þegar ný beiðni um tilboð er búin til. Ef beiðnigerð er úthlutað getur sjálfgefin kauptilboðsgerð tilboðsbeiðni sótt hana. Annars er hægt að nota sjálfgefna úthlutunargerð sem er skilgreind í færibreytum innkaupa og aðfanga.

## <a name="the-sealed-bidding-process"></a>Lokaða tilboðsferlið

Innsiglað tilboð fylgir nánast sama ferli og lýst er í [Yfirliti yfir tilboðsbeiðnir](request-quotations.md). Meginmunurinn er sá að útboðsgögnin og viðhengi þeirra eru geymd dulkóðuð þar til útboðið er opnað.

> [!IMPORTANT]
> [Spurningalistar](/dynamicsax-2012/appuser-itpro/view-and-respond-to-questionnaires) eru ekki dulkóðaðir og ætti ekki að nota þá til að safna viðkvæmum upplýsingum

Hér er yfirlit yfir ferlið:

1. Þú stofnar og sendir BUT til eins eða fleiri lánardrottna.
1. Lánardrottnar svara með því að leggja fram innsiglað tilboð sitt.
1. Þú opnar tilboðin eftir að tíminn til að senda inn kauptilboð rennur út.
1. Tilboðin verða sýnileg og hægt er að meta þau og bera saman.
1. Eftir að tilboð hefur verið samþykkt er hægt að búa til innkaupapöntun, búa til innkaupasamning eða uppfæra innkaupabeiðni.

### <a name="create-an-rfq-case-that-uses-sealed-bidding"></a>Búa til RFQ-mál sem notar innsiglað tilboð

Ferlið við að búa til tilboðsbeiðni fyrir innsiglað kauptilboð er næstum það sama og ferlið fyrir óinnsigluð kauptilboð. Til að fá upplýsingar um hvernig á að stofna báðar gerðir tilboðsbeiðna skal skoða [Stofna beiðni um tilboð](tasks/create-request-quotation.md). Í þessum hluta er lögð áhersla á nokkur mikilvæg atriði þegar tilboðsbeiðni er stofnuð fyrir innsiglað kauptilboð.

Tilboðsbeiðnir fyrir innsigluð kauptilboð verða að vera með gildið **Gerð kauptilboðs** sem *Innsiglað*. Það eru þrjár leiðir til að úthluta þessu gildi til tilboðsbeiðni-máls:

- Stilltu gildið í tilboðsbeiðninni eftir að þú stofnar hana.
- Skilgreindu innsiglað kauptilboð sem sjálfgefna kauptilboðsgerð fyrir allar tilboðsbeiðnir í færibreytum innkaupa og aðfanga. (Sjá kaflann [Setja sjálfgefna tilboðsgerð](#set-default-bid-type) fyrr í þessum kafla.)
- Þegar þú stofnar nýja tilboðsbeiðni skaltu velja beiðnigerðina sem er sett upp fyrir innsigluð kauptilboð. (Sjá hlutann [Stilla sjálfgefna gerð kauptilboðs](#set-default-bid-type).)

Fyrir innsiglað tilboð er það gildið **Lokadagur og -tími** sem sker úr um hvenær opna má innsend tilboð. Gildið **Lokadagur og -tími** í hverri línu mun passa við gildið í hausnum.

Ekki er hægt að breyta tilboðsgerð eftir að RFQ tilboðsbeiðni er send.

### <a name="vendors-respond-to-an-rfq"></a>Svör fyrirspurna lánardrottna um verð

Lánardrottnar sem svara innsigluðu kauptilboði nota sömu aðferð og eir nota til að svara opnum tilboðum eins er útskýrt í [Vinna með beiðnir um tilboð á vinnusvæði fyrir lánardrottnatilboð](vendor-collaboration-work-customers-dynamics-365-operations.md#working-with-rfqs-in-the-vendor-bidding-workspace). Fyrir ítarlegar upplýsingar um hvernig á að vinna með bæði opin tilboð og innsigluð tilboð skal skoða [Færa inn og bera saman tilboð vegna tilboðsbeiðna og gera samninga](tasks/enter-compare-rfq-bids-award-contracts.md). Eini munurinn á afgreiðslu innsiglaðra tilboða og opinna tilboða er að starfsmenn innkaupa geta ekki opnað innsiglað tilboð lánardrottins fyrr en tilboðstímabilinu lýkur. Aðeins tengiliður lánardrottisins getur opnað innsiglað tilboð lánardrottisins.

> [!IMPORTANT]
> Fyrir innsiglað tilboð geta lánardrottnar aðeins hlaðið upp viðhengjum á PDF-sniði. Engin önnur snið verða samþykkt.

Eftir að skráður notandi lánardrottins velur **Tilboð** í tilboðsbeiðni innsiglaðs tilboðs getur hann slegið inn gögn um tilboðið og þeim gögnum verður haldið öruggum. Lánardrottnar geta vistað verkin sín þegar þeir undirbúa tilboð, skilað þeim eins oft og þörf er á og sent þau svo inn þegar þau eru tilbúin. Söluaðilar geta einnig skoðað tilboð sitt eftir að þeir leggja það fram. Ef lánardrottnar þurfa að breyta tilboði sínu eftir að þeir leggja það fram geta þeir kallað það til baka, uppfært það og sent það inn aftur hvenær sem er þar til tilboðstímabilið rennur út.

Eftirfarandi skilyrði gilda á meðan á innsigluðu útboði stendur:

- Í innsigluðu kauptilboðsferli býr kerfið til færslubók fyrir *Tilboðsbeiðnir*.
- Þegar lánardrottinn sendir inn tilboð eru færslubækur tilboðsbeiðni án lína með innsigluðu verði stofnaðar.
- Eftir að málið er opnað eru færslubækur tilboðsbeiðna með verði og upphæð stofnaðar. Hægt er að komast í þessa færslubók með því að velja **Færslubækur beiðna um tilboð** á síðunni **Allar beiðnir um tilboð**.
- Kerfið geymir kladda yfir hverja aðgerð sem notendur framkvæma á innsigluðu kauptilboði. Þessar aðgerðir fela í sér að skoða, breyta og vista tilboðið. Þessi skrá er sýnileg bæði lánardrottni og sérfræðingum sem hefur aðgang að tilboðinu.
- Eftir því sem líður á tilboðið geta sérfræðingar skoðað stöðu þess. Staðan verður annaðhvort *Lánardrottinn er að uppfæra* eða *Sent af lánardrottni*.
- Staða lína í lokuðu tilboði verður áfram *Send* þar til tilboðið er opnað.
- Ef lánardrottinn velur að hafna tilboði mun tilboðið fá stöðuna **Framvinda svara** sem *Hafnað af lánardrottni*. Þessi staða verður sýnileg starfsfólki verkkaupa.
- Svör í spurningalistum eru **ekki** geymd á dulkóðuðu formi í gagnagrunninum. Þau eru þar af leiðandi ekki innsigluð. Þau verða hinsvegar ekki sýnileg í notandaviðmóti tilboðsbeiðni fyrr en málið er opnað.

### <a name="all-sealed-bid-activities-are-logged"></a>Allar lokaðar tilboðsaðgerðir eru skráðar

Ítarlegur annáll skráir allar athafnir og aðgerðir notenda fyrir tilboð. Virkniskráin gerir fyrirtækjum kleift að ákvarða hver uppfærði tilboð á líftíma þess og hverjar uppfærslurnar voru. Það gerir stofnunum einnig kleift að staðfesta að aðeins þeir sem hafa heimild til þess hafi fengið aðgang að innsigluðu boði. Aðgerðakladdinn er tiltækur á öllum **Aðgerðasíðum** tilboðsins.

### <a name="review-rfq-activity"></a>Yfirfara aðgerðir tilboðsbeiðni

Öll samskipti með tilboðið eru skráð og hægt að skoða á síðunni **Aðgerðir**. Eftirfarandi skýringarmynd sýnir dæmi.

![Dæmi um aðgerðarsíðuna](media/sealed-bidding-rfq-activity.png "Dæmi um aðgerðarsíðuna")

Lánardrottnar geta fengið aðgang að síðunni **Aðgerðir** með því að velja **Aðgerðir** á síðunni **Innsiglað kauptilboð tilboðsbeiðni**. Starfsfólk innkaupa geta fengið aðgang að henni með því að velja **Aðgerðir** á síðunni **Tilboðsbeiðnir**. Aðgerðakladdinn býður upp á fullan sýnileika fyrir lánardrottna og fyrir starfsfólk innkaupa sem hafa aðgang að tilboðinu. Þar af leiðandi getur hann gefið upplýsingar um óheimilan aðgang.

### <a name="unseal-sealed-bids"></a>Opna innsigluð tilboð

Þegar gildið **Lokadagur og -tími** sem var skilgreint fyrir tilboðsbeiðni innsiglaðs tilboðs rennur út verður hnappurinn **Opna** tiltækur. Veldu **Opna** til að opna öll tilboð fyrir valið mál tilboðsbeiðni. Þá verða öll tilboðsgögn og fylgigögn sýnileg svo hægt sé að hafa umsjón með svörum við málinu. Auk þess eru stofnaðar færslubækur sem innihalda innsend tilboðsgögn.

Tilvik opnunar er skráð og er hægt að skoða á síðunni **Aðgerðir**.

### <a name="process-accepted-bids"></a>Vinna úr samþykktum tilboðum

Ferlið við að bera saman og samþykkja áður innsigluð tilboð er það sama og ferlið fyrir opin tilboð. Upplýsingar um hvernig á að skora, bera saman, hafna og samþykkja óinnsigluð tilboð er að finna í [Færa inn og bera saman tilboð vegna tilboðsbeiðna og gera samninga](tasks/enter-compare-rfq-bids-award-contracts.md).

## <a name="the-rfq-activity-log-can-never-be-deleted"></a>Aldrei er hægt að eyða RFQ aðgerðakladdanum

Enginn, ekki einu sinni stjórnendur og notendaþjónusta Microsoft, getur breytt eða eytt virkniskránni fyrir tilboðsbeiðni. Þessi takmörkun hjálpar til við að tryggja sanngirni við innsiglaða tilboðsferlið. Það hjálpar einnig til við að tryggja að nákvæmri færsluslóð sé viðhaldið.
