---
title: Stjórnun viðskiptavina í verslunum
description: Þetta efnisatriði útskýrir hvernig smásöluaðilar geta virkjað stjórnunarmöguleika viðskiptavinar á sölustað í Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 05/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: dd17593d84a8bf262712a84b11829f8ec6c49049
ms.sourcegitcommit: c5c8f19a696ad4a3d68dffd63bfe7b484b999d2b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/25/2021
ms.locfileid: "6097209"
---
# <a name="customer-management-in-stores"></a>Stjórnun viðskiptavina í verslunum

[!include [banner](includes/banner.md)]

Þetta efnisatriði útskýrir hvernig smásöluaðilar geta virkjað stjórnunarmöguleika viðskiptavinar á sölustað í Microsoft Dynamics 365 Commerce.

Mikilvægt er að fulltrúar verslunar geti stofnað og breytt færslum viðskiptavina á sölustað. Þannig geta þeir sótt uppfærslur á upplýsingum um viðskiptavin á borð við netfang, símanúmer og heimilisfang. Þessar upplýsingar eru gagnlegar í ofansæknum kerfum á borð við markaðssetningu vegna þess að skilvirkni þessara kerfa fer eftir nákvæmni viðskiptavinagagnanna.

Söluaðilar geta sett af stað verkflæði fyrir stofnun viðskiptavinar á tveimur aðgangsstöðum sölustaðar. Þeir geta valið hnapp sem varpað er í aðgerðina **Bæta við viðskiptavini** eða þeir geta valið **Stofna viðskiptavin** á forritastikunni á síðu leitarniðurstaðna. Í báðum tilvikum birtist svarglugginn **Nýr viðskiptavinur** þar sem söluaðilar geta slegið inn nauðsynlegar upplýsingar um viðskiptavin, svo sem nafn viðskiptavinar, netfang, símanúmer, heimilisfang og frekari upplýsingar sem tengjast viðskiptunum. Þessar viðbótarupplýsingar er hægt að sækja með því að nota eigindir viðskiptavinar sem tengjast viðskiptavininum. Frekari upplýsingar um eigindir viðskiptavinar er að finna í [Eigindir viðskiptavinar](dev-itpro/customer-attributes.md).

Söluaðilar geta einnig sótt önnur netföng og símanúmer. Þar að auki geta þeir sótt kjörstillingar viðskiptavinar hvað varðar móttöku markaðsupplýsinga í gegnum eitt þessara aukalegu netfanga eða símanúmera. Til að virkja þennan möguleika verða smásöluaðilar að kveikja á eiginleikanum **Sækja mörg netföng og símanúmer og samþykki fyrir markaðssetningu til þessara tengiliða** á vinnusvæðinu **Eiginleikastjórnun** í höfuðstöðvum Commerce (**Kerfisstjórnun \> Vinnusvæði \> Eiginleikastjórnun**).

## <a name="default-customer-properties"></a>Eiginleikar sjálfgefins viðskiptavinar

Smásöluaðilar geta notað síðuna **Allar verslanir** í höfuðstöðvum Commerce (**Smásala og viðskipti \> Rásir \> Verslanir**) til að tengja sjálfgefinn viðskiptavin við hverja verslun. Commerce afritar þá eiginleikana sem eru skilgreindir fyrir sjálfgefna viðskiptavininn í allar nýjar færslur viðskiptavinar sem eru stofnaðar. Til dæmis sýnir svarglugginn **Stofna viðskiptavin** eiginleika sem eru erfðir frá sjálfgefnum viðskiptavini sem tengist versluninni. Þessir eiginleikar innihalda **viðskiptavinagerð**, **viðskiptavinaflokk**, **valkost kvittunar**, **tölvupóstur kvittunar**, **gjaldmiðil** og **tungumál**. Öll **tengsl** (flokkanir viðskiptavina) eru einnig erfð frá sjálfgefnum viðskiptavini. **Fjárhagsvíddir** eru hins vegar erfðar frá viðskiptavinaflokknum sem tengist sjálfgefnum viðskiptavini, ekki beint frá sjálfgefna viðskiptavininum.

> [!NOTE]
> Gildið fyrir **tölvupóst kvittunar** er afritað úr sjálfgefnum viðskiptavini aðeins ef kenni tölvupósts vegna kvittunar er ekki gefið upp fyrir nýlega stofnaða viðskiptavini. Þetta þýðir að ef kenni tölvupósts vegna kvittunar er til staðar í sjálfgefnum viðskiptavini, þá fá allir viðskiptavinir sem stofnaðir eru á svæði rafrænna viðskipta sama tölvupóstskenni kvittunar því ekki er neitt notandaviðmót til að ná í tölvupóstskenni kvittunar frá viðskiptavininum. Mælt er með því að halda reit **kvittunartölvupósts** auðum fyrir sjálfgefinn viðskiptavin verslunarinnar og aðeins nota hann þú ert með viðskiptaferli sem reiðir sig á að netfang fyrir kvittun sem til staðar. 

Söluaðilar geta sótt mörg heimilisföng fyrir viðskiptavin. Nafn og símanúmer viðskiptavinar eru fengin frá tengslaupplýsingum sem tengjast hverju heimilisfangi. Flýtiflipinn **Heimilisföng** fyrir viðskiptavinafærslu inniheldur reitinn **Tilgangur** sem söluaðilar geta breytt. Ef gerð viðskiptavinar er **Einstaklingur** verður sjálfgefna gildið **Heimili**. Ef gerð viðskiptavinar er **Fyrirtæki** verður sjálfgefna gildið **Vinnustaður**. Önnur gildi sem þessi reitur styður eru m.a. **Heimili**, **Skrifstofa** og **Pósthólf**. Gildi reitsins **Land** fyrir heimilisfang er fengið frá aðalheimilsfanginu sem er tilgreint á síðunni **Rekstrareining** í höfuðstöðvum Commerce í **Fyrirtækisstjórnun \> Fyrirtæki \> Rekstrareiningar**.

## <a name="sync-customers-and-async-customers"></a>Samstilltir viðskiptavinir og ósamstilltir viðskiptavinir

Í Commerce eru til tvær stillingar fyrir stofnun viðskiptavinar: Samstillt og ósamstillt. Viðskiptavinir eru stofnaðir samstilltir að sjálfgefnu. Þ.e.a.s. þeir eru stofnaðir í Commerce Headquarters á rauntíma. Samstillt stofnun viðskiptavinar er gagnleg vegna þess að strax verður hægt að leita að nýjum viðskiptavinum yfir allar rásir. Hins vegar er einnig galli á henni. Þar sem hún myndar köll [Commerce Data Exchange: Rauntímaþjónustu](dev-itpro/define-retail-channel-communications-cdx.md#realtime-service) til Commerce Headquarters, þá getur það haft áhrif á afköst ef mörg köll vegna stofnunar viðskiptavina eru gerð á sama tíma.

Ef valkosturinn **Stofna viðskiptavin í Async-stillingu** er stilltur á **Já** í virknireglu verslunar (**Smásala og viðskipti \> Uppsetning rásar \> Uppsetning netverslunar \> Virknireglur**), þá eru köll rauntímaþjónustu ekki notuð til að stofna viðskiptavinafærslur í gagnagrunni rásarinnar. Async-stilling á stofnun viðskiptavinar hefur ekki áhrif á afköst Commerce Headquarters. Altækt einkvæmt kennimerki (GUID) er úthlutað til sérhverrar nýrrar ósamstilltrar viðskiptavinafærslu og notað sem auðkenni viðskiptavinareiknings. Notendur sölustaðar fá ekki að sjá þetta GUID. Þess í stað munu þessir notendur sjá **Bíður samstillingar** sem auðkenni viðskiptavinareikningsins. Þótt þessi skilgreining geri það að verkum að viðskiptavinir verði stofnaðir ósamstillt skal hafa í huga að breytingar á viðskiptavinafærslum eru alltaf gerðar samstillt.

### <a name="convert-async-customers-to-sync-customers"></a>Breyta ósamstilltum viðskiptavinum í samstillta viðskiptavini

Til að breyta ósamstilltum viðskiptavinum í samstillta viðskiptavini þarf fyrst að keyra P-vinnslu til að senda ósamstillta viðskiptavini til Commerce Headquarters. Síðan skal keyra vinnsluna **Samstilla viðskiptavini og viðskiptafélaga úr async-stillingu** til að stofna auðkenni viðskiptavinareikninga. Keyrið að lokum vinnsluna **1010** til að samstilla ný auðkenni viðskiptavinareikninga við rásirnar.

### <a name="async-customer-limitations"></a>Takmarkanir ósamstilltra viðskiptavina

Virkni ósamstilltra viðskiptavina er sem stendur með eftirfarandi takmarkanir:

- Ekki er hægt að breyta ósamstilltum færslum viðskiptavina nema viðskiptavinurinn hafi verið stofnaður í Commerce Headquarters og nýtt auðkenni viðskiptavinareiknings hefur verið samstillt aftur við rásina.
- Tengsl geta ekki verið tengd við ósamstillta viðskiptavini. Þar af leiðandi erfa nýir ósamstilltir viðskiptavinir ekki tengsl frá sjálfgefnum viðskiptavini.
- Ekki er hægt að gefa út vildarkort til ósamstilltra viðskiptavina nema nýtt auðkenni viðskiptavinareiknings hafi verið samstillt aftur við rásina.
- Ekki er hægt að sækja önnur netföng og símanúmer fyrir ósamstillta viðskiptavini.

### <a name="customer-creation-in-pos-offline-mode"></a>Stofnun viðskiptavinar á sölustað án nettengingar

Ef sölustaðurinn missir netsamband á meðan stilling fyrir stofnun ósamstillts viðskiptavinar er virkjuð, verða nýjar viðskiptavinafærslur stofnaðar ósamstillt. Ef sölustaður missir netsamband á meðan verið er að slökkva á stillingu fyrir stofnun ósamstillts viðskiptavinar, skiptir kerfið sjálfkrafa í stillingu fyrir stofnun ósamstillts viðskiptavinar. Þ.e.a.s. færslur viðskiptavina gætu verið stofnaða ósamstillt jafnvel þótt slökkt sé á stillingu fyrir stofnun ósamstillts viðskiptavinar. Þess vegna verða stjórnendur Commerce Headquarters að búa til og tímasetja endurtekna runuvinnslu fyrir P-vinnslu, vinnsluna **Samstilla viðskiptavini og viðskiptafélaga úr async-stillingu** og **1010** vinnslunni þannig að öllum ósamstilltum viðskiptavinum er breytt í samstillta viðskiptavini í Commerce Headquarters.

> [!NOTE]
> Ef valkosturinn **Afmarka samnýttar gagnatöflur viðskiptavinar** er stilltur á **Já** á síðunni **Skema fyrir viðskiptarás** (**Smásala og viðskipti \> Uppsetning höfuðstöðva \> Viðskiptaverkraðari \> Gagnagrunnsflokkur rásar**), verða færslur viðskiptavina ekki stofnaðar á sölustað sem er án tengingar. Frekari upplýsingar er að finna í [Útilokun gagna án nettengingar](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion).

## <a name="additional-resources"></a>Frekari upplýsingar

[Eigindir viðskiptavinar](dev-itpro/customer-attributes.md)

[Útilokun gagna án nettengingar](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
