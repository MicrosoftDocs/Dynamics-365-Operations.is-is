---
title: Opna vefslóð í POS
description: Þetta efnisatriði gefur yfirlit yfir úrbætur sem hafa verið gerðar á vöru og viðskiptahugbúnaði í Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 01/28/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.1.1
ms.openlocfilehash: 0e02a08e5afd15fd9622495fd77f4dc01b85786bcffc222b5c979c82a59a6aab
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6714115"
---
# <a name="open-url-in-pos"></a>Opna vefslóð í sölustað

[!include [banner](includes/banner.md)]

Þetta efnisatriði lýsir því hvernig hægt er að skilgreina hnapp í Dynamics 365 Commerce-sölustað (POS) til að opna vefslóð. Þessi eiginleiki krefst ekki sérstillingar á kóða og einhver sem ekki er í hlutverki þróunaraðila getur stillt hann. 

Þessi eiginleiki leyfir stillingu á hnapp í POS með hönnuði hnappahnits til að opna vefslóð. Sem stendur er þetta stutt í eftirfarandi stillingum:

- Opna í nýjum glugga.
- Opna innan POS.
- Opna native-forrit.

## <a name="open-in-new-window"></a>Opna í nýjum glugga

Þessi stilling skilgreinir hvort vefslóðin verði opnuð í nýjum glugga eða innan forritsins. Yfirlitssvæðið til hliðar og efsta slá POS eru sýnileg og í boði fyrir notandann þegar stillt er á að vefslóð verði opnuð í forriti. Vefslóðin opnast í nýjum glugga forrits í Modern POS fyrir Windows og í nýjum vafraglugga í öllum öðrum POS-biðlurum þegar stillt er á að nýr gluggi eigi að opnast. Til að virkja þetta verður að stilla vefslóðina með því að velja valkostinn **Opna í nýjum glugga**.

## <a name="open-within-pos"></a>Opna innan POS

Opnun vefslóðar innan POS er sem stendur aðeins stutt fyrir Modern POS í Windows. Á öðrum biðlurum er þessi möguleiki í þróun og áætlað er að gefa hann út í síðari uppfærslum. Til að virkja þetta verður að stilla vefslóðina með því að velja ekki valkostinn **Opna í nýjum glugga**.

## <a name="open-a-native-app"></a>Opna native-forrit

Þessi eiginleiki leyfir þér einnig að tilgreina slóðir sem ekki eru vefslóðir til að opna native-forrit. Til dæmis er hægt að tilgreina samskiptareglur slóðar, eins og MailTo, SIP, IM eða MSTEAMS, sem native-forrit á tæki hýsils getur síðan meðhöndlað. Til að virkja þetta verður að stilla vefslóðina með því að velja valkostinn **Opna í nýjum glugga**.

- Fyrir Windows-tölvur skal skoða [Flytja út eða flytja inn sjálfgefnar forritatengingar](/windows-hardware/manufacture/desktop/export-or-import-default-application-associations) til að stilla sjálfgefnar tengingar samskiptareglu ef verið er að setja upp tölvuna með DISM (meðhöndlun afritsmynda).
- Ef MDM er notað, t.d. Intune til að stjórna Windows-tölvunni, skal skoða [CSP-regla - ApplicationDefaults](/windows/client-management/mdm/policy-csp-applicationdefaults).
- Ef þú ert þróunaraðili að smíða sérsniðna vefsíðu skaltu skoða [Ræsa sjálfgefið forrit fyrir URI](/windows/uwp/launch-resume/launch-default-app).

## <a name="open-a-native-app-seamlessly"></a>Opna native-forrit án vandkvæða

Windows, iOS og Android leyfa einnig ræsingu forrita án vandkvæða, sem byggist á samskiptareglutengingu forrits. Ef forritið þitt er ekki þegar stillt til að meðhöndla ræsingu úr vafra, gæti verið að þu þurfir þróunaraðila til að stilla þetta.

- Fyrir Windows skal skoða [Virkja forrit fyrir vefsíður sem nota URI-forritarekla](/windows/uwp/launch-resume/web-to-app-linking).
- Fyrir iOS skal skoða [Altækir tenglar fyrir þróunaraðila](https://developer.apple.com/ios/universal-links/).
- Fyrir Android, sjá [Meðhöndlun Android forritatengla](https://developer.android.com/training/app-links/).

| Biðlari                | Opna í nýjum glugga | Opna native-forrit | Opna innan POS | Upplýsingar                           |
|-----------------------|--------------------|-----------------|-----------------|-----------------------------------|
| Modern POS í Windows | ✓\*                | ✓               | ✓              | \* Opnast í nýjum glugga Modern POS |
| Sölustaður í skýi             | ✓\*                | ✓               | X              | \* Opnast í nýjum vafraglugga        |
| Modern POS í iOS     | ✓\*                | ✓               | X              | \* Opnast í nýjum vafraglugga        |
| Modern POS í Android | ✓\*                | ✓               | X              | \* Opnast í nýjum vafraglugga        |

## <a name="before-you-begin"></a>Áður en hafist er handa

Áður en hafist er handa skal yfirfara hvernig á að stilla [Skjáútlit fyrir sölustað (POS)](pos-screen-layouts.md).

## <a name="open-url-in-pos"></a>Opna vefslóð í POS

Til að stilla vefslóð svo hún opnist í POS, skal framkvæma eftirfarandi skref.

1. Á aðalskrifstofu skal fara í **Retail og Commerce \> Uppsetning rásar \> Uppsetning sölustaðar \> Sölustaður \> Útlit afgreiðsluskjás**.
2. Veljið **Hnappahnit \> Hönnuður**.
3. Búið til nýjan hnapp.
4. Veljið eiginleikana **Hnappur**.
5. Veljið **Opna vefslóð** sem aðgerðina.
6. Færið inn vefslóðina sem á að nota.
7. Stillið hvort eigi að opna vefslóðina eða nýjan glugga.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
