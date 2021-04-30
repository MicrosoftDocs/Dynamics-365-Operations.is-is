---
title: Skilgreina söluskatt fyrir pantanir á netinu
description: Þetta efnisatriði veitir yfirlit yfir val á VSK-flokki fyrir mismunandi gerðir pantana á netinu í Dynamics 365 Commerce.
author: gvrmohanreddy
manager: AnnBe
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: gmohanv
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8df939c1a566fb63bc53e455cc6c2aa85956ac79
ms.sourcegitcommit: 583801af75c50915ea5ffc60e831fb617d045533
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2021
ms.locfileid: "5853812"
---
# <a name="configure-sales-tax-for-online-orders"></a>Skilgreina söluskatt fyrir pantanir á netinu

[!include [banner](includes/banner.md)]

Þetta efnisatriði veitir yfirlit yfir val á VSK-flokki fyrir mismunandi gerðir pantana á netinu með því að nota annaðhvort skattstillingar sem byggja á staðsetningu eða viðskiptavinalykli. 

Hugsanlega viltu að rafræna viðskiptarásin styðji valkosti eins og sendingu eða afhendingu pantana á netinu. Notkun virðisaukaskatts miðast við val viðskiptavina þinna á netinu. 

## <a name="destination-based-taxes-for-online-orders"></a>Skattar sem byggja á staðsetningu fyrir pantanir á netinu

Almennt séð miðast skattar fyrir pantanir á netinu sem senda á heimilisföng viðskiptavinar við áfangastaðinn. Sérhver VSK-flokkur inniheldur skattaskilgreiningu miðað við áfangastað smásölu þar sem fyrirtækið þitt getur skilgreint upplýsingar um áfangastað, eins og hérað eða svæði, ríki, land og borg á stigveldisformi.

### <a name="orders-delivered-to-customer-address"></a>Pantanir afhentar á heimilisfang viðskiptavinar

Þegar pöntun á netinu berst notar Commerce-skattakerfið afhendingaraðsetur hvers línuatriðis pöntunarinnar og finnur VSK-flokka með samsvarandi skattaviðmið miðað við ákvörðunarstað. Þegar t.d. pöntun er gerð á netinu með afhendingaraðsetur línuatriðis í San Francisco Kaliforníu, finnur skattakerfið VSK-flokkinn og VSK-kóðann fyrir Kaliforníu og reiknar síðan út skattinn fyrir hvert línuatriði samkvæmt því.

### <a name="order-pick-up-in-store"></a>Pöntun sótt í verslun

Þegar pöntun er skilgreind í pöntunarlínu sem sótt í verslun eða afhent í bíl, verður notaður skattflokkur verslunarinnar þar sem pöntunin er sótt. Frekari upplýsingar um hvernig á að setja upp virðisaukaskatta fyrir tilgreinda verslun er að finna í [Stilla aðra skattvalkosti fyrir verslanir](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

## <a name="customer-account-based-taxes-for-online-orders"></a>Skattar sem byggja á viðskiptavinalykli fyrir pantanir á netinu

Upp geta komið viðskiptaaðstæður þar sem þú vilt skilgreina VSK-flokk fyrir tiltekinn viðskiptavinalykil í Commerce Headquarters. Það eru tveir staðir í höfuðstöðvum þar sem hægt er að skilgreina virðisaukaskatt fyrir viðskiptavinalykil. Til að fá aðgang að þeim þarf fyrst að fara á upplýsingasíðu viðskiptavinar með því að fara í **Smásala og viðskipti \> Viðskiptavinir \> Allir viðskiptavinir** og síðan velja viðskiptavin.

Staðirnir tveir þar sem virðisaukaskattur er skilgreindur fyrir viðskiptavinalykil eru:

- **VSK-flokkur** í flýtiflipanum **Reikningur og afhending** á upplýsingasíðu viðskiptavinar. 
- **Virðisaukaskattur** í flýtiflipanum **Almennt** á síðunni **Stjórna aðsetrum**. Til að komast þangað frá upplýsingasíðu viðskiptavinar skal velja tiltekið aðsetur undir flýtiflipanum **Aðsetur** og síðan velja **Ítarlegt**.

> [!TIP]
> Fyrir pantanir viðskiptavinar á netinu, ef ætlunin er að nota aðeins skatta sem byggja á staðsetningu og forðast skatta sem byggja á viðskiptavinalykli, skal ganga úr skugga um að reiturinn **VSK-flokkur** sé auður í flýtiflipanum **Reikningur og afhending** á upplýsingasíðu viðskiptavinar. Til að tryggja að nýir viðskiptavinir sem skrá sig með netrásinni erfi ekki stillingar VSK-flokksins frá sjálfgefnum stillingum viðskiptavinar eða viðskiptavinaflokks skal tryggja að reiturinn **VSK-flokkur** sé auður fyrir sjálfgefnar stillingar viðskiptavinar og stillingar viðskiptavinaflokks í netrásinni (**Smásala og viðskipti \> Viðskiptavinir \> Viðskiptavinaflokkar**).

## <a name="determine-destination-based-tax-or-customer-account-based-tax-applicability"></a>Skera úr um hvort skattur sem byggir á staðsetningu eða skattur sem byggir á viðskiptavinalykli eigi við 

Eftirfarandi tafla útskýrir hvort skattar sem byggja á staðsetningu eða skattar sem byggja á viðskiptavinalykli séu notaðir fyrir pantanir á netinu. 

| Gerð viðskiptavinar | Heimilisfang viðtakanda                   | Viðskiptavinur > Reikningur og afhending > VSK-flokkur? | Aðsetur í viðskiptavinalykli í höfuðstöðvum? | Aðsetur viðskiptavinar > Ítarlegt > Almennt > VSK-flokkur?                                              | VSK-flokkur notaður      |
|---------------|------------------------------------|-----------------------------------------------------|-----------------------------------|--------------------------------------------------------------------------------------------------------|------------------------------|
| Gestur         | Manhattan, NY                      | Nei (autt)                                                | Nei (autt)                              | Nei (autt)                                                                                                   | NY (svæðisháðir skattar) |
| Innskráð     | Austin, TX                          | Nei (autt)                                             | Já                               | Engum<br/><br/>Nýju aðsetri bætt við í gegnum netrás.                                                            | TX (svæðisháðir skattar) |
| Innskráð     | San Francisco, CA (sækja í verslun) | Já (NY)                                            | Ekki tiltækt                              | Ekki tiltækt                                                                                                    | CA (svæðisháðir skattar) |
| Innskráð     | Houston, TX                         | Já (NY)                                            | Já                               | Já (NY)<br/><br/>Nýju aðsetri bætt við í gegnum netrás og VSK-flokkur erfður frá viðskiptavinalykli. | NY (skattar byggðir á viðskiptavinalykli)  |
| Innskráð     | Austin, TX                          | Já (NY)                                            | Já                               | Já (NY)<br/><br/>Nýju aðsetri bætt við í gegnum netrás og VSK-flokkur erfður frá viðskiptavinalykli. | NY (skattar byggðir á viðskiptavinalykli)  |
| Innskráð     | Sarasota, FL                       | Já (NY)                                            | Já                               | Já (WA)<br/><br/>Stillta handvirkt á WA.                                                                          | WA (skattar byggðir á viðskiptavinalykli)  |
| Innskráð     | Sarasota, FL                       | Nei (autt)                                                | Já                               | Já (WA)<br/><br/>Stillta handvirkt á WA.                                                                          | WA (skattar byggðir á viðskiptavinalykli)  |

## <a name="additional-resources"></a>Frekari upplýsingar

[Setja upp skatta fyrir netverslanir á grundvelli áfangastaðar](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination)

[Yfirlit virðisaukaskatts](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[Útreikningsaðferðir VSK í upprunareitnum](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[ Úthlutun og hnekking virðisaukaskatts](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[Valkostir heildarupphæðar og tímabilsútreikninga fyrir VSK-kóða](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[Reikna út skattundanþágu](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
