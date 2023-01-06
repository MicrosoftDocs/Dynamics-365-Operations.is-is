---
title: Rafræn skilaboð
description: Þessi grein veitir yfirlit og upplýsingar um uppsetningu fyrir rafræn skilaboð í Microsoft Dynamics 365 Finance.
author: AdamTrukawka
ms.date: 01/04/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 3e2fe6a70d449adea07f5aa0db9e625f0378d8c2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283455"
---
# <a name="electronic-messaging"></a>Rafræn skilaboð

[!include [banner](../includes/banner.md)]

Í þessari grein er að finna yfirlit og upplýsingar um uppsetningu fyrir virknina **Rafræn skilaboð** (EM).

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

## <a name="security-privileges"></a>Öryggisréttindi

Eftirfarandi öryggisréttindi eru í boði fyrir rafræn skilaboð.

| Öryggisréttindi           | Aðgangsstig | Tengingar |
|------------------------------|--------------|-------------|
| Vinna með rafræn skilaboð | Þessi réttindi veita fullan aðgang að virkni rafrænna skilaboða. Ef þú ert með þessi réttindi getur þú sett upp rafræn skilaboð og keyrt alla úrvinnsluna. | Þessi réttindi eru innifalin í öryggisheimildinni **Vinna með VSK-færslur**. Sú aðgangsheimild er á móti einnig innifalin í öryggishlutverkinu **Bókhaldari**. |
| Skoða rafræn skilaboð     | Þessi réttindi veita skrifvarinn aðgang að virkni rafrænna skilaboða. Ef þú ert með þessi réttindi getur þú skoðað stillingar rafrænna skilaboða og skilaboð. Hins vegar er ekki hægt að setja upp eða keyra neitt. | Þessi réttindi eru innifalin í öryggisheimildinni **Spyrjast fyrir um stöðu VSK-færslu**. Sú aðgangsheimild er á móti einnig innifalin í eftirfarandi öryggishlutverkum:<ul><li>Innheimtustjóri</li><li>Starfsmaður viðskiptakrafa</li><li>Viðskiptakröfustjóri</li><li>Skattaendurskoðandi</li><li>Bókhaldari</li><li>Bókhaldsstjóri</li><li>Yfirmaður bókhalds</li><li>Sölustjóri</li><li>Afgreiðslumaður viðskiptaskulda</li></ul> |
| Keyra rafræn skilaboð  | Þessi réttindi veita aðeins aðgang að síðunum **Rafræn skilaboð** og **Rafræn skilaboðaatriði**. Ef þú ert með þessi réttindi getur þú keyrt alla úrvinnsluna sem kallað er á af þessum síðum. | Þessi réttindi eru innifalin í öryggisheimildinni **Stjórna rafrænum skilaboðum**. Sú aðgangsheimild er á móti einnig innifalin í öryggishlutverkinu **Stjórnandi rafrænna skilaboða**. |

## <a name="country-specific-regulatory-features-supported-by-the-em-functionality"></a>Eftirlitseiginleikar ákveðins lands studdar af virkni rafrænna skilaboða

Í eftirfarandi töflu eru upplýsingar um eftirlitseiginleika tiltekins lands sem eru studdir af virkni rafrænna skilaboða.

| Land     | Heiti eiginleika | Skráning á sýniútgáfu eiginleika |
|-------------|--------------|------------------------|
| Spánn       | [Tafarlaus afhending upplýsinga um VSK (Suministro Inmediato de Información del IVA, SII)](../localizations/emea-esp-sii.md) | |
| Ungverjaland     | [Reikningsfærslukerfi á netinu](../localizations/emea-hun-online-invoicing.md) | |
| Bretland | [Skattur gerður stafrænn (MTD) – Innsending VSK-yfirlits](../localizations/emea-gbr-mtd-vat-integration.md) | [Fjármál- og rekstur: UK Digital Tax - VSK-skýrsla í Dynamics 365](https://community.dynamics.com/365/b/techtalks/posts/finance-and-operations-uk-digital-tax-vat-declaration-in-dynamics-365) |
| Litháen   | [i.SAF skýrslugerð](../localizations/emea-ltu-isaf.md) | |
| Pólland      | [VSK-skýrsla ásamt afgreiðslukössum (JPK_V7M, VDEK)](../localizations/emea-pol-vdek.md) | [Dynamics 365 Finance: SAF/JPK VKS-eftirlitsskrár](https://community.dynamics.com/365/b/techtalks/posts/dynamics-365-finance-saf-jpk-vat-audit-registers-june-4-2020) |
| Holland | [VSK-skýrsla fyrir Holland](../localizations/emea-nl-vat-declaration-netherlands.md) | |
| Tékkland | [VSK-skýrsla](../localizations/emea-cze-vat-declaration-tax-declaration-model.md) | |
| Brasilía      | [SPED-Reinf](../localizations/latam-bra-sped-reinf-overview.md) | |
| Rússland      | [VSK-skýrsla](../localizations/rus-vat-declaration.md) | |
| Rússland      | [Reikningsskýrslur á rafrænu formi](../localizations/rus-accounting-reporting.md) | |
| Rússland      | [Skattskýrsla fyrir skatt á hagnað](../localizations/rus-profit-tax-declaration.md) | |
| Rússland      | [Áætluð skattskýrsla](../localizations/rus-assessed-tax-declaration.md) | |
| Rússland      | [Flutningsskattsskýrsla](../localizations/rus-transport-tax-declaration.md) | |
| Rússland      | [Lóðarskattsskýrsla](../localizations/rus-land-tax-declaration.md) | |
| Noregur      | [VSK-skilagrein með beinni innsendingu til Altinn](../localizations/emea-nor-vat-return.md) | [VSK-skilagrein með beinni innsendingu til Altinn í Dynamics 365 Finance](https://community.dynamics.com/365/dynamics-365-fasttrack/b/techtalks/posts/new-vat-return-with-direct-submission-to-altinn-in-dynamics-365-finance-december-1-2021) |
| Frakkland      | [VSK-skýrsla (Frakkland)](../localizations/emea-fra-VAT-declaration-preview-France.md) | |
| Austurríki     | [VSK-skýrsla (Austurríki)](../localizations/emea-aut-vat-declaration-austria.md) | |
| Þýskaland     | [VSK-skýrsla (Þýskaland)](../localizations/emea-deu-vat-declaration-germany.md) | |
| Holland | [VSK-skýrsla fyrir Holland](../localizations/emea-nl-vat-declaration-netherlands.md) | |
| Svíþjóð      | [VSK-skýrsla (Svíþjóð)](../localizations/emea-swe-VAT-declaration-Sweden.md) | |
| Sviss | [VSK-skýrsla (Sviss)](../localizations/emea-che-vat-declaration-switzerland.md) | |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]


