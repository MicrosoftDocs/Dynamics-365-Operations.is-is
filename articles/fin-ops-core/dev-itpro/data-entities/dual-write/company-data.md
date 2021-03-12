---
title: Fyrirtækishugtak í Dataverse
description: Þetta efni lýsir samþættingu fyrirtækjaupplýsinga milli Finance and Operations og Dataverse.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: bbe634b87b3cb30ed993f9b3afeb4321d70f07e6
ms.sourcegitcommit: 7e1be696894731e1c58074d9b5e9c5b3acf7e52a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/17/2020
ms.locfileid: "4744880"
---
# <a name="company-concept-in-dataverse"></a>Fyrirtækishugtak í Dataverse

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]


Í Finance and Operations er hugtakið a *fyrirtæki* bæði lögleg smíð og viðskiptasmíð. Það er einnig öryggis- og sýnileikamörk fyrir gögn. Notendur vinna alltaf í samhengi við eitt fyrirtæki og flest gögnin eru röndótt af fyrirtækinu.

Dataverse er ekki með sambærilegt hugtak. Næsta hugtakið er *rekstrareining*, sem er fyrst og fremst öryggis- og sýnileikamörk fyrir notendagögn. Þetta hugtak hefur ekki sömu lagalegu eða viðskiptalegu afleiðingar og hugtakið fyrirtæki.

Vegna þess að rekstrareining og fyrirtæki eru ekki sambærileg hugtök er ekki mögulegt að þvinga kortlagningu á milli þeirra (1: 1) í þeim tilgangi að samþætta Dataverse. Hins vegar, vegna þess að notendur verða að sjá sömu línur í forritinu og Dataverse, hefur Microsoft kynnt til leiks nýja töflu í Dataverse sem nefnist cdm\_Fyrirtæki. Þessi tafla jafngildir fyrirtækjatöflunni í forritinu. Til að tryggja að sömu línur sjáist í forriti og nýju Dataverse er mælt með eftirfarandi uppsetningu gagna í Dataverse:

+ Fyrir hverja Finance and Operations -fyrirtækislínu sem er virk fyrir tvöfalda skráningu er tengd cdm\_fyrirtækjalína búin til.
+ Þegar cdm\_fyrirtækislína er búin til og virkjuð fyrir tvöfalda skráningu er sjálfgefin viðskiptaeining stofnuð með sama heiti. Þó að sjálfgefið teymi sé sjálfkrafa búið til fyrir þá rekstrareiningu er rekstrareiningin ekki notuð.
+ Sérstakt eigendateymi er búið til sem hefur sama nafn. Það er líka tengt rekstrareiningunni.
+ Sjálfgefið er að eigandi allra lína sem eru búnar til og tvöfalt skráðar á Dataverse sé stilltur á hópinn „DW-eigandi“ sem er tengdur við tengda viðskiptaeiningu.

Eftirfarandi skýringarmynd sýnir dæmi um þessa gagnauppsetningu í Dataverse.

![Uppsetning gagna í Dataverse](media/dual-write-company-1.png)

Í þessari grunnstillingu eru færslur sem tengjast USMF fyrirtækinu í eigu teymis sem tengist USMF rekstrareiningunni í Dataverse. Því geta notendur sem hafa aðgang að viðskiptaeiningunni í gegnum öryggishlutverk sem er stillt á sýnileika viðskiptaeiningarstigs nú séð línurnar. Eftirfarandi dæmi sýnir hvernig hægt er að nota teymi til að veita réttan aðgang að þessum línum.

+ Hlutverkinu „Sölustjóri“ er úthlutað til meðlima „USMF sölu“ teymisins.
+ Notendur sem eru með hlutverkið „sölustjóri“ hafa aðgang að öllum lyklalínum sem eru hluti af sömu viðskiptaeiningu og notendurnir eru meðlimir í.
+ "USMF Sales" teymið er tengt við USMF viðskiptadeildina sem áður var nefnd.
+ Þess vegna geta meðlimir í "USMF sölu" teyminu séð hvaða reikning sem er í eigu "USMF DW" notandans, sem hefði komið frá USMF fyrirtækjatöflunni í Finance and Operations.

![Hvernig hægt er að nota teymi](media/dual-write-company-2.png)

Eins og myndin hér að ofan sýnir er þessi 1:1 kortlagning milli rekstrareiningar, fyrirtækis og teymis aðeins upphafspunktur. Í þessu dæmi er ný „eining“ í Evrópu búin til handvirkt í Dataverse sem yfireining bæði fyrir DEMF og ESMF. Þessi nýja rótarviðskiptaeining er ekki skyld tvöföldum skrifum. Hins vegar er hægt að nota hana til að veita meðlimum „EUR Sales“ teymisins aðgang að reikningsgögnum bæði í DEMF og ESMF með því að stilla sýnileika gagna á **Yfir-/undir-BU** í tilheyrandi öryggishlutverki.

Lokaumfjöllunarefnið er hvernig tvöföld skráning ákvarðar hvaða eigendahóp hún á að úthluta línum á. Hegðuninni er stjórnað af töflunni **Sjálfgefið eigendateymi** í cdm\_Fyrirtæki línunni. Þegar cdm\_fyrirtækjalína er virkjuð fyrir tvískrif býr viðbót sjálfkrafa til tengda viðskiptaeiningu og eigendateymi (ef það er ekki þegar til) og stillum dálkinn **Sjálfgefið eigendateymi**. Stjórnandi getur breytt þessum dálki í annað gildi. Stjórnandi getur þó ekki hreinsað dálkinn svo framarlega sem taflan er virk fyrir tvöfalda skráningu.

> [!div class="mx-imgBorder"]
![Sjálfgefinn dálkur eigendahóps](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>Fyrirtækjaskrár og ræsibönd

Dataverse-samþætting færir fyrirtækjajöfnun með því að nota auðkenni fyrirtækisins til að randa gögn. Eins og eftirfarandi mynd sýnir eru allar fyrirtækistöflur útvíkkaðar þannig til að þær séu með margt-í-eitt (N:1) vensl við töfluna cdm\_Fyrirtæki.

> [!div class="mx-imgBorder"]
![N:1 vensl milli fyrirtækjasértakrar töflunnar og töflunnar cdm_Company](media/dual-write-bootstrapping.png)

+ Gildi lína verður skrifvarið eftir að fyrirtæki hefur verið bætt við og það vistað. Þess vegna ættu notendur að gæta þess að þeir velja rétt fyrirtæki.
+ Aðeins línur sem eru með fyrirtækisgögn eru hæfar fyrir tvöfalda skráningu milli forrits og Dataverse.
+ Fyrir núverandi gögn Dataverse mun stjórnandaleidd ræsibandareynsla brátt verða tiltæk.


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a>Heiti fyrirtækis sem er sjálfkrafa fyllt út í forritum fyrir viðskiptavini

Ýmsar leiðir eru til að fylla út sjálfkrafa Fyrirtækisheitið í forritum fyrir viðskiptavini.

+ Ef notandi er kerfisstjóri er hægt að stilla sjálfgefið fyrirtæki með því að fara í **Ítarlegar stillingar > Kerfi > Öryggi > notendur**. Opnaðu skjámyndina **Notandi** og í **Upplýsingar um stofnun/fyrirtæki** hlutanum skaltu stilla gildið **Fyrirtækið á sjálfgefin á skjámyndum**.

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="Velja sjálfgefið fyrirtæki í upplýsingahluta fyrirtækis.":::

+ Ef þú hefur **skrifheimild** fyrir **SystemUser** töfluna fyrir stig **Viðskiptaeiningar**, getur þú breytt sjálfgefna fyrirtækinu í hvaða skjámynd sem er með því að velja fyrirtæki úr fellivalmynd **Fyrirtækis**.

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="Breyta heiti fyrirtækisins á nýjum lykli.":::

+ Ef þú hefur **Skrifheimild** fyrir gögn í fleiri en einu fyrirtæki, geturðu breytt sjálfgefna fyrirtækinu með því að velja línu sem tilheyrir öðru fyrirtæki.

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="Að velja línu breytir sjálfgefna fyrirtækinu.":::

+ Ef þú sérð um kerfisstillingar eða ert kerfisstjóri og þú vilt fylla út fyrirtækisgögn sjálfkrafa í sérsniðinni skjámynd, geturðu valið [skjámyndatilvik](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids). Bættu við JavaScript tilvísun á **msdyn_/DefaultCompany.js** og nota eftirfarandi tilvik. Hægt er að nota hvaða tilbúnu skjámynd sem er, t.d. skjámyndina **Lykill**.

    + **OnLoad** tilvik fyrir skjámyndina: Stillið dálkinn **defaultCompany**.
    + **OnChange** tilvik fyrir dálkinn **Fyrirtæki**: Stillið dálkinn **updateDefaultCompany**.

## <a name="apply-filtering-based-on-the-company-context"></a>Nota síun sem byggir á samhengi fyrirtækis

Til að nota síun sem byggir á samhengi fyrirtækisins í sérsniðnum skjámyndum eða í sérsniðnum uppflettidálkum sem bætt hefur verið við staðlaðar skjámyndir, skal opna skjámyndina og nota hlutann **Síun á tengdum færslum** til að nota fyrirtækissíuna. Þetta verður að stilla fyrir hvern uppflettidálk sem krefst síunar sem byggir á undirliggjandi fyrirtæki fyrir uppgefna röð. Stillingin er sýnd fyrir **Lykil** á eftirfarandi mynd.

:::image type="content" source="media/apply-company-context.png" alt-text="Nota samhengi fyrirtækis":::

