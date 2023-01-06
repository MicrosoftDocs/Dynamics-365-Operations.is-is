---
title: Hafist handa með viðbót rafrænnar reikningsfærslu fyrir Frakkland
description: Í þessari grein er að finna upplýsingar sem hjálpa til við að komast af stað með viðbót rafrænnar reikningsfærslu fyrir Fraklland.
author: dkalyuzh
ms.date: 07/07/2022
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2022-00-02
ms.dyn365.ops.version: AX 10.0.29
ms.openlocfilehash: 3ac4af8c131e35d9a499d0d558c7cce1d4872b37
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573279"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-france"></a>Hafist handa með viðbót rafrænnar reikningsfærslu fyrir Frakkland

[!include [banner](../includes/banner.md)]

Í þessari grein er að finna upplýsingar sem hjálpa til við að komast af stað með viðbót rafrænnar reikningsfærslu fyrir Frakkland. Það leiðir notandann í gegnum grunnstillingarskrefin sem fara eftir hverju landi fyrir sig í Regulatory Configuration Services (RCS). Þessi skref eru viðbót við skrefin sem lýst er í [Hafist handa með innbót rafrænna reikninga](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-french-chorus-pro-submission-fr-electronic-invoicing-feature"></a>Landssértækar stillingar fyrir franskan eiginleika Chorus Pro-innsendingar (FR) rafrænnar reikningsfærslu

Sum skref eru nauðsynleg til að skilgreina rafrænan reikningsfærslueiginleika **Frönsk Chorus Pro-innsending (FR)**. Sumar færibreyturnar úr skilgreiningunni eru birtar með sjálfgefnum gildum. Þessi gildi verður að endurskoða og uppfæra svo að þau endurspegli betur rekstur fyrirtækisins.

### <a name="prerequisites"></a>Forkröfur

Áður en hægt er að hefja ferlið í þessari grein þarf að ljúka eftirfarandi skilyrði:

- Læra á rafræna reikningsfærslu. Frekari upplýsingar eru í [Yfirlit rafrænnar reikningsfærslu](e-invoicing-service-overview.md).
- Skráðu þig fyrir RCS og settu upp Rafræna reikninga. Frekari upplýsingar er hægt að finna í eftirfarandi greinum:

    - [Skráðu þig fyrir og settu upp þjónustu fyrir rafræna reikninga](e-invoicing-sign-up-install.md)
    - [Setja upp Azure-tilföng fyrir rafrænar reikningsfærslur](e-invoicing-set-up-azure-resources.md)
    - [Setja upp viðbót smáþjónustu í Lifecycle Services](e-invoicing-install-add-in-microservices-lcs.md)
    - [Virkjaðu og settu upp samþættingu við rafræna reikningsfærslu](e-invoicing-activate-setup-integration.md) – Notaðu upplýsingarnar í þessari grein til að virkja samþættingu milli forrits Microsoft Dynamics 365 Finance eða Dynamics 365 Supply Chain Management forritsins og þjónustu rafrænnar reikningsfærslu.
    - [NAF-kóðar og Siret-númer](emea-fra-naf-codes-siret-numbers.md) og [Setja upp NAF-kóða og Siret-númer](tasks/fr-00003-naf-codes-siret-numbers.md) – Notið upplýsingarnar í þessum greinum til að setja upp NAF-kóða og Siret-númer í lögaðilum. 

- Þú verður að skrá stofnunina/fyrirtækið til að virka með Chorus Pro. Microsoft veitir samþættingu við Chorus pro í OAuth2 Mode í gegnum forritaskil (API). Nánari upplýsingar um skráningu og virkjun á Chorus Pro er að finna í [opinberum fylgiskjölum](https://communaute.chorus-pro.gouv.fr/documentation/help-for-api-developers-in-oauth2-mode/).

    Fylgdu þessum skrefum til að skrá þig hjá Chorus Pro.

    1. Opnaðu [PISTE gáttina ](https://piste.gouv.fr/en/component/apiportal/registration) til að hefja skráningu. 
    2. Skráðu forrit, og virkjaðu OAuth (Open Authorization) skilríkin.
    3. Afritaðu og vistaðu biðlarakenni OAuth-auðkennis og leynilykilinn. Þessar upplýsingar verða notaðar í síðari skrefum.
    4. Opnaðu [Chorus Pro gáttina](https://portail.chorus-pro.gouv.fr/aife_csm/?id=aife_enrollment) til að skrá þig. 
    5. Stofna tæknireikning fyrir API-aðgang. Frekari upplýsingar er að finna í [Stofnun tæknilegs aðgangs fyrir API í framleiðslu](https://communaute.chorus-pro.gouv.fr/documentation/creation-of-a-technical-account-for-an-api-access-in-production/).
    6. Afritaðu kenni notandans af tæknilega reikningnum og lykilorðinu. Þessar upplýsingar verða notaðar í síðari skrefum.

## <a name="country-specific-configuration-of-the-application-setup-for-the-french-chorus-pro-submission-fr-electronic-invoicing-feature"></a>Landsbundin skilgreining forritsuppsetningar fyrir eiginleika rafrænnar reikningsfærslu fyrir franska Chorus Pro-innsendingu (FR)

Sumar færibreyturnar úr rafræna reikningsfærslueiginleikanum **Frönsk Chorus Pro-innsending (FR)** eru birtar með sjálfgefnum gildum. Farið yfir og uppfærið sjálfgefin gildin og svo þau endurspegli betur fyrirtækjareksturinn áður en rafræni reikningseiginleikinn er notaður í þjónustuumhverfinu.

1. Í Azure-lyklageymsluni skaltu búa til leynilykla og samsvarandi tilvísun til þeirra. Frekari upplýsingar er að finna í [Vottorð og leynilyklar viðskiptavina](e-invoicing-customer-certificates-secrets.md).
2. Flytja inn nýjustu útgáfu af altæka eiginleikans **Frönsk Chorus Pro-innsending (FR)** sem lýst er í [Flytja inn eiginleika úr altækri geymslu](e-invoicing-import-feature-global-repository.md).
3. Útbúðu afrit af innflutta altæka eiginleikanum og veldu skilgreiningarveitu. Nánari upplýsingar má finna í [Stofna altækan eiginleika](e-invoicing-create-new-globalization-feature.md).
4. Í flipanum **Útgáfa** skal staðfesta að útgáfan **Drög** sé valin.
5. Í flipanum **Uppsetningar**, í hnitanetinu, skal velja eiginleikauppsetningu **UBL-sölureikningur afleiddur**.
6. Veljið **Breyta** og því næst, á flipanum **Pípuvinnsla**, í hlutanum **Pípuvinnsla**, veljið **(Forútgáfa) Samþætta við franskt Chorus Pro** með aðgerðarheitinu **Franskt Chorus Pro**.
7. Í hlutanum **Færibreytur**, í reitnum **Leyniheiti biðlarakennis**, skaltu velja leyniheiti sem þú bjóst til fyrir biðlarakenni í lyklageymslunni.
8. Í svæðinu **Leyniheiti leyniorðs biðlara** skal velja leyniheitið sem þú bjóst til fyrir leyniorð biðlara í lyklageymslunni.
9. Í reitnum **Leyniheiti tæknilegrar innskráningar** skal velja leyniheitið sem þú bjóst til fyrir tæknilega innskráningu á reikning í lyklageymslunni.
10. Í reitnum **Leyniheiti tæknilegs aðgangsorðs** skaltu velja leyniheitið sem þú bjóst til fyrir tæknilegt aðgangsorð reiknings í lyklageymslunni.
11. Á flipanum **Pípuvinnsla**, í hlutanum **Pípuvinnsla**, veljið **Samþætta við franskt Chorus Pro** með aðgerðarheitinu **Beiðnistaða fyrir franskt Chorus Pro**.
12. Í hlutanum **Færibreytur**, í reitnum **Leyniheiti biðlarakennis**, skaltu velja leyniheiti sem þú bjóst til fyrir biðlarakenni í lyklageymslunni.
13. Í svæðinu **Leyniheiti leyniorðs biðlara** skal velja leyniheitið sem þú bjóst til fyrir leyniorð biðlara í lyklageymslunni.
14. Í reitnum **Leyniheiti tæknilegrar innskráningar** skal velja leyniheitið sem þú bjóst til fyrir tæknilega innskráningu á reikning í lyklageymslunni.
15. Í reitnum **Leyniheiti tæknilegs aðgangsorðs** skaltu velja leyniheitið sem þú bjóst til fyrir tæknilegt aðgangsorð reiknings í lyklageymslunni.
16. Veljið **Vista** og lokið síðan skjámyndinni.
17. Endurtakið skref 6 til 16 fyrir eiginleikauppsetninguna **UBL-verkreikningur afleiddur**, **UBL-sölukreditnóta afleidd** og **UBL-verkkreditnóta afleidd**.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit innbótar rafrænna reikninga](e-invoicing-service-overview.md)
- [Hafist handa með viðbót rafrænna reikninga fyrir Brasilíu](e-invoicing-get-started-service-administration.md)
- [Hafist handa með innbót rafrænna reikninga](e-invoicing-get-started.md)
