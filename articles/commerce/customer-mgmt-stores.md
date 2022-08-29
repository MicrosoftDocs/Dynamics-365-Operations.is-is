---
title: Stjórnun viðskiptavina í verslunum
description: Þessi grein útskýrir hvernig smásalar geta virkjað getu viðskiptavinastjórnunar á sölustað (POS) í Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 12/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: shajain
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.search.industry: retail
ms.search.form: RetailOperations
ms.openlocfilehash: 2928aa5c4e62611b54799fbe7c1bba25fe186bcd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282242"
---
# <a name="customer-management-in-stores"></a>Stjórnun viðskiptavina í verslunum

[!include [banner](includes/banner.md)]

Þessi grein útskýrir hvernig smásalar geta virkjað getu viðskiptavinastjórnunar á sölustað (POS) í Microsoft Dynamics 365 Commerce.

Mikilvægt er að fulltrúar verslunar geti stofnað og breytt færslum viðskiptavina á sölustað. Þannig geta þeir sótt uppfærslur á upplýsingum um viðskiptavin á borð við netfang, símanúmer og heimilisfang. Þessar upplýsingar eru gagnlegar í ofansæknum kerfum á borð við markaðssetningu vegna þess að skilvirkni þessara kerfa fer eftir nákvæmni viðskiptavinagagnanna.

Söluaðilar geta sett af stað verkflæði fyrir stofnun viðskiptavinar á tveimur aðgangsstöðum sölustaðar. Þeir geta valið hnapp sem varpað er í aðgerðina **Bæta við viðskiptavini** eða þeir geta valið **Stofna viðskiptavin** á forritastikunni á síðu leitarniðurstaðna. Í báðum tilvikum birtist svarglugginn **Nýr viðskiptavinur** þar sem söluaðilar geta slegið inn nauðsynlegar upplýsingar um viðskiptavin, svo sem nafn viðskiptavinar, netfang, símanúmer, heimilisfang og frekari upplýsingar sem tengjast viðskiptunum. Þessar viðbótarupplýsingar er hægt að sækja með því að nota eigindir viðskiptavinar sem tengjast viðskiptavininum. Frekari upplýsingar um eigindir viðskiptavinar er að finna í [Eigindir viðskiptavinar](dev-itpro/customer-attributes.md).

Söluaðilar geta einnig sótt önnur netföng og símanúmer. Þar að auki geta þeir sótt kjörstillingar viðskiptavinar hvað varðar móttöku markaðsupplýsinga í gegnum eitt þessara aukalegu netfanga eða símanúmera. Til að virkja þennan möguleika verða smásöluaðilar að kveikja á eiginleikanum **Sækja mörg netföng og símanúmer og samþykki fyrir markaðssetningu til þessara tengiliða** á vinnusvæðinu **Eiginleikastjórnun** í höfuðstöðvum Commerce (**Kerfisstjórnun \> Vinnusvæði \> Eiginleikastjórnun**).

## <a name="default-customer-properties"></a>Eiginleikar sjálfgefins viðskiptavinar

Smásöluaðilar geta notað síðuna **Allar verslanir** í höfuðstöðvum Commerce (**Smásala og viðskipti \> Rásir \> Verslanir**) til að tengja sjálfgefinn viðskiptavin við hverja verslun. Commerce afritar þá eiginleikana sem eru skilgreindir fyrir sjálfgefna viðskiptavininn í allar nýjar færslur viðskiptavinar sem eru stofnaðar. Til dæmis sýnir svarglugginn **Stofna viðskiptavin** eiginleika sem eru erfðir frá sjálfgefnum viðskiptavini sem tengist versluninni. Þessir eiginleikar innihalda **viðskiptavinagerð**, **viðskiptavinaflokk**, **valkost kvittunar**, **tölvupóstur kvittunar**, **gjaldmiðil** og **tungumál**. Öll **tengsl** (flokkanir viðskiptavina) eru einnig erfð frá sjálfgefnum viðskiptavini. **Fjárhagsvíddir** eru hins vegar erfðar frá viðskiptavinaflokknum sem tengist sjálfgefnum viðskiptavini, ekki beint frá sjálfgefna viðskiptavininum.

> [!NOTE]
> Gildið fyrir **tölvupóst kvittunar** er afritað úr sjálfgefnum viðskiptavini aðeins ef kenni tölvupósts vegna kvittunar er ekki gefið upp fyrir nýlega stofnaða viðskiptavini. Þetta þýðir að ef kenni tölvupósts vegna kvittunar er til staðar í sjálfgefnum viðskiptavini, þá fá allir viðskiptavinir sem stofnaðir eru á svæði rafrænna viðskipta sama tölvupóstskenni kvittunar því ekki er neitt notandaviðmót til að ná í tölvupóstskenni kvittunar frá viðskiptavininum. Mælt er með því að skilja reit **kvittunartölvupósts** eftir auðan fyrir sjálfgefinn viðskiptavin verslunarinnar og aðeins nota hann ef þú ert með viðskiptaferli sem reiðir sig á að netfang fyrir kvittun sé til staðar. 

Söluaðilar geta sótt mörg heimilisföng fyrir viðskiptavin. Nafn og símanúmer viðskiptavinar eru fengin frá tengslaupplýsingum sem tengjast hverju heimilisfangi. Flýtiflipinn **Heimilisföng** fyrir viðskiptavinafærslu inniheldur reitinn **Tilgangur** sem söluaðilar geta breytt. Ef gerð viðskiptavinar er **Einstaklingur** verður sjálfgefna gildið **Heimili**. Ef gerð viðskiptavinar er **Fyrirtæki** verður sjálfgefna gildið **Vinnustaður**. Önnur gildi sem þessi reitur styður eru m.a. **Heimili**, **Skrifstofa** og **Pósthólf**. Gildi reitsins **Land** fyrir heimilisfang er fengið frá aðalheimilsfanginu sem er tilgreint á síðunni **Rekstrareining** í höfuðstöðvum Commerce í **Fyrirtækisstjórnun \> Fyrirtæki \> Rekstrareiningar**.



## <a name="additional-resources"></a>Frekari upplýsingar

[Ósamstillt stilling til að stofna viðskiptavin](async-customer-mode.md)

[Umbreyta ósamsettum viðskiptavinum í samstillta viðskiptavini](convert-async-to-sync.md)

[Eigindir viðskiptavinar](dev-itpro/customer-attributes.md)

[Útilokun gagna án nettengingar](dev-itpro/implementation-considerations-cdx.md#offline-data-exclusion)
