---
title: Byrjaðu með rafræna reikningaviðbótinni fyrir Frakkland
description: Þessi grein veitir upplýsingar sem hjálpa þér að byrja með rafræna reikningaviðbót fyrir Frakkland.
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
ms.openlocfilehash: 365316b204b6d76fa6ee6b2402fefee50c8ff3ef
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220715"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-france"></a>Byrjaðu með rafræna reikningaviðbótinni fyrir Frakkland

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Þessi grein veitir upplýsingar sem hjálpa þér að byrja með rafræna reikningagerð fyrir Frakkland. Það leiðir þig í gegnum stillingarskrefin sem eru háð landinu í Regulatory Configuration Service (RCS). Þessi skref eru viðbót við þau skref sem lýst er í [Byrjaðu með viðbótinni fyrir rafræna reikninga](e-invoicing-get-started.md).

## <a name="country-specific-configuration-for-french-chorus-pro-submission-fr-electronic-invoicing-feature"></a>Landssértæk uppsetning fyrir franska Chorus Pro uppgjöf (FR) Rafræn innheimtuaðgerð

Nokkur skref eru nauðsynleg til að stilla **French Chorus Pro uppgjöf (FR)** Rafræn innheimtuaðgerð. Sumar færibreytur úr uppsetningu eru birtar með sjálfgefnum gildum. Þessi gildi verður að endurskoða og uppfæra svo þau endurspegli betur rekstur þinn.

### <a name="prerequisites"></a>Forkröfur

Áður en þú byrjar aðgerðir í þessari grein skaltu ljúka eftirfarandi forsendum:

- Kynntu þér rafræna reikningagerð. Fyrir frekari upplýsingar, sjá [Yfirlit rafrænna reikninga](e-invoicing-service-overview.md).
- Skráðu þig í RCS og settu upp rafræna reikninga. Frekari upplýsingar er hægt að finna í eftirfarandi greinum:

    - [Skráðu þig í og settu upp rafræna reikningaþjónustu](e-invoicing-sign-up-install.md)
    - [Setja upp Azure-tilföng fyrir rafrænar reikningsfærslur](e-invoicing-set-up-azure-resources.md)
    - [Setja upp viðbót smáþjónustu í Lifecycle Services](e-invoicing-install-add-in-microservices-lcs.md)
    - [Virkjaðu og settu upp samþættingu við rafræna reikningagerð](e-invoicing-activate-setup-integration.md) – Notaðu upplýsingarnar í þessari grein til að virkja samþættingu þína Microsoft Dynamics 365 Fjármál eða Dynamics 365 Supply Chain Management app og rafræn reikningaþjónusta.
    - [NAF kóða og siret númer](emea-fra-naf-codes-siret-numbers.md) og [Settu upp NAF kóða og Siret númer](tasks/fr-00003-naf-codes-siret-numbers.md) – Notaðu upplýsingarnar í þessum greinum til að setja upp NAF kóða og Siret númer hjá lögaðilum þínum. 

- Stofnunin þín verður að vera skráð til að starfa með Chorus Pro. Microsoft veitir samþættingu við Chorus pro í OAuth2 ham í gegnum forritunarviðmót (API). Fyrir nákvæmar upplýsingar um Chorus Pro skráningu og virkjun forrita, sjáðu [opinber skjöl](https://communaute.chorus-pro.gouv.fr/documentation/help-for-api-developers-in-oauth2-mode/).

    Fylgdu þessum skrefum til að skrá þig hjá Chorus Pro.

    1. Farðu í [PISTE vefgátt](https://piste.gouv.fr/en/component/apiportal/registration) til að hefja skráningu þína. 
    2. Skráðu forrit og virkjaðu Open Authorization (OAuth) skilríki.
    3. Afritaðu og vistaðu auðkenni viðskiptavinarins fyrir OAuth skilríkin og leynilykilinn. Þú munt nota þessar upplýsingar í síðari skrefum.
    4. Farðu í [Chorus Pro vefgátt](https://portail.chorus-pro.gouv.fr/aife_csm/?id=aife_enrollment) að skrá. 
    5. Búðu til tæknilegan reikning fyrir API aðgang. Fyrir frekari upplýsingar, sjá [Stofnun tæknireiknings fyrir API aðgang í framleiðslu](https://communaute.chorus-pro.gouv.fr/documentation/creation-of-a-technical-account-for-an-api-access-in-production/).
    6. Afritaðu notandaauðkenni tæknireikningsins og lykilorðið. Þú munt nota þessar upplýsingar í síðari skrefum.

## <a name="country-specific-configuration-of-the-application-setup-for-the-french-chorus-pro-submission-fr-electronic-invoicing-feature"></a>Landssértæk uppsetning forritsuppsetningar fyrir franska Chorus Pro uppgjöf (FR) rafræna reikningseiginleika

Sumir af breytum frá **French Chorus Pro uppgjöf (FR)** eiginleikar rafrænna reikninga eru birtir með sjálfgefnum gildum. Áður en þú setur rafræna reikningseiginleikann í notkun í þjónustuumhverfinu skaltu endurskoða og uppfæra sjálfgefin gildi eftir þörfum, svo þau endurspegli betur rekstur þinn.

1. Í Azure lyklahvelfingunni skaltu búa til leyndarmál og samsvarandi tilvísun í þau. Fyrir frekari upplýsingar, sjá [Viðskiptavinavottorð og leyndarmál](e-invoicing-customer-certificates-secrets.md).
2. Flytja inn nýjustu útgáfuna af **French Chorus Pro uppgjöf (FR)** hnattvæðingareiginleika eins og lýst er í [Flytja inn eiginleika úr alþjóðlegu geymslunni](e-invoicing-import-feature-global-repository.md).
3. Búðu til afrit af innfluttum hnattvæðingareiginleikanum og veldu stillingaþjónustuna þína. Fyrir frekari upplýsingar, sjá [Búðu til hnattvæðingareiginleika](e-invoicing-create-new-globalization-feature.md).
4. Í flipanum **Útgáfa** skal staðfesta að útgáfan **Drög** sé valin.
5. Á **Uppsetningar** flipann, í hnitanetinu, veldu **UBL Sölureikningur fenginn** uppsetningu eiginleika.
6. Veldu **Breyta**, og síðan, á **Vinnsluleiðsla** flipa, í **Vinnsluleiðsla** kafla, veldu **(Forskoðun) Samþætta við French Chorus Pro** með nafni aðgerðarinnar **French Chorus Pro senda inn**.
7. Í **Færibreytur** kafla, í **Auðkenni viðskiptavinar leyndarmál** reit, veldu leyndarmálið sem þú bjóst til fyrir auðkenni viðskiptavinarins í lyklahólfinu.
8. Í **Leyndarmál viðskiptavinar** reit, veldu leyndarmálið sem þú bjóst til fyrir leyndarmál viðskiptavinar í lyklahólfinu.
9. Í **Leyndarheiti fyrir tæknilega innskráningu** reit, veldu leynda nafnið sem þú bjóst til fyrir tæknilega reikningsinnskráningu í lyklahólfinu.
10. Í **Leyndarheiti fyrir tæknilegt lykilorð** reit, veldu leyndarmálið sem þú bjóst til fyrir lykilorð tæknireikningsins í lyklahólfinu.
11. Á **Vinnsluleiðsla** flipa, í **Vinnsluleiðsla** kafla, veldu **Samþætta við French Chorus Pro** með nafni aðgerðarinnar **Staða beiðni um French Chorus Pro**.
12. Í **Færibreytur** kafla, í **Auðkenni viðskiptavinar leyndarmál** reit, veldu leyndarmálið sem þú bjóst til fyrir auðkenni viðskiptavinarins í lyklahólfinu.
13. Í **Leyndarmál viðskiptavinar** reit, veldu leyndarmálið sem þú bjóst til fyrir leyndarmál viðskiptavinar í lyklahólfinu.
14. Í **Leyndarheiti fyrir tæknilega innskráningu** reit, veldu leynda nafnið sem þú bjóst til fyrir tæknilega reikningsinnskráningu í lyklahólfinu.
15. Í **Leyndarheiti fyrir tæknilegt lykilorð** reit, veldu leyndarmálið sem þú bjóst til fyrir lykilorð tæknireikningsins í lyklahólfinu.
16. Veljið **Vista** og lokið síðan skjámyndinni.
17. Endurtaktu skref 6 til 16 fyrir **UBL Verkefnareikningur fenginn** uppsetning eiginleika, **UBL sölukreditnóta fengin** eiginleikauppsetning, og **UBL Project Credit Note fengin** uppsetningu eiginleika.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit innbótar rafrænna reikninga](e-invoicing-service-overview.md)
- [Hafist handa með viðbót rafrænna reikninga fyrir Brasilíu](e-invoicing-get-started-service-administration.md)
- [Hafist handa með innbót rafrænna reikninga](e-invoicing-get-started.md)
