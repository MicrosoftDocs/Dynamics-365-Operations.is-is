---
title: Búa til og skilgreina framlengdar ábyrgðir
description: Þessi grein fjallar um auknar ábyrgðir og lýsir því hvernig á að búa til og stilla þær í Microsoft Dynamics 365 Commerce.
author: sijoshi
ms.date: 06/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: sijoshi
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9ed9851a9609e8a87ae0ffadc5cdd20c03fa17ee
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886985"
---
# <a name="create-and-configure-extended-warranties"></a>Búa til og skilgreina framlengdar ábyrgðir

[!include [banner](includes/banner.md)]

Þessi grein fjallar um auknar ábyrgðir og lýsir því hvernig á að búa til og stilla þær í Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Yfirlit

Viðskiptavinir velja í auknu mæli aukinn stuðning og þjónustu þegar þeir kaupa vörur, sérstaklega neytendavörur sem seldar eru á góðu verði, t.d. símar og tölvur. Með því að bjóða upp á aukna ábyrgð á kaupum geta söluaðilar hjálpað til við að byggja upp viðskiptavild kaupenda. Auknar ábyrgðir láta viðskiptavini vita hvar þjónustu og stuðning er að finna. Þeir geta því verið vissir um að tekið verði á vandamálum þeirra.

Hægt er að selja viðskiptavinum auknar ábyrgðir í smásölurás við upphafleg kaup afurðar. Einnig er hægt að selja þær í takmarkaðan tíma eftir upphaflegu kaupin.

### <a name="warranty-item-setup"></a>Uppsetning vöruábyrgðar

Dynamics 365 Commerce býður upp á virkni sem gerir þér kleift að búa til vöruábyrgð og stilla eigindir fyrir hana. Þessar eigindir fela í sér tengslin milli afurðar og vöruábyrgðar, verð ábyrgðar og tímalengd ábyrgðar. Þegar búið er að skilgreina og gefa út vöruábyrgð til fyrirtækiseiningu, getur söluaðili selt ábyrgðir í gegnum nútíma sölustað (MPOS), netverslanir og aðrar smásölurásir.

### <a name="warranty-item-sales"></a>Sala vöruábyrgðar

Auknar ábyrgðir eru seldar í smásölurás við upphafleg kaup afurðar. Einnig er hægt að selja þær í takmarkaðan tíma eftir upphaflegu kaupin.

Á sölustað eru sölufulltrúar beðnir um að bæta við aukna ábyrgð þegar tengdri afurð er bætt við körfu viðskiptavinar. Möguleikar á söluauka og krosssölu eru þar af leiðandi kynntir sölufulltrúum sem hluti af söluflæðinu.

Viðskiptavinir geta einnig snúið aftur seinna og keypt aukna ábyrgð á afurð sem þeir keyptu áður. Í slíkum tilfellum getur sölufulltrúi flett upp á upprunalegri færslu og selt viðskiptavinum viðeigandi aukna vöruábyrgð.

### <a name="warranty-terminology"></a>Hugtök ábyrgðar

Eftirfarandi tafla skilgreinir nokkur ábyrgðartengd hugtök.

| Hugtak | lýsing |
|------------------------------|--------------|
| Aukin ábyrgð/ábyrgð | *Aukin ábyrgð* vísar til þjónustusamnings eða samkomulag sem veitir viðskiptavinum lengri ábyrgð. Aukna ábyrgðin felur í sér viðbótarþjónustu við að skipta um eða gera við vörur á meðan tryggingatími framlengdrar ábyrgðar stendur yfir. |
| Ábyrgð framleiðanda | *Ábyrgð framleiðanda* (oft kölluð *takmörkuð ábyrgð*) er ábyrgðin sem viðskiptavinir fá þegar þeir kaupa afurð. Hér eru nokkrir þættir í ábyrgð framleiðanda:<ul><li>Ábyrgðarkostnaður er innifalinn í kostnaði afurðar. Viðskiptavinir þurfa ekki að greiða viðbótarupphæð fyrir ábyrgð framleiðanda.</li><li>Það fer eftir vöruflokki, en ábyrgð framleiðanda varir yfirleitt í 30 daga, sex mánuði eða eitt ár. (Fyrir flest raftæki gildir ábyrgðin í eitt ár).</li><li>Ábyrgðin nær til galla sem orsakast af vélar- eða rafmagnsbilun. Tryggingin er takmörkuð og hún felur ekki í sér óvæntar skemmdir á keyptri afurð. Viðskiptavinir sem vilja verja afurðirnar sem þeir kaupa frá hvers konar tjóni ættu að fjárfesta í aukinni ábyrgð. Aukin ábyrgð stendur yfir í tvö til tíu ár, fer allt eftir vöruflokki. Þær eru einnig með víðtækari tryggingu og ná yfir hversdagsleg óhöpp eins og að missa á gólfið, hella yfir og bletti.</li></ul> |
| Ábyrgðarvara | *Vöruábyrgð* er aukin vöruábyrgð sem er seld fyrir ábyrgðarhæfa vöru. Dæmi er tveggja ára slysatrygging fyrir fartölvur. |
| Ábyrgðarhæf vara | *Ábyrgðarhæf vara* er afurð með raðnúmeri sem ábyrgð er seld fyrir. Til dæmis er fartölva ábyrgðarhæf vara sem tveggja ára og þriggja ára auknar ábyrgðir eru seldar fyrir. |
| Ábyrgðarhópur | *Ábyrgðarflokkur* er tengsl milli vöruábyrgða og ábyrgðarhæfra vara. Sölustaður notar ábyrgðarflokka til að ákveða hvaða vöruábyrgðir sölufulltrúar eiga að leggja til að bætt verði við þegar ábyrgðarhæfri vöru er bætt við körfu viðskiptavinar. |
| Regla ábyrgðar | *Stefna ábyrgðar* er eining sem búin er til í Commerce þegar ábyrgðarstefna er seld. Ábyrgðarstefna inniheldur upplýsingar eins og upphafs- og lokadagsetningar keyptrar vöruábyrgðar, skilmálar og raðnúmer á afurð sem er afurð með ábyrgð. Hægt er að deila númerum ábyrgðarstefnu með viðskiptavinum þannig að þeir séu með tilvísun fyrir vöru með aukna ábyrgð sem þeir keyptu. |

## <a name="create-a-warranty-item"></a>Búa til vöruábyrgð

Til að búa til vöruábyrgð í Commerce skal fylgja þessum skrefum.

1. Fara skal í **Smásala og viðskipti \> Afurðir og tegundir \> Afurðir**.
1. Veljið **Ný** til að búa til vöruábyrgð.
1. Í glugganum **Ný afurð**, í reitnum **Gerð afurðar**, skal velja **Þjónusta**.
1. Í reitnum **undirgerð afurðar** skal velja **Afurð**.
1. Í reitnum **Þjónustugerð afurðar** skal velja **Þjónusta**.
1. Í reitinn **Heiti afurðar** skal slá inn heiti afurðar.
1. Í reitnum **Tegund smásölu** skal velja gildi í fellilistaglugganum og síðan velja **Í lagi**.
1. Í **Afurðarnúmer** skal slá inn númer afurðar.
1. Veljið **Í lagi**.
1. Á síðunni **Upplýsingar um afurð**, í flýtiflipanum **Ábyrgð**, skal stilla reitina **Tímaeining** og **Tímalengd**.

    | Svæðisheiti | Virði | lýsing |
    |------------|-------|-------------|
    | Tímaeining | **Dagur/dagar**, **Vika/vikur**, **Mánuður/mánuðir** eða **Ár** | Þessi reitur tilgreinir tímaeininguna sem notuð er við ábyrgðina. |
    | Tímalengd | Jákvætt heiltölugildi | Þessi reitur tilgreinir tímalengd ábyrgðar í valdri tímaeiningu. |

    Fyrir tveggja ára ábyrgð skal til dæmis stilla reitinn **Tímaeining** á **Ár** og reitinn **Tímalengd** á **2**. Einnig er hægt að stilla reitinn **Tímaeining** á **Mánuður/mánuðir** og reitinn **Tímalengd** á **24** eins og sýnt er á eftirfarandi skýringarmynd.

    ![Upplýsingasíða afurðar fyrir vöruábyrgð.](./media/ew-time-properties.png)

1. Veljið **Vista** til að vista vöruábyrgðina.
1. Losa afurð með ábyrgð til fyrirtækisins svo að hægt sé að selja hana. Frekari upplýsingar er að finna í [Setja upp smásöluafurðir](set-up-retail-products.md).
1. Á síðunni **Upplýsingasíða um losaðar afurðir**, í flýtiflipanum **Ábyrgð**, skal stilla reitina **Grunnur verðbils**, **Lægri mörk** og **Efri mörk**.

    | Svæðisheiti | Virði | lýsing |
    |------------|-------|-------------|
    | Grunnur verðbils | **Ekkert**, **Grunnverð** eða **Söluverð** | <ul><li>**Ekkert** - Gildin **Lægri mörk** og **Efri mörk** fyrir verðbil eiga ekki við.</li><li>**Grunnverð** - Uppgefin ábyrgð verður tiltæk ef grunnverð (þ.e. verðið án afsláttar) ábyrgðarhæfrar vörur er á milli gildanna **Lægri mörk** og **Efri mörk** sem eru sýnd hér, byggt á verði ábyrgðarhæfu vörunnar.</li><li>**Söluverð** - Þetta gildi er tekið frá fyrir seinni tíma notkun.</li></ul> |
    | Neðri mörk, efri mörk | Jákvætt heiltölugildi | Þessir reitir skilgreina efri og neðri mörk verðs á ábyrgðarhæfri vöru og hvernig núverandi vöruábyrgð á við ábyrgðarhæfu vöruna. Þessi mörk geta byggst á grunnverði ábyrgðarhæfrar vöru (einnig þekkt sem ráðlagt smásöluverð framleiðanda \[MSRP\]). Ef reiturinn **Grunnur verðbils** er stilltur á **Grunnverð** mun aðeins ábyrgðarhæf vara (afurð) sem er með grunnverð á milli gildanna **Neðri mörk** og **Efri mörk** kveikja á beiðni um að bæta við vöruábyrgð á sölustað. |

    Eftirfarandi skýringarmynd sýnir til dæmis að reiturinn **Grunnur verðbils** er stilltur á **Grunnverð**, reiturinn **Lægri mörk** er stilltur á $500 og reiturinn **Efri mörk** er stilltur á $1000.
    
    ![Upplýsingasíða um losaðar afurðir fyrir vöruábyrgð.](./media/ew-release-product-details.png)

1. Komið vöruábyrgðinni fyrir í rásinni þar sem hún verður seld. Frekari upplýsingar er að finna í [Setja upp vöruúrval](set-up-assortments.md).

### <a name="example"></a>Dæmi

Ábyrgðarhæf fartölva er með grunnverð $999 og til eru tvær vöruábyrgðir fyrir fartölvu:

- Ábyrgð\_1 er með lægri mörkin $500 og efri mörkin $1000 og reiturinn **Grunnur verðbils** er stilltur á **Grunnverð**.
- Ábyrgð\_2 er með lægri mörkin $1001 og efri mörkin $2000 og reiturinn **Grunnur verðbils** er stilltur á **Grunnverð**.

Í þessu tilfelli, þegar ábyrgðarhæfu fartölvunni er bætt við körfu viðskiptavinar, birtist kvaðning á sölustað um að bæta við Ábyrgð\_1 vegna þess að verð fartölvunnar er á milli neðri og efri marka fyrir Ábyrgð\_1.

> [!NOTE]
> Fyrir þetta dæmi, ef þú vilt að kvaðningar verði sýndar fyrir bæði Ábyrgð\_1 og Ábyrgð\_2, óháð verðsins á ábyrgðarhæfu vörunni, skal stilla reitinn **Grunnur verðbils** á **Enginn**.

## <a name="configure-channel-specific-settings"></a>Skilgreina stillingar sem tengjast rásum

Stillingar sem tengjast rásum gera þér kleift að tilgreina hvort eigi að sýna kvaðningu um að bæta við vöruábyrgð á sölustaðnum þegar ábyrgðarhæfri vöru er bætt við körfu viðskiptavinar.

Til að skilgreina stillingar sem tengjast rásum í Commerce skal fylgja þessum skrefum.

1. Fara skal í **Smásala og viðskipti \> Afurðir og flokkar \> Ábyrgð \> Ábyrgðarstillingar**.
1. Í flipanum **Tengt rás**, í dálknum **Biðja um ábyrgð** fyrir rásina þína, skal fylgja einu af þessum skrefum:

    - Veljið gátreitinn ef beðið er um vöruábyrgðina á sölustaðnum þegar ábyrgðarhæfri vöru er bætt við körfuna.
    - Hreinsið gátreitinn ef ekki er beðið um vöruábyrgðina á sölustaðnum þegar ábyrgðarhæfri vöru er bætt við körfuna.

1. Keyrið verkið **1070** til að samstilla gögnin við rásina.

## <a name="configure-a-number-sequence-for-warranty-policies"></a>Skilgreina númeraröð fyrir ábyrgðarstefnur

Hver ábyrgðarstefna er auðkennd með númeri ábyrgðarstefnu sem er búið til með númeraröð. Nánari upplýsingar um númeraraðir er að finna í [Yfirlit númeraraða](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md).

Til að skilgreina númeraröð fyrir ábyrgðarstefnur í Commerce skal fylgja þessum skrefum.

1. Fara skal í **Smásala og viðskipti \> Afurðir og flokkar \> Ábyrgð \> Ábyrgðarstillingar**.
1. Í flipanum **Númeraraðir**, í línunni fyrir tilvísunina **Ábyrgðarstefna**, skal slá inn eða velja gildi í reitnum **Númeraraðarkóði**.

## <a name="set-up-a-warranty-group"></a>Setja upp ábyrgðarflokk

Ábyrgðarflokkur er tengsl milli vöruábyrgða og ábyrgðarhæfra vara. Sölustaður notar ábyrgðarflokka til að ákveða hvaða vöruábyrgðir sölufulltrúar eiga að leggja til að bætt verði við þegar ábyrgðarhæfri vöru er bætt við körfu viðskiptavinar.

Til að setja upp ábyrgðarflokk í Commerce skal fylgja þessum skrefum.

1. Fara skal í **Smásala og viðskipti \> Afurðir og flokkar \> Ábyrgð \> Ábyrgðarflokkar**.
1. Veljið **Nýr** til að búa til ábyrgðarflokk.
1. Í **Heiti** reitinn, slá inn heiti fyrir nýjan hóp.
1. Í flipanum **Almennt**, í reitnum **Lýsing**, skal slá inn lýsingu á flokknum.
1. Í flýtiflipanum **Ábyrgðarvörur** skal velja **Bæta við línu** til að bæta við vöruábyrgð.
1. Í reitinn **Röð birtingar** skal slá inn númer til að raða upp ábyrgðarflokknum á sölustað. Sölustaðurinn mun sýna vöruábyrgðir í hækkandi röð þar sem beðið er um ábyrgð.
1. Í flýtiflipanum **Ábyrgðarhæfar afurðir** skal velja **Bæta við línu** til að bæta við ábyrgðarhæfum afurðum.
1. Ef ábyrgðarvaran á við um allan flokkinn yfir ábyrgðarhæfar vörur (afurðir), skal velja flokkinn í reitnum **Flokkur**. Ef ábyrgðarvaran á við um tiltekna ábyrgðarhæfa vöru (afurð), skal velja afurðina í reitnum **Afurð**.
1. Í flýtiflipanum **Tiltækar rásir** skal velja **Bæta við línu** til að bæta við rásinni þar sem á að selja ábyrgðarvöruna.
1. Veljið **Vista** til að vista stillinguna.
1. Veljið **Gefa út** til að gefa út ábyrgðarflokkinn.
1. Keyrið verkið **1040** til að samstilla gögnin við rás.

## <a name="sell-warranty-items-at-the-pos"></a>Selja ábyrgðarvörur á sölustað

Tvær aðgerðir sölustaðar gera sölufulltrúum kleift að selja ábyrgðarvörur í verkflæði fyrir kaup viðskiptavinar:

- **Bæta við ábyrgð** - Þessi aðgerð kveikir á kvaðningu um að sýna tiltækar ábyrgðir fyrir ábyrgðarhæfa vöru sem valin er í körfunni.
- **Bæta ábyrgð við fyrirliggjandi færslu** - Þessi aðgerð gerir sölufulltrúum kleift að selja ábyrgðir fyrir ábyrgðarhæfar vörur sem voru áður seldar. Sölufulltrúar geta fundið upprunalegu færsluna fyrir ábyrgðarhæfa vörur með því að slá inn kvittananúmer færslunnar.

Eftirfarandi skýringarmynd sýnir dæmi um síðu afgreiðslukassa þar sem beðið er um að bæta við vöruábyrgð fyrir núverandi kaup á ábyrgðarhæfri vöru.

![Dæmi um kvaðningu um að bæta við vöruábyrgð fyrir núverandi kaup.](./media/ew-sell-warranty.png)

Eftirfarandi skýringarmynd sýnir dæmi um eiginleikann að bæta við vöruábyrgð fyrir ábyrgðarhæfa vöru sem var áður seld.

![Dæmi um eiginleikann að bæta við vöruábyrgð fyrir áður selda ábyrgðarhæfa vöru.](./media/ew-add-warranty-existing.png)

## <a name="process-warranty-transactions"></a>Vinna úr ábyrgðarfærslum

Þegar ábyrgðir eru seldar í staðgreiðslufærslum, eftir að færslurnar eru bókaðar í Commerce Headquarters, geta notendur Commerce keyrt verkið **Vinna úr ábyrgðarfærslum** til að vinna úr ábyrgðarfærslunum og búa til ábyrgðarstefnur.

Til að vinna úr ábyrgðarfærslum í Commerce Headquarters skal fylgja þessum skrefum.

1. Fara skal í **Smásala og viðskipti \> Afurðir og flokkar \> Ábyrgð \> Vinna úr ábyrgðarfærslum**.
1. Í glugganum **Veljið fyrirtækjahnúta**, í reitnum **Stigveldi fyrirtækis**, skal velja gildi.
1. Í listanum **Tiltækir fyrirtækjahnútar** skal velja annaðhvort ákveðna verslun eða, ef á að búa til runuvinnslu fyrir hóp af verslunum, hnút.
1. Veljið hægri örvarhnappinn til að bæta valinu þínu við listann **Valdir fyrirtækishnútar**.
1. Veljið flipann **Keyra í bakgrunni**.
1. Stillið valkostinn **Runuvinnsla** á **Já** og veljið síðan **Endurtekning**.
1. Í glugganum **Skilgreina endurtekningu**, í reitnum **Upphafsdagsetning**, skal velja eða slá inn upphafsdag fyrir endurtekninguna.
1. Í reitnum **Upphafstími** skal velja eða slá inn upphafstíma fyrir endurtekninguna.
1. Fylgið einu af eftirfarandi skrefum:

    - Veljið valkostinn **Engin lokadagsetning** ef endurtekningin á ekki að enda.
    - Veljið valkostinn **Enda eftir** ef endurtekningin á að enda eftir tiltekinn keyrslufjölda. Ef þessi valkostur er valinn skal slá inn keyrslufjöldann.
    - Veljið valkostinn **Enda á** ef endurtekningin á að enda á tiltekinni dagsetningu. Ef þessi valkostur er valinn skal velja eða slá inn dagsetninguna.

1. Veljið **Í lagi**.
1. Veljið **Í lagi**.

## <a name="warranty-policies"></a>Ábyrgðarstefnur

Þegar aukin ábyrgð er seld verður eining ábyrgðarstefnu sjálfkrafa búin til. Hægt er að deila númerum ábyrgðarstefnu með viðskiptavinum þannig að þeir séu með tilvísun fyrir vöru með ábyrgð sem þeir keyptu. Eiginleikar ábyrgðarstefnanna fela í sér virka upphafsdagsetningu og lokadagsetningu ábyrgðarinnar, skilmála og raðnúmer ábyrgðarhæfrar vöru sem ábyrgðin var seld fyrir.

> [!NOTE]
> Eiginleikar ábyrgðarstefnunnar verða sjálfkrafa myndaðar þegar einingar ábyrgðarstefnu eru búnar til. Sem stendur er ekki hægt að skilgreina þá eða breyta þeim.

Eftirfarandi tafla lýsir eiginleikum ábyrgðarstefnunnar og gildum þeirra. Í Commerce Headquarters kallast gagnagrunnstaflan WARRANTYPOLICY.

| Nafn eiginleika | Virði | lýsing |
|---------------|-------|-------------|
| PolicyNumber | Stafastrengur (hámark 20 stafir) | Númer ábyrgðarstefnunnar |
| WarrantiedItemId | Stafastrengur (hámark 20 stafir) | Auðkenni ábyrgðarhæfrar vöru |
| WarrantiedInventoryLotId | Stafastrengur (hámark 20 stafir) | Lotukenni birgða fyrir ábyrgðarhæfa vöru |
| WarrantiedSerialNumber | Stafastrengur (hámark 20 stafir) | Raðnúmer ábyrgðarhæfrar vöru |
| WarrantiedFulfilledDate | Dagsetning | Uppfyllingardagur ábyrgðarhæfrar vöru |
| WarrantyItemId | Stafastrengur (hámark 20 stafir) | Auðkenni vöru með ábyrgð |
| WarrantyInventoryLotId | Stafastrengur (hámark 20 stafir) | Lotukenni birgða fyrir vöru með ábyrgð |
| WarrantySalesDate | Dagsetning | Söludagur vöru með ábyrgð |
| WarrantyEffectiveDate | Dagsetning | Gildisdagsetning ábyrgðarstefnunnar |
| WarrantyExpirationDate | Dagsetning | Lokadagsetning ábyrgðarstefnunnar |
| CustAccount | Stafastrengur (hámark 20 stafir) | Lykilnúmer viðskiptavinar |
| Staða | **Búið til**, **Ógilt**, **Virkt** eða **Útrunnið** | Staða ábyrgðarstefnunnar |
| Athugasemdir | Stafastrengur (að hámarki 255 stafir) | Athugasemdir um ábyrgðarstefnuna, t.d. skilmálar |

## <a name="frequently-asked-questions-faq"></a>Algengar spurningar

**Af hverju sé ég ekki ábyrgðarkvaðningu á sölustað?**

Gakktu úr skugga um að vöruábyrgðinni hafi verið komið fyrir í rásinni. Gakktu einnig úr skugga um að ábyrgðarflokkurinn sé stilltur þannig að hann innihaldi viðkomandi rás.

**Þegar ég reyni að bæta ábyrgð við núverandi færslu og slá inn kvittananúmer viðskiptavinapöntunar, af hverju sé ég ekki neinar færslulínur fyrir vörur?**

Aðeins er hægt að finna kvittanir ef sækja-verk er keyrt til að hlaða upp kvittunum í Commerce Headquarters. Til að keyra sækja-verk skal fara í **Smásala og viðskipti \> Upplýsingatækni smásölu og viðskipta \> Dreifingaráætlun**, velja verkið **P-0001** og síðan velja **Keyra núna**.

**Hvers vegna er eiginleikinn fyrir ábyrgð aðeins í boði fyrir raðaðar afurðir?**

Ábyrgð er þjónusta sem er veitt fyrir ákveðna, einkvæma afurð. Í Dynamics 365 er aðeins hægt að bera kennsl á afurð með raðnúmeri.

## <a name="additional-resources"></a>Frekari upplýsingar

[Setja upp smásöluafurðir](set-up-retail-products.md)

[Setja upp úrval](set-up-assortments.md)

[Yfirlit númeraraða](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]