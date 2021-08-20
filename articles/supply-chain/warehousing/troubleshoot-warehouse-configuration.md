---
title: Úrræðaleit fyrir grunnstillingu vöruhúss
description: Þetta efnisatriði lýsir því hvernig á að laga almenn vandamál sem kunna að koma upp við stillingu Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 60873cb76ee08dd5a4bd4ed8b38cc4845b500453bf34bd10708b105448b58c9a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735088"
---
# <a name="troubleshoot-warehouse-configuration"></a>Úrræðaleit fyrir grunnstillingu vöruhúss

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að laga almenn vandamál sem kunna að koma upp við stillingu Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a>Ég fæ eftirfarandi villuboð: „Númeraplatan eða staðsetningin er ekki gild“.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þessi villuboð birtast þegar kenni númeraplötu eða staðsetning er skönnuð.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Gangið úr skugga um að kenni númeraplötunnar sé ekki tekið frá eitthvað annað. Þetta vandamál kom upp þegar gildið sem notandi skannaði í farsímaforriti vöruhúsakerfis var bæði gild staðsetning og gilt númerakenni. Hins vegar var þetta vandamál leyst í útgáfu 10.0.11.

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a>Ég fæ eftirfarandi villuboð: „Tilgreina þarf númeraplötu fyrir þessa staðsetningu“.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Þessi villuboð verða send ef flutningspöntun er stofnuð með því að nota vöruhús sem er virkt fyrir ítarlega vöruhúsastjórnun (WMS), og svo er reynt að staðfesta sendinguna eftir að vinnu er lokið.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Reiturinn **Sjálfgefin staðsetning innhreyfinga** er auður fyrir flutningsvöruhús „úr“ vöruhúsi. Til að laga þetta vandamál þarf að tilgreina sjálfgefna staðsetningu móttöku í flutningsvöruhúsinu. Ganga skal úr skugga um að þessi staðsetning sé númeraplata – stjórnað.

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a>Ég fæ eftirfarandi villuboð: Ekki er hægt að stofna vinnusniðmátslínu fyrir Breyting á birgðastöðu því að vinnutegundin er ógild. Velja skal aðra vinnutegund.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Fyrir vinnusniðmát er ekki hægt að velja *Breyting á birgðastöðu* í dálknum **Vinnusniðmát** í hlutanum **Upplýsingar um vinnusniðmát**.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Þessi hegðun er samkvæmt hönnuninni. Vinnutegundin *Breyting á birgðastöðu* er aðeins notuð af kerfisvinnslu. Ekki er hægt að stilla þetta. Vegna þess að listi yfir vinnugerðir er fastur sem tölusetning er ekki hægt að sía aukafærslur úr fellivalmyndinni **Vinnutegund**.

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a>Ég fæ eftirfarandi villuskilaboð: „Magnið er ekki gilt fyrir einingu „Magnið er ekki gilt fyrir einingu 1%“.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Magnið er ekki gilt fyrir *ea* eininguna þegar um er að ræða tiltektarvinnu sem er með margar númeraplötur á einni staðsetningu.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Gangið úr skugga um að **Auðkenni röðunarflokks einingar** og **Einingaumreikningar** reitir á útgefnu afurðina eða afurðarafbrigðið séu rétt stillt.

Athugið að villuboðin hafa verið endurbætt í útgáfu 10.0.15 (sjá [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)). Nýju villuboðin eru, Magnið er ekki gilt. Væntanlegt %1 %2."

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a>Í staðsetningarleiðbeiningum fyrir frágang sölupöntunar metur valkostur birgðahaldseiningar ekki margar aðgerðir staðsetningarleiðbeininga.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Staðsetningarleiðbeiningar af vinnutegundinni *Sölupantanir* og *Frágangur* ekki meta margar aðgerðir staðsetningarleiðbeininga þegar valkosturinn **Margar birgðahaldseiningar** er valinn. Aðeins fyrsta aðgerð fyrir staðsetningarleiðbeiningar er metin.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Nýr eiginleiki, *Meta allar aðgerðir fyrir staðsetningarleiðbeiningar margra birgðahaldseininga*, hefur verið bætt við útgáfu 10.0.15 (sjá [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)). Þessi eiginleiki metur allar aðgerðir fyrir staðsetningarleiðbeiningar margra birgðahaldseininga. Ef þessi eiginleiki er nauðsynlegur skal nota [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að kveikja á honum.

## <a name="i-cant-use-the-warehouse-management-mobile-app-to-do-partial-picking"></a>Ég get ekki notað farsímaforrit vöruhúsakerfis fyrir hlutatínslu.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Fyrir sölu-og flutningspantanir er ekki hægt að sleppa vörum og gera hlutatiltekt.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Á síðunni **Valmyndaratriði fartækis**, fyrir hvert valmyndaratriði sem er sett upp til að vinna sölupantanirnar eða flutningspantanir, skal stilla **Leyfa skiptingu vinnu** á flipanum **Almennt** í *Já*.

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a>Hvernig get ég breytt birgðastöðu fyrir verk að hluta?

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Ætlunin er að gera breytingu á birgðastöðu fyrir hlutamagn runu.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Til að gera starfskröftum kleift að gera þessa breytingu er hægt að stofna valmyndaratriði fyrir farsímaforrit vöruhúsakerfis. Á síðunni **Valmyndaratriði fartækis** skal stofna (eða breyta) valmyndaratriði sem er með eftirfarandi stillingum:

- **Máti:** *Vinna*
- **Nota fyrirliggjandi vinnu:** *Nei*
- **Ferli verkstofnunar:** *Hreyfing*
- **Birta birgðastöðu:** *Já*

Hægt er að stilla aðra reiti á síðunni eftir þörfum.

## <a name="the-dock-management-profile-of-a-location-profile-is-not-preventing-inventory-types-from-being-mixed"></a>Forstilling dreifingarstjórnunar fyrir staðsetningarforstillingu hindrar ekki að tegundir birgða blandist saman.

### <a name="issue-description"></a>Lýsing á úrlausnaratriði

Verið er að nota *samstæðureglur sendingar*. Setja þarf upp *forstillingu dreifingarstjórnunar* fyrir *staðsetningarforstillingu*, en þegar vinna er stofnuð er tegundum birgða blandað saman á lokastaðsetningunni.

### <a name="issue-resolution"></a>Úrlausn úrlausnaratriðis

Forstilling dreifingarstjórnunar krefst þess að vinnu sé skipt upp fyrirfram. Með öðrum orðum býst forstilling dreifingarstjórnunar við því að vinnuhaus verði ekki með mörgum frágangsstaðsetningum.

Til að forstilling dreifingarstjórnunar geti haft umsjón með blöndun birgða, þarf að setja upp vinnuhausaskil.

Í þessu dæmi er forstilling dreifingarstjórnunar skilgreind á þann hátt að **Birgðagerðir sem ætti ekki að blanda saman** er stillt á *Auðkenni sendingar* og við munum setja upp vinnuhausaskil fyrir hana:

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnusniðmát**.
1. Veljið **Gerð verkbeiðni** til að breyta (t.d. *Innkaupapantanir*).
1. Velið vinnusniðmátið til að breyta.
1. Á aðgerðasvæðinu skal velja **Breyta fyrirspurn**.
1. Opnið flipann **Röðun** og bætið við línu með eftirfarandi stillingum:
    - **Tafla** - *Tímabundnar vinnufærslur*
    - **Afleidd tafla:** - *Tímabundnar vinnufærslur*
    - **Reitur** - *Auðkenni sendingar*
1. Veljið **Í lagi**.
1. Þú ferð til baka á síðuna **Vinnusniðmát**. Á aðgerðasvæðinu skal velja **Vinnuhausaskil**.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Veljið gátreitinn sem tengist **Heiti reits** *Auðkenni sendingar*.
1. Í aðgerðarúðunni skal velja **Vista**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
