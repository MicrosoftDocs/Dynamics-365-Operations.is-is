---
title: Rafræn skilaboð
description: Þetta efnisatriði veitir yfirlit og upplýsingar um uppsetningu fyrir rafræn skilaboð í Microsoft Dynamics 365 Finance.
author: liza-golub
ms.date: 06/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: elgolu
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 339e0c811a70ca6b722d8967c2df103500578664
ms.sourcegitcommit: 73d320d2103f2b0c6ecbb2b9df746469bc544ea2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/07/2021
ms.locfileid: "6433720"
---
# <a name="electronic-messaging"></a>Rafræn skilaboð

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er að finna yfirlit og upplýsingar um uppsetningu fyrir virknina **Rafræn skilaboð** (EM).

Ríkisstjórnir og löggjafarvald í hinum ýmsu löndum og svæðum um allan heim hafa nýlega innleitt skýrslukröfur fyrir fyrirtæki sem eru skráð í þessum löndum og svæðum. Tilgangur kröfunnar er að gera það mögulegt að fá gögn frá þessum fyrirtækjum á rafrænu formi, beint frá kerfinu þar sem þau voru skráð, vistuð og unnin.

Virknin fyrir rafræn skilaboð í Microsoft Dynamics 365 Finance styður ýmsa ferla rafrænnar samaðgerðar milli Finance og kerfanna sem ríkisstjórnir og löggjafarvald bjóða upp á hvað varðar skýrslugerð, afhendingu og móttöku á opinberum upplýsingum.

Virknin fyrir rafræn skilaboð er samþætt við eininguna **Rafræn skýrslugerð**. Hægt er að setja upp snið rafrænnar skýrslugerðar fyrir rafræn skilaboð. Frekari upplýsingar eru í [Rafræn skýrslugerð](/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting).

## <a name="basic-concepts-for-em-functionality"></a>Grunnhugtök fyrir virkni rafrænna skilaboða

Virkni rafrænna skilaboða byggir á eftirfarandi einingum:

- **Rafræn skilaboð** – Skýrsla eða yfirlýsing sem ætti að tilkynna eða senda innanhúss, svo sem skýrsla sem er send skattstofu.
- **Atriði rafrænna skilaboða** – Færslur sem ber að hafa með í skilaboðunum sem eru skráð.
- **Úrvinnsla rafrænna skilaboða** – Röð aðgerða sem ber að keyra til að safna saman nauðsynlegum gögnum, búa til skýrslur, vista gögn í Azure Blob-geymslu, flytja skýrslur út fyrir kerfið, fá viðbrögð utan kerfis og, á grundvelli móttekinna upplýsinga, uppfæra gagnagrunninn. Aðgerðirnar í röðinni geta verið tengdar eða ótengdar.

Eftirfarandi skýringarmynd sýnir flæði gagna fyrir rafræn skilaboð.

![Gagnaflæði rafrænna skilaboða.](media/electronic-messaging-data-flow.png)

## <a name="scenarios-supported-by-the-em-functionality"></a>Aðstæður studdar af virkni rafrænna skilaboða

Virkni rafrænna skilaboða styður eftirfarandi aðstæður:

- Búa til skilaboð og gera skýrslur handvirkt sem byggjast á útflutningstengdum sniðum rafrænnar skýrslugerðar af ýmsum gerðum. Þessar gerðir eru m.a. Microsoft Excel, XML, JavaScript Object Notation (JSON), PDF, texti og fleira Microsoft Word.
- Stofna og vinna úr skilaboðum sjálfvirkt sem tengjast upplýsingum sem óskað var eftir og voru fengin frá yfirvöldum með því að nota útflutningstengt snið rafrænnar skýrslugerðar.
- Safna og vinna úr upplýsingum úr gagnaveitu sem skilaboðaatriði. Gagnagjafinn tafla í Finance.
- Geyma viðbótarupplýsingar og meta ýmis gildi með því að kalla á sérstaklega skilgreinda keyranlega klasa í tengslum við skilaboð eða skilaboðaatriði.
- Safna saman upplýsingum sem eru fengin í skilaboðaatriðum, skipta þeim upplýsingum eftir skilaboðum, og búa til skýrslur sem eru á útflutningstengdum sniðum rafrænnar skýrslugerðar.
- Senda skýrslurnar sem eru búnar til á vefþjónustu með því að nota öryggisupplýsingar sem eru geymdar í Azure-lyklageymslunni.
- Fá svar frá vefþjónustu, túlka svarið og uppfæra gögn í Finance, eftir því sem við á.
- Geyma og yfirfara allar skýrslur sem eru búnar til.
- Geyma og yfirfara allar kladdaupplýsingar sem tengjast aðgerðum sem eru keyrðar fyrir skilaboð eða skilaboðaatriði.
- Stjórna vinnslu í gegnum ýmsar stöður skilaboða og skilaboðaatriða.

## <a name="country-specific-regulatory-features-supported-by-the-em-functionality"></a>Eftirlitseiginleikar ákveðins lands studdar af virkni rafrænna skilaboða

Í eftirfarandi töflu eru upplýsingar um eftirlitseiginleika tiltekins lands sem eru studdir af virkni rafrænna skilaboða.

| Land     | Heiti eiginleika | Skráning á sýniútgáfu eiginleika |
|-------------|--------------|------------------------|
| Spánn       | [Tafarlaus afhending upplýsinga um VSK (Suministro Inmediato de Información del IVA, SII)](../localizations/emea-esp-sii.md) | |
| Ungverjaland     | [Reikningsfærslukerfi á netinu](../localizations/emea-hun-online-invoicing.md) | |
| Bretland | [Skattur gerður stafrænn (MTD) – Innsending VSK-yfirlits](../localizations/emea-gbr-mtd-vat-integration.md) | [Finance and Operations: UK Digital Tax - VSK-skýrsla í Dynamics 365](https://community.dynamics.com/365/b/techtalks/posts/finance-and-operations-uk-digital-tax-vat-declaration-in-dynamics-365) |
| Litháen   | [i.SAF skýrslugerð](../localizations/emea-ltu-isaf.md) | |
| Pólland      | [VSK-skýrsla ásamt afgreiðslukössum (JPK_V7M, VDEK)](../localizations/emea-pol-vdek.md) | [Dynamics 365 Finance: SAF/JPK VSK-eftirlitsskrár](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-finance-saf-jpk-vat-audit-registers-june-4-2020) |
| Holland | [VSK-skýrsla fyrir Holland](../localizations/emea-nl-vat-declaration-netherlands.md) | |
| Tékkland | [VSK-skýrsla](../localizations/emea-cze-vat-declaration-tax-declaration-model.md) | |
| Brasilía      | [SPED-Reinf](../localizations/latam-bra-sped-reinf-overview.md) | |
| Rússland      | [VSK-skýrsla](../localizations/rus-vat-declaration.md) | |
| Rússland      | [Reikningsskýrslur á rafrænu formi](../localizations/rus-accounting-reporting.md) | |
| Rússland      | [Skattskýrsla fyrir skatt á hagnað](../localizations/rus-profit-tax-declaration.md) | |
| Rússland      | [Áætluð skattskýrsla](../localizations/rus-assessed-tax-declaration.md) | |
| Rússland      | [Flutningsskattsskýrsla](../localizations/rus-transport-tax-declaration.md) | |
| Rússland      | [Lóðarskattsskýrsla](../localizations/rus-land-tax-declaration.md) | |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

