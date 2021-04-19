---
title: Skilgreina söluskatt fyrir pantanir á netinu
description: Þetta efnisatriði veitir yfirlit yfir val á VSK-flokki fyrir mismunandi gerðir pantana á netinu í Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 11/16/2020
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
ms.openlocfilehash: 68b7e59a1e1ea18bdcd4e7a9117e4892407f40ff
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791848"
---
# <a name="configure-sales-tax-for-online-orders"></a>Skilgreina söluskatt fyrir pantanir á netinu

[!include [banner](includes/banner.md)]

Þetta efnisatriði veitir yfirlit yfir val á VSK-flokki fyrir mismunandi gerðir pantana á netinu. 

Hugsanlega skal e-Commerce-rásin styðja valkosti eins og sendingu eða afhendingu pantana á netinu. Notkun virðisaukaskatts miðast við val notenda þinna á netinu. Þegar viðskiptavinur vefsvæðis kýs að kaupa vöru á netinu og fær hana senda á heimilisfang, miðast virðisaukaskatturinn við VSK-flokk heimilisfangs viðtakanda viðskiptavinarins. Þegar viðskiptavinur ákveður að sækja keypta vöru í verslun miðast virðisaukaskattur við VSK-flokk verslunarinnar þar sem varan er sótt. 

## <a name="orders-shipped-to-a-customer-address"></a>Pantanir sendar á heimilisfang viðskiptavinar 

Almennt séð miðast skattar fyrir pantanir á netinu sem senda á heimilisföng viðskiptavinar við áfangastaðinn. Sérhver VSK-flokkur inniheldur skattaskilgreiningu miðað við áfangastað smásölu þar sem fyrirtækið þitt getur skilgreint upplýsingar um áfangastað, eins og hérað/svæði, ríki, land og borg á stigveldisformi. Þegar pöntun á netinu berst notar Commerce-skattakerfið afhendingaraðsetur hvers línuatriðis pöntunarinnar og finnur VSK-flokka með samsvarandi skattaviðmið miðað við ákvörðunarstað. Þegar t.d. pöntun er gerð á netinu með afhendingaraðsetur línuatriðis í San Francisco Kaliforníu, finnur skattakerfið VSK-flokkinn og VSK-kóðann fyrir Kaliforníu og reiknar síðan út skattinn fyrir hvert línuatriði samkvæmt því.  

## <a name="customer-based-tax-groups"></a>Skattflokkar miðað við viðskiptavin

Hægt er að grunnstilla skattflokka viðskiptavinar á tveimur stöðum í Commerce Headquarters:

- **Prófíll viðskiptavinar**
- **Heimilisfang viðtakanda viðskiptavinar**

### <a name="if-a-customers-profile-has-a-tax-group-configured"></a>Þegar skattflokkur er grunnstilltur í prófíl viðskiptavinar

Hugsanlega er skattaflokkur grunnstilltur fyrir færslu í prófíl viðskiptavinar í Commerce Headquarters, hins vegar notar skattakerfið ekki grunnstilltan skattaflokk í prófíl viðskiptavinarins fyrir pantanir á netinu. 

### <a name="if-a-customers-shipping-address-has-a-tax-group-configured"></a>Þegar skattflokkur er grunnstilltur í heimilisfangi viðtakanda viðskiptavinar

Þegar aðsetursfærsla viðskiptavinar er með grunnstilltan skattflokk og pöntun á netinu (eða línuatriði) er sent til heimilisfangs viðtakanda viðskiptavinar, notar skattakerfið grunnstillta skattflokkinn í aðsetursfærslunni við skattaútreikninga.

#### <a name="configure-a-tax-group-for-a-customers-shipping-address-record"></a>Skilgreina skattflokk fyrir aðsetursfærslu viðskiptavinar

Fylgdu eftirfarandi skrefum til að grunnstilla skattflokk fyrir aðsetursfærslu viðskiptavinar í Commerce Headquarters.

1. Opnaðu **Allir viðskiptavinir** og smelltu síðan á viðkomandi viðskiptavin. 
1. Á flýtiflipanum **Heimilisföng** er viðkomandi heimilisfang valið og síðan er smellt á **Fleiri valkostir \> Ítarlegt**. 
1. Á flipanum **Almennt** á síðunni **Stjórna heimilisföngum** skal stilla VSK-gildið eftir þörfum.

> [!NOTE]
> Skattflokkurinn er skilgreindur með því að nota afhendingaraðsetur pöntunarlínunnar og skattar miðað áfangastað eru grunnstilltir í skattflokknum sjálfum. Frekari upplýsingar er að finna í [Setja upp skatta fyrir netverslanir á grundvelli áfangastaðar](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-taxes-for-online-stores-based-on-destination).

## <a name="order-pickup-in-store"></a>Pöntun sótt í verslun

Þegar pöntun er skilgreind í pöntunarlínu sem sótt í verslun eða afhent í bíl, verður notaður skattflokkur verslunarinnar þar sem pöntunin er sótt. Frekari upplýsingar um hvernig skal grunnstilla skattflokk fyrir tiltekna verslun er að finna í [Stilla aðra skattvalkosti fyrir verslanir](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-other-tax-options-for-stores).

> [!NOTE]
> Þegar pöntunarlína er grunnstillt sem sótt í verslun eru skattstillingar heimilisfangs viðskiptavinar (ef slíkar eru grunnstilltar) hunsaðar af skattkerfinu og notuð verður skattaskilgreining verslunarinnar þar sem pöntunin er sótt. 

## <a name="additional-resources"></a>Frekari upplýsingar

[Yfirlit virðisaukaskatts](https://docs.microsoft.com/dynamics365/finance/general-ledger/indirect-taxes-overview?toc=/dynamics365/commerce/toc.json) 

[Útreikningsaðferðir VSK í upprunareitnum](https://docs.microsoft.com/dynamics365/finance/general-ledger/sales-tax-calculation-methods-origin-field?toc=/dynamics365/commerce/toc.json) 

[ Úthlutun og hnekking virðisaukaskatts](https://docs.microsoft.com/dynamics365/supply-chain/procurement/tasks/sales-tax-assignment-overrides?toc=/dynamics365/commerce/toc.json) 

[Valkostir heildarupphæðar og tímabilsútreikninga fyrir VSK-kóða](https://docs.microsoft.com/dynamics365/finance/general-ledger/whole-amount-interval-options-sales-tax-codes?toc=/dynamics365/commerce/toc.json) 

[Reikna út skattundanþágu](tax-exempt-price-inclusive.md) 



[!INCLUDE[footer-include](../includes/footer-banner.md)]