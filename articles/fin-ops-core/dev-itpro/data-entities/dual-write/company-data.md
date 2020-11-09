---
title: Fyrirtækishugtak í Common Data Service
description: Þetta efni lýsir samþættingu fyrirtækjaupplýsinga milli Finance and Operations og Common Data Service.
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
ms.openlocfilehash: 46a6ed9763781de8e05cff7adadf75fe2a931fdc
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997527"
---
# <a name="company-concept-in-common-data-service"></a>Fyrirtækishugtak í Common Data Service

[!include [banner](../../includes/banner.md)]


Í Finance and Operations er hugtakið a *fyrirtæki* bæði lögleg smíð og viðskiptasmíð. Það er einnig öryggis- og sýnileikamörk fyrir gögn. Notendur vinna alltaf í samhengi við eitt fyrirtæki og flest gögnin eru röndótt af fyrirtækinu.

Common Data Service er ekki með sambærilegt hugtak. Næsta hugtakið er *rekstrareining* , sem er fyrst og fremst öryggis- og sýnileikamörk fyrir notendagögn. Þetta hugtak hefur ekki sömu lagalegu eða viðskiptalegu afleiðingar og hugtakið fyrirtæki.

Vegna þess að rekstrareining og fyrirtæki eru ekki sambærileg hugtök er ekki mögulegt að þvinga kortlagningu á milli þeirra (1: 1) í þeim tilgangi að samþætta Common Data Service. Hins vegar vegna þess að notendur verða sjálfgefið að geta séð sömu skrár í forritinu og Common Data Service, hefur Microsoft kynnt nýja einingu í Common Data Service sem heitir cdm\_Fyrirtæki. Þessi eining jafngildir fyrirtækinu í forritinu. Til að hjálpa til við að tryggja að sýnileiki gagna sé jafnstór milli forritsins og Common Data Service úr kassanum, mælum við með eftirfarandi uppsetningu fyrir gögn í Common Data Service:

+ Fyrir hverja færslu fyrirtækis Finance and Operations sem er virk fyrir tvískiptingu, er tilheyrandi cdm\_Fyrirtækjaskrá búin til.
+ Þegar cdm\_Fyrirtækjaskrá er búin til og virkjuð fyrir tvískipt skrif, er sjálfgefin rekstrareining búin til með sama nafn. Þó að sjálfgefið teymi sé sjálfkrafa búið til fyrir þá rekstrareiningu er rekstrareiningin ekki notuð.
+ Sérstakt eigendateymi er búið til sem hefur sama nafn. Það er líka tengt rekstrareiningunni.
+ Sjálfgefið að eigandi skrár sem er búinn til og tvískrifaður til Common Data Service er stillt á „DW Owner“ teymið sem er tengt tilheyrandi rekstrareiningum.

Eftirfarandi skýringarmynd sýnir dæmi um þessa gagnauppsetningu í Common Data Service.

![Uppsetning gagna í Common Data Service](media/dual-write-company-1.png)

Vegna þessarar stillingar verða allar skrár sem tengjast USMF fyrirtækinu í eigu teymis sem er tengt USMF viðskiptareiningunni í Common Data Service. Þess vegna getur hver notandi sem hefur aðgang að þeirri rekstrareiningu með öryggishlutverki sem er stillt á sýnileika rekstrareininga, nú séð þessar skrár. Eftirfarandi dæmi sýnir hvernig hægt er að nota teymi til að veita réttan aðgang að þeim skrám.

+ Hlutverkinu „Sölustjóri“ er úthlutað til meðlima „USMF sölu“ teymisins.
+ Notendur sem hafa hlutverk „sölustjóra“ geta fengið aðgang að öllum reikningsgögnum sem eru aðilar að sömu viðskiptareiningunni og þeir eru aðilar að.
+ "USMF Sales" teymið er tengt við USMF viðskiptadeildina sem áður var nefnd.
+ Þess vegna geta meðlimir í "USMF sölu" teyminu séð hvaða reikning sem er í eigu "USMF DW" notandans, sem hefði komið frá USMF fyrirtækinu í Finance and Operations.

![Hvernig hægt er að nota teymi](media/dual-write-company-2.png)

Eins og myndin hér að ofan sýnir er þessi 1:1 kortlagning milli rekstrareiningar, fyrirtækis og teymis aðeins upphafspunktur. Í þessu dæmi er ný „eining“ í Evrópu búin til handvirkt í Common Data Service sem yfireining bæði fyrir DEMF og ESMF. Þessi nýja rótarviðskiptaeining er ekki skyld tvöföldum skrifum. Hins vegar er hægt að nota hana til að veita meðlimum „EUR Sales“ teymisins aðgang að reikningsgögnum bæði í DEMF og ESMF með því að stilla sýnileika gagna á **Yfir-/undir-BU** í tilheyrandi öryggishlutverki.

Lokaumræðan sem þarf að ræða er hvernig tvískipt skrifa ákvarðar hvaða eigendateymi það ætti að úthluta skrám til. Þessari hegðun er stjórnað af reitnum **Sjálfgefið eigendateymi** á cdm\_Fyrirtækjaskrá. Þegar cdm\_Fyrirtækjaskrá er virk fyrir tvískipta skrifun, stofna viðbætur sjálfkrafa tilheyrandi viðskiptaeiningu og eigendateymi (ef það er ekki þegar til) og stillir reitinn **Sjálfgefið eigendateymi**. Stjórnandi getur breytt þessum reit í annað gildi. Stjórnandi getur þó ekki hreinsað reitinn svo framarlega sem einingin er virk fyrir tvískipta skrifun.

> [!div class="mx-imgBorder"]
![Reiturinn Sjálfgefið eigendateymi](media/dual-write-default-owning-team.jpg)

## <a name="company-striping-and-bootstrapping"></a>Fyrirtækjaskrár og ræsibönd

Common Data Service-samþætting færir fyrirtækjajöfnun með því að nota auðkenni fyrirtækisins til að randa gögn. Eins og eftirfarandi mynd sýnir, eru allar fyrirtækjasértækar einingar útvíkkaðar þannig að þær hafa mörg-til-einn (N: 1) vensl við cdm\_Fyrirtækjaeining.

> [!div class="mx-imgBorder"]
![N:1 vensl milli fyrirtækjasértakrar einingar og einingarinnar cdm_Company](media/dual-write-bootstrapping.png)

+ Fyrir skrár, eftir að fyrirtæki er bætt við og vistað, verður gildið aðeins lesanlegt. Þess vegna ættu notendur að gæta þess að þeir velja rétt fyrirtæki.
+ Aðeins skrár sem hafa fyrirtækjagögn eru gjaldgengar fyrir tvískiptingu milli forritsins og Common Data Service.
+ Fyrir núverandi gögn Common Data Service mun stjórnandaleidd ræsibandareynsla brátt verða tiltæk.


## <a name="autopopulate-company-name-in-customer-engagement-apps"></a>Heiti fyrirtækis sem er sjálfkrafa fyllt út í forritum fyrir viðskiptavini

Ýmsar leiðir eru til að fylla út sjálfkrafa Fyrirtækisheitið í forritum fyrir viðskiptavini.

+ Ef notandi er kerfisstjóri er hægt að stilla sjálfgefið fyrirtæki með því að fara í **Ítarlegar stillingar > Kerfi > Öryggi > notendur**. Opnaðu skjámyndina **Notandi** og í **Upplýsingar um stofnun/fyrirtæki** hlutanum skaltu stilla gildið **Fyrirtækið á sjálfgefin á skjámyndum**.

    :::image type="content" source="media/autopopulate-company-name-1.png" alt-text="Velja sjálfgefið fyrirtæki í upplýsingahluta fyrirtækis.":::

+ Ef þú hefur **skrifheimild** fyrir **SystemUser** eininguna fyrir stig **Viðskiptaeiningar** , getur þú breytt sjálfgefna fyrirtækinu í hvaða skjámynd sem er með því að velja fyrirtæki úr fellivalmynd **Fyrirtækis**.

    :::image type="content" source="media/autopopulate-company-name-2.png" alt-text="Breyta heiti fyrirtækisins á nýjum lykli.":::

+ Ef þú hefur **skrifheimild** fyrir gögn í fleiri en einu fyrirtæki, geturðu breytt sjálfgefna fyrirtækinu með því að velja færslu sem tilheyrir öðru fyrirtæki.

    :::image type="content" source="media/autopopulate-company-name-3.png" alt-text="Að velja færslu breytir sjálfgefna fyrirtækinu.":::

+ Ef þú sérð um kerfisstillingar eða ert kerfisstjóri og þú vilt fylla út fyrirtækisgögn sjálfkrafa í sérsniðinni skjámynd, geturðu valið [skjámyndatilvik](https://docs.microsoft.com/powerapps/developer/model-driven-apps/clientapi/events-forms-grids). Bættu við JavaScript tilvísun á **msdyn_/DefaultCompany.js** og nota eftirfarandi tilvik. Hægt er að nota hvaða tilbúnu skjámynd sem er, t.d. skjámyndina **Lykill**.

    + **OnLoad** tilvik fyrir skjámyndina: Stillið reitinn **defaultCompany**.
    + **OnChange** tilvik fyrir reitinn **Fyrirtæki** : Stillið reitinn **updateDefaultCompany**.

## <a name="apply-filtering-based-on-the-company-context"></a>Nota síun sem byggir á samhengi fyrirtækis

Til að nota síun sem byggir á samhengi fyrirtækisins í sérsniðnum skjámyndum eða í sérsniðnum uppflettireitum sem bætt hefur verið við staðlaðar skjámyndir, skal opna skjámyndina og nota hlutann **Síun á tengdum færslum** til að nota fyrirtækissíuna. Þetta verður að stilla fyrir hvern uppflettireit sem krefst síunar sem byggir á undirliggjandi fyrirtæki fyrir uppgefna færslu. Stillingin er sýnd fyrir **Lykil** á eftirfarandi mynd.

:::image type="content" source="media/apply-company-context.png" alt-text="Nota samhengi fyrirtækis":::

