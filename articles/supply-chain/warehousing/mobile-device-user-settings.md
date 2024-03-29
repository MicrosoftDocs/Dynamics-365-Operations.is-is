---
title: Notandastillingar fartækis
description: Þessi grein útskýrir hvernig á að stjórna notendastillingum fartækis fyrir starfsmenn í vöruhúsi.
author: Mirzaab
ms.date: 02/09/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSMobileAppDeviceBrand,WHSMobileAppUserDisplaySettings
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2021-02-09
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 15f9ce1768e1ed9dc6f7e84d245082b46a7f122c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882345"
---
# <a name="mobile-device-user-settings"></a>Notandastillingar fartækis

[!include [banner](../../includes/banner.md)]

Nýja farsímaforritið fyrir Vöruhúsakerfi er með sértækar stillingar fyrir forrit sem hjálpa til við að bæta notandaupplifunina. Þar sem hægt er að nota forritið í tækjum með mismunandi skjástærð og grunnstillingar (svo sem spjaldtölva eða sími), er hægt að nota það til að stjórna miðlægt þessum stillingum úr Microsoft Dynamics 365 Supply Chain Management.

Með eiginleikanum *notandastillingar fartækis* er hægt að skilgreina altækar notandastillingar sem verða notaðar í öllum tækjum. Einnig er hægt að skilgreina fleiri stakar Notendastillingar fyrir stök tækjasniðmát, gerðir tækja og/eða starfskrafta. Þegar starfsmaður skráir sig inn í farsímaforrit í vöruhúsakerfi sækir forritið og beitir sértækustu forstillingunum sem eru geymdar í Supply Chain Management fyrir samsvarandi gerð, tæki og/eða notandakenni.

Þessi eiginleiki getur hjálpað starfsmönnum að hefjast handa á skjótan hátt hvenær sem er þegar þeir byrja að nota nýtt tæki. Hér eru nokkur dæmi:

- Stjórnendur geta komið á fót stöðluðu safni af kjörstillingum sem hentar best fyrir tæki frá tilteknum framleiðanda og/eða fyrir tilteknar gerðir tækja. Því geta starfsmenn hafist handa með nýtt tæki án þess að þurfa endilega að breyta stillingum.
- Ef fyrirtækið er með hóp samskonar tækja sem eru samnýtt af starfsmönnum munu þeir sjá æskilega uppsetningu þeirra í hvert skipti sem þeir skrá sig inn, jafnvel þótt þeir hafi aldrei notað tilgreint efnislegt tæki sem þeir völdu á tilteknum degi.
- Í Supply Chain Management geta stjórnendur skoðað og breytt öllum vistuðum stillingum, jafnvel fyrir einstaka starfsmenn. Þetta getur hjálpað til við úrræðaleit eða til að fínstilla nýja eiginleika.

> [!IMPORTANT]
> *Notandastillingar fartækis* eiginleikinn gildir aðeins fyrir nýja farsímaforrit vöruhúsakerfis. Þetta virkar ekki með eldra forriti vöruhússins.

## <a name="turn-the-mobile-device-user-settings-feature-on-or-off"></a>Kveikja eða slökkva á eiginleika notandastillinga fartækis

Til að nota virknina sem lýst er í þessari grein verður að vera kveikt á eiginleikanum *Notandastillingar, tákn og titlar skrefa fyrir nýja vöruhúsaforritið* fyrir kerfið. Frá og með útgáfu 10.0.25 af Supply Chain Management er þessi eiginleiki skylda og ekki er hægt að slökkva á henni. Ef þú ert að keyra útgáfu sem er eldri en 10.0.25 geta stjórnendur kveikt eða slökkt á þessum eiginleika með því að leita að eiginleikanum *Notandastillingar, tákn og titlar skrefa fyrir nýja vöruhúsaforritið* á vinnusvæðinu [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="create-and-manage-user-settings"></a>Stofna og stjórna notandastillingum

Notið **Notandastillingar fartækis** síðuna til að búa til, skoða og stjórna forstillingum á öllum stigum uppskiptingar. Í fyrsta skipti sem starfsmaður breytir notandastillingum sínum í nýju tæki er nýrri forstillingu sjálfkrafa bætt við á þessari síðu ef hún er ekki þegar til. Þessi forstilling er uppfærð í hvert skipti sem starfskrafturinn gerir breytingu.

Einnig er hægt að skilgreina forstillingarsnið sem gildir fyrir öll tæki, gerðir og/eða starfskrafta. Síðan er hægt að auka uppskiptingi með því að setja á fleiri sértækar stillingar fyrir einstaka gerðir, tegundir og/eða starfsmenn.

Fylgdu þessum skrefum til að búa til og stjórna notendastillingum fyrir fartæki.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Notandastillingar fartækis**.
1. Velja skal fyrirliggjandi forstillingu notandastillinga úr listasvæðinu til að opna færslu hennar. Einnig er hægt að velja **Nýtt** á aðgerðasvæðinu til að búa til nýjar forstillingar.

    Hver forstilling á listasvæðinu er merkt til að gefa til kynna gerð, tegund og/eða notandakenni sem forstillingin á við um. Fleiri almennar forstillingar eru með gildið *Allt* fyrir sum þessara einkenna.

1. Í haus hlutans í færslunni fyrir nýju eða völdu stillingarforstillinguna skal stilla eftirfarandi reiti:

    - **Vöruheiti tækis** – Veljið vörumerki tækisins sem forstillingin á að gilda fyrir. Ef forstillingin ætti að gilda fyrir öll vörumerki skal láta þennan reit vera auðan. Listinn yfir gildin inniheldur öll vörumerki sem hafa verið skilgreind í kerfinu. Upplýsingar um hvernig skilgreina á lista yfir vörumerki er að finna í næsta hluta.
    - **Kenni tækjategundar** – Veljið gerð tækisins sem forstillingin á að gilda fyrir. Ef forstillingin ætti að gilda fyrir allar gerðir vörumerkisins skal láta þennan reit vera auðan. Listi yfir gildin fela í sér öll líkön sem hafa verið skilgreind fyrir tegundina sem er valin **Vöruheiti tækis** reiturinn. Frekari upplýsingar um hvernig á að skilgreina lista yfir gerðir fyrir hvert vörumerki er að finna í næsta hluta.
    - **Notandakenni** – Veljið notandakenni starfskrafts vöruhússins sem stillingasniðin á að gilda fyrir. Ef forstillingin á að gilda fyrir alla stafskrafta skal skilja þennan reit eftir auðan.

1. Á flýtiflipanum **Almennt** stillirðu eftirfarandi reiti:

    - **Staðsetning hnapps** – Veljið hvernig á að staðsetja hnappa á tækinu. Einingarnar í forritinu verða fluttar til að passa betur við kjörstillingar eða því hvort starfskrafturinn er rétthentur eða örvhentur. Tiltækir valmöguleikar eru *Neðst til hægri (sjálfgefið)*, *Neðst til vinstri*, *Efst til hægri* og *Efst til vinstri*.
    - **Sýna legu** – Veljið birtingarstefnu sem á að nota sjálfkrafa í forritinu.
    - **Skanna með myndavél** – Stillið þennan valkost á *Já* til að nota myndavél tækisins til að skanna innsláttarreiti þar sem æskileg innsláttarstilling er stillt á *Skönnun*. Ef tækið er með innbyggðan skanna skal stilla þennan valkost á *Nei* til að nota skannann í staðinn.
    - **Sýna mynd afurðar** – Veljið hvort sýna eigi afurðamyndir ef þær eru í boði fyrir útgefna afurð. Frekari upplýsingar um það hvernig á að bæta við afurðarmyndum má finna í [Bæta mynd við vöru](../pim/tasks/add-image-product.md).
    - **Birta litaþema** – Veljið litaþema fyrir tækið.
    - **Hljóðstyrkur** – Veljið hljóðstig fyrir tækið. Veldu gildi milli núll (0) og 10. Gildið *0* táknar ekkert hljóð og gildið *10* táknar hámarkshljóð. Sjálfgildið er *4*.
    - **Titringsstig** – Veljið titringsstig fyrir tækið. Veldu gildi milli núll (0) og 5. Gildið *0* táknar engan titring og gildið *5* táknar hámarkstitring. Sjálfgildið er *1*.
    - **Kvörðunarhlutfal texta** – Tilgreinir stærð texta sem prósentur af stöðluðu stærðinni. Sláðu inn gildli á bilinu 70 til 400. Gildið *70* táknar minnsta textakvarða og gildið *400* táknar stærsta textakvarðann. Sjálfgildið er *100*.
    - **Kvörðunarhlutfall hnapps** – Tilgreinir stærð hnappsins sem prósentu af stöðluðu stærðinni. Sláðu inn gildli á bilinu 50 til 200. Gildið *50* táknar minnsta hnappakvarðann og gildið *200* táknar stærsta hnappakvarðann. Sjálfgildið er *100*.

## <a name="create-and-manage-mobile-device-brands"></a>Stofna og stjórna vörumerki fartækis

Notið **Vörumerki fartækja** síða til að skoða, stofna og stjórna vörumerkjum og gerðum tækjasem hægt er að nota með stillingasniðum. Fartækjaforritið sækir sjálfkrafa og sendir inn staðbundið heiti vöru og auðkenni líkans í fyrsta skipti sem starfsmaður breytir stillingum sínum á tilteknu tæki. Þess vegna verða flestar þessar færslur yfirleitt sjálfkrafa myndaðar. Hins vegar er einnig hægt að stjórna öllum færslunum á þessari síðu. Til dæmis er hægt að gefa upp gagnlegri upplýsingar til hverrar vöru og tegundar til að gera greinarmun á svipuðum dulkóðuðum auðkennum líkana.

Fylgið eftirfarandi skrefum til að búa til og stjórna eigin tegundum og gerðum fartækja.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Fartækjavörumerki**.
1. Á listasvæðinu skal velja gerð fartækis til að opna færslu þess. Einnig er hægt að velja **Nýtt** á aðgerðasvæðinu til að búa til nýtt vörumerki.
1. Í haushluta færslunnar fyrir nýtt eða valið vörumerki tækis skal stilla eftirfarandi reiti:

    - **Vöruheiti tækis** – Vörumerki tækisins, t.d. *Microsoft Corporation*.
    - **Lýsing** – Hægt er að færa inn lýsingu til að aðstoða við að aðgreina vöruheiti.

1. **Gerðir fartækja** Flýtiflipi sýnir öll líkanið fyrir valda gerð tækis. Notið hnappana á tækjastikunni til að bæta línum við hnitanetið eða til að fjarlægja línur. Fyrir hverja línu er hægt að stilla eftirfarandi reiti:

    - **Kenni tækjategundar** – Kenni tækjagerðinnar, svo sem *Surface Book 2*.
    - **Lýsing** – Hægt er að færa inn lýsingu til að aðstoða við að aðgreina kenni gerða.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Setja upp og tengja farsímaforrit vöruhúsakerfis](install-configure-warehouse-management-app.md)
- [Úthluta skrefatáknum og titlum fyrir Warehouse Management farsímaforritið](step-icons-titles.md)