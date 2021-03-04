---
title: Flutningur gagnagerðar gjaldmiðils fyrir tvöföld skrif
description: Þetta efnisatriði lýsir því hvernig á að breyta fjölda aukastafa sem tvöföld skrif styðja fyrir gjaldmiðil.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 04/06/2020
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
ms.search.validFrom: 2020-04-06
ms.openlocfilehash: 6a0f114bce6bdb7813c93e9441744d67cd043c30
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683734"
---
# <a name="currency-data-type-migration-for-dual-write"></a>Flutningur gagnagerðar gjaldmiðils fyrir tvöföld skrif

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Hægt er að fjölga fjölda aukastafa sem eru studdir fyrir upphæðir gjaldmiðla upp í allt að 10. Sjálfgefin mörk eru fjórir aukastafir. Ef aukastöfum er fjölgað er komið í veg fyrir gagnatap þegar tvöföld skrif eru notuð til að samstilla gögn. Fjölgun aukastafa er breyting sem þarf að velja sérstaklega. Til að innleiða hana þarf að biðja Microsoft um aðstoð.

Leiðin til að breyta fjölda aukastafa felur í sér tvö skref:

1. Biðja um flutning frá Microsoft.
2. Breyta fjölda aukastafa í Dataverse.

Forritið Finance and Operations og Dataverse verða að styðja sama fjölda aukastafa í upphæðum gjaldmiðla. Annars getur gagnatap orðið þegar þessar upplýsingar eru samstilltar milli forrita. Flutningsferlið endurstillir hvernig gildi gjaldmiðils og gengis eru vistuð en það breytir ekki neinum gögnum. Þegar flutningnum er lokið eru fjölda aukastafa fyrir gjaldmiðilskóða og verðlagningu fjölgað og gögnin sem notendur slá inn og skoða eru með meiri nákvæmni.

Flutningur er valfrjáls. Ef þú gætir notið góðs af stuðningi fyrir fleiri aukastafi, mælum við með að þú hugleiðir flutning. Fyrirtæki sem ekki þurfa gildi með fleiri en fjórum aukastöfum þurfa ekki að breyta.

## <a name="requesting-migration-from-microsoft"></a>Beðið um flutning frá Microsoft

Geymsla fyrir núverandi gjaldmiðilsreiti í Dataverse getur ekki stutt meira en fjóra aukastafi. Í flutningsferlinu eru gildi gjaldmiðla þar af leiðandi afrituð í nýja innri reiti í gagnagrunninum. Þetta ferli heldur samfleytt áfram þar til öll gögn hafa verið flutt. Innan fyrirtækisins, við lok flutnings, taka nýju geymslugerðirnar við af þeim eldri en gagnagildin haldast óbreytt. Gjaldmiðilsreitirnir geta í kjölfarið stutt allt að 10 aukastafi. Meðan á flutningi stendur, er hægt að halda áfram að nota Dataverse án truflunar.

Á sama tíma er gengi breytt þannig að það styður allt að 12 aukastafi í stað núgildandi hámarks upp á 10. Þörf er á þessari breytingu svo að fjöldi aukastafa sé sá sami í bæði Finance and Operations-forritinu og Dataverse.

Flutningur breytir engum gögnum. Þegar reitum gjaldmiðils og gengis hefur verið breytt, geta stjórnendur stillt kerfið til að nota allt að 10 aukastafi fyrir gjaldmiðilsreiti með því að tilgreina fjölda aukastafa fyrir hvern gjaldmiðil færslu og fyrir verðlagningu.

### <a name="request-a-migration"></a>Óska eftir flutningi

Til að gera þennan eiginleika tiltækan skal senda tölvupóst á **CDSExpandDecimal@microsoft.com** og láta eftirfarandi upplýsingar fylgja með:

+ **Efnisatriði:** Óska eftir því að virkja stuðning við fjölgun aukastafa fyrir \<organizationID\>
+ **Meginmál:** Mig langar að virkja stuðning við fjölgun aukastafa fyrir fyrirtækið \<organizationID\>.

Fulltrúi Microsoft mun hafa samband við þig innan tveggja til þriggja virkra daga fyrir næstu skref.

Þegar beðið er um flutning ætti að hafa eftirfarandi upplýsingar í huga og gera viðeigandi ráðstafanir:

+ Tíminn sem þarf til að flytja gögnin fer eftir gagnamagni í kerfinu. Flutningur stórra gagnagrunna getur tekið nokkra daga.
+ Stærð gagnagrunnsins eykst tímabundið meðan flutningur er í gangi vegna þess að þörf er á viðbótarplássi fyrir vísa. Meirihluti viðbótarplássins er losað þegar flutningi lýkur.
+ Í flutningsferlinu, ef villur koma upp sem koma í veg fyrir að flutningi ljúki, eykur kerfið viðvaranir til notendaþjónustu Microsoft þannig að starfsfólk notendaþjónustu geti gripið inn í. En jafnvel þó að villur komi upp við flutninginn, verður áfram hægt að nota Dataverse að fullu.
+ Flutningsferlið er ekki afturkræft.

## <a name="changing-the-number-of-decimal-places"></a>Fjölda aukastafa breytt

Þegar flutningi er lokið getur Dataverse vistað tölur sem eru með fleiri aukastöfum. Stjórnendur geta valið hversu margir aukastafir eru notaðir fyrir tiltekna gjaldmiðilskóða og verðlagningu. Notendur Microsoft Power Apps, Power BI og Power Automate geta þá skoðað og notað tölur sem eru með fleiri aukastöfum.

Til að gera þessa breytingu þarf að uppfæra eftirfarandi stillingar í Power Apps:

+ **Kerfisstillingar: Gjaldmiðilsnákvæmni fyrir verðlagningu** - Reiturinn **Stilla gjaldmiðilsnákvæmni sem notuð er fyrir verðlagningu í öllu kerfinu** skilgreinir hvernig gjaldmiðillinn virkar fyrir fyrirtækið þegar **Nákvæmni í verðlagningu** er valið.
+ **Viðskiptastjórnun: Gjaldmiðlar** - Reiturinn **Nákvæmni gjaldmiðils** gerir notanda kleift að tilgreina sérsniðinn fjölda aukastafa fyrir tiltekinn gjaldmiðil. Til er varastilling fyrir fyrirtækjastillinguna.

Nokkrar takmarkanir eru til staðar:

+ Ekki er hægt að stilla gjaldmiðilsreitinn í einingu.
+ Aðeins er hægt að tilgreina fleiri en fjóra aukastafi á stigunum **Verðlagning** og **Gjaldmiðill færslu**.

### <a name="system-settings-currency-precision-for-pricing"></a>Kerfisstillingar: Nákvæmni gjaldmiðils fyrir verðlagningu

Eftir að flutningi er lokið geta stjórnendur stillt nákvæmni gjaldmiðilsins. Opnið **Stillingar \> Stjórnun** og veljið **Kerfisstillingar**. Síðan skal, í flipanum **Almennt**, breyta gildinu á reitnum **Stilla nákvæmni gjaldmiðils sem notaður er fyrir verðlagningu í öllu kerfinu** eins og sýnt er á eftirfarandi skýringarmynd.

![Kerfisstillingar fyrir gjaldmiðil](media/currency-system-settings.png)

### <a name="business-management-currencies"></a>Viðskiptastjórnun: Gjaldmiðlar

Ef nákvæmni gjaldmiðils fyrir tiltekinn gjaldmiðil þarf að vera önnur en fyrir nákvæmni gjaldmiðils sem notaður er fyrir verðlagningu, er hægt að breyta henni. Opnið **Stillingar \> Viðskiptastjórnun**, veljið **Gjaldmiðlar** og veljið gjaldmiðilinn sem á að breyta. Stillið síðan reitinn **Nákvæmni gjaldmiðils** á þann fjölda aukastafa sem sóst er eftir eins og sýnt er á eftirfarandi skýringarmynd.

![Stillingar gjaldmiðils fyrir ákveðinn stað](media/specific-currency.png)

### <a name="tables-currency-field"></a>töflur: Gjaldmiðilsreitur

Fjöldi aukastafa sem hægt er að stilla fyrir tiltekna gjaldmiðilsreiti takmarkast við fjóra.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]