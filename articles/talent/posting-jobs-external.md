---
title: Auglýsa störf á utanaðkomandi ráðningarsíðum úr Attract
description: Þetta efnisatriði útskýrir hvernig á að nota Dynamics 365 for Talent - Attract til að auglýsa störf á utanaðkomandi ráðningarsíðum
author: pganapmsft
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-03-19
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: eca599ad189edae29ef2de496196b08799a5e745
ms.sourcegitcommit: 1653d1e28d02f8a9a4bea8df562ac98d7a350ed1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/15/2019
ms.locfileid: "993669"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a>Auglýsa störf á utanaðkomandi ráðningarsíðum úr Attract

[!include [banner](../includes/banner.md)]

Þú vilt að sem flestir hæfir umsækjendur sjái lausu stöðurnar þínar. Ráðningarsíður á borð við Broadbean auðvelda þér að ná þessu markmiði. Microsoft Dynamics 365 Talent: Attract gerir þér nú kleift að auglýsa störf á Broadbean og Microsoft er stöðugt að bjóða upp á nýjar leiðir í þessum efnum.

## <a name="post-jobs-to-broadbean"></a>Auglýsa störf á Broadbean

Áður en þú getur auglýst störf á Broadbean þarf fyrst að stilla Broadbean-samþættinguna.

> [!NOTE]
> - Til að auglýsa störf á utanaðkomandi síðum verður þú að hafa [Viðbót við alhliða ráðningar](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).
> - Þessi eiginleiki er í forútgáfu sem stendur. Ef þú vilt prófa hann verður þú að [kveikja á honum í stjórnandastillingum Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).

### <a name="configure-broadbean-integration"></a>Skilgreina Broadbean-samþættingu

1. Skráðu þig inn í Attract sem stjórnandi.
2. Veldu hnappinn **Stillingar** (gírtáknið) efst í hægra horni síðunnar og veldu síðan **Stjórnandamiðstöð**.
3. Í flipanum **Stillingar atvinnutorgs**, í hlutanum **Virkja Broadbean-samþættingu** skal kveikja á samþættingunni.
4. Hafðu samband við Broadbean og færðu inn upplýsingarnar í **Notandanafn, auðkenni notanda, dulritunarlykill**.

> [!WARNING]
> Broadbean-aðgangsupplýsingarnar þínar eru viðkvæmar og trúnaðarmál. Þar af leiðandi skaltu geyma og deila þeim af varkárni. Hver sá sem gegnir stjórnandahlutverki í Attract getur skoðað þessar aðgangsupplýsingar.

> [!NOTE]
> Microsoft og Attract taka engan þátt í að búa til og viðhalda þessum gildum. Það er á þína ábyrgð að halda þeim uppfærðum í Attract og vinna með Broadbean til að leysa úr öllum vandamálum sem hafa með aðgangsupplýsingarnar þínar að gera.

### <a name="post-a-job-to-broadbean"></a>Auglýsa starf á Broadbean

Eftir að kveikt hefur verið á Broadbean geta ráðningaraðilar og stjórnendur birt störf þar. Þú verður að hafa umsóknarvefslóð fyrir starfið.

1. Í Attract, opnaðu starfið sem þú vilt auglýsa á Broadbean.
2. Í hlutanum **Birtingar** skal velja hnappinn **Birta núna** sem á við um Broadbean.
3. Fylgdu leiðbeiningunum í Broadbean-glugganum.

Attract sendir eftirfarandi upplýsingar til Broadbean:

- Beiðnikenni
- Starfsheiti
- Lýsing vinnslu
- Staðsetning starfs
- Sækja um vefslóðin
- Upplýsingar um ráðningaraðila

Eftir að Broadbean lýkur við birtinguna sýnir hlutinn **Birtingar** fyrir starfið í Attract stöðuna á Broadbean sem **Birt**.

> [!NOTE]
> - Broadbean þarf á reitnum **Atvinnugrein** að halda. Sem stendur er þessi reitur sjálfkrafa stilltur á **Upplýsingatækni**. Hins vegar er hægt að breyta gildinu í rétta atvinnugrein í glugganum fyrir birtingar á störfum í Broadbean.
> - Það tekur smá tíma fyrir Broadbean að birta starfið þitt á öllum atvinnutorgum sem þú hefur valið. Því kunna að vera smá tafir áður en Attract birtir uppfærslu á stöðu fyrir starfið.

### <a name="view-a-broadbean-job-posting"></a>Skoða auglýst starf á Broadbean

Eftir að starf er auglýst á Broadbean er hægt að skoða það í Attract.

1. Opnaðu starfið í Attract sem þú vilt skoða á Broadbean.
2. Í hlutanum **Birtingar** skal velja þrípunktahnappinn (**...**) sem á við um Broadbean og velja því næst **Skoða**.

Starfsauglýsingin í Broadbean birtist í nýjum glugga.

### <a name="update-a-broadbean-job-posting"></a>Uppfæra starfsauglýsingu í Broadbean

Hægt er að uppfæra starfsauglýsingu í Broadbean á tvenna vegu.

1. Opnaðu starfið í Attract sem þú vilt uppfæra.
2. Í hlutanum **Birtingar** skal velja hnappinn **Uppfæra auglýsingu** sem á við um Broadbean.
3. Breyttu auglýsingunni í Broadbean-glugganum.

– eða –

1. Opnaðu starfið í Attract sem þú vilt skoða á Broadbean.
2. Í hlutanum **Birtingar** skal velja þrípunktahnappinn (**...**) sem á við um Broadbean og velja því næst **Skoða**.
3. Í Broadbean-glugganum skal breyta upplýsingum um starfið og síðan birta starfið aftur. Upplýsingar um starfið í Attract haldast óbreyttar.

### <a name="remove-a-broadbean-job-posting"></a>Fjarlægja starfsauglýsingu úr Broadbean

Hægt er að fjarlægja starfsauglýsingu úr Broadbean ef þess gerist þörf.

1. Opnaðu starfið í Attract sem þú vilt fjarlægja.
2. Í hlutanum **Birtingar** skal velja þrípunktahnappinn (**...**) sem á við um Broadbean og velja því næst **Fjarlægja auglýsingu**.

Eftir að Broadbean fjarlægir starfið verður Broadbean-atriðið í Attract með hnappinn **Birta núna**. Hnappurinn gefur til kynna að starfið hafi verið fjarlægt og hægt sé að birta það aftur.

### <a name="troubleshoot-the-broadbean-integration"></a>Úrræðaleita Broadbean-samþættinguna

Ef þú átt í vandræðum með að birta starf á Broadbean, reyndu þá þessi skref.

1. Staðfestu að aðgangsupplýsingarnar fyrir Broadbean sem þú slóst inn í Attract séu réttar og í gildi.
2. Ef upplýsingarnar eru enn í gildi og réttar skaltu hafa samband við [Notendaþjónusta Broadbean](https://www.broadbean.com/resources/support/).
3. Ef vandamálið er viðvarandi skaltu hafa samband við [Notendaþjónusta Microsoft](./talent-support.md).