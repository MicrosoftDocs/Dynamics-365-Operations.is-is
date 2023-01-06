---
title: Skilgreina SharePoint-tengingu
description: Í þessari grein er útskýrt hvernig á að skilgreina tengingu þannig að rafræn reikningsfærsla geti fengið aðgang að Microsoft SharePoint svæði.
author: gionoder
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: a2762178686d1f29c457b6de2a9b052fd048484b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283988"
---
# <a name="configure-a-sharepoint-connection"></a>Skilgreina SharePoint-tengingu

[!include [banner](../includes/banner.md)]

Rafræna reikningaþjónustan getur lesið skrár úr Microsoft SharePoint möppum og hlaðið inn skrám í SharePoint. Til að tryggja að rafrænir reikningar fái aðgang að tilteknu SharePoint svæði þarf að gefa upp innskráningarupplýsingar svæðisins í rafrænni reikningsfærsluþjónustu. Auk þess skal ekki gefa innskráningarupplýsingarnar beint upp til að tryggja að þær séu geymdar á öruggan hátt. Í staðinn skal geyma þær í Azure-lyklageymslu og gefa upp leynilykil Azure-lyklageymslu.

## <a name="grant-access-to-a-sharepoint-folder"></a>Heimila aðgang að SharePoint möppu

1. Búðu til forritsskráningu í leigjandanum þar sem Regulatory Configuration Service (RCS) er uppsett.

    1. Skráðu þig inn á [Azure-gáttina](https://portal.azure.com/).
    2. Farðu í **Skráning forrits**.
    3. Veljið **Ný skráning**.
    4. Færðu inn heiti eins og **SharePoint forrit fyrir rafræna reikningsfærslu** og ljúktu við skráninguna.
    5. Veldu nýju forritsskráninguna.
    6. Í flipanum **Sannvottun** skal virkja valkostinn **Leyfa flæði opins biðlara**.
    4. Á flipanum **Vottorð og leynilyklar** skaltu velja **Veljið Nýtt leyniorð biðlara** til að búa til leyninúmer biðlara.
    5. Afritaðu gildið á leynilyklinum sem var búið til.

    Fylgdu þessum leiðbeiningum:

    - Ekki nota sömu forritsskráninguna fyrir mismunandi þjónustur.
    - Fylgdu [ráðleggingum aðgangsorðareglu](/microsoft-365/admin/misc/password-policy-recommendations?view=o365-worldwide).
    - Settu upp endurnýjun lykilorða. Meðan á snúningi stendur skal búa til nýja leynilykil fyrir forritsskráninguna, uppfæra lyklageymsluna og síðan eyða gamla leynilyklinum.

2. Vistaðu gildin **Leynilykill forritsskráningar** og **Auðkenni forrits (biðlara)** sem tvo nýja leynilykla í lyklageymslunni í uppsetningu á umhverfi rafrænnar reikningsfærslu.
3. Bættu leynilyklum sem þú bjóst til við færibreytur lyklageymslunnar í uppsetningu á umhverfi rafrænnar reikningsfærslu í RCS.
4. Í Azure-gáttinni skal veita aðgang að SharePoint. Stjórnandi leigjanda á að ljúka þessu skrefi.

    1. Veldu forritsskráninguna sem var búin til.
    2. Í flipanum **API-heimildir** skal velja **Bæta við heimild**.
    3. Veldu **Microsoft Graph (forritsheimildir)** \> **Sites.Selected**.
    4. Veljið **Veita samþykki kerfisstjóra fyrir \<user&nbsp;name\>**.
    5. Farðu yfir reitinn **Staða** til að ganga úr skugga um að heimildirnar séu veittar.

        ![Heimildir veittar á API-heimildaflipanum.](media/configured-permissions.jpg)

    6. Opnaðu [Graph Explorer - Microsoft Graph](https://developer.microsoft.com/graph/graph-explorer) og skráðu þig inn.
    7. Á vinstra svæðinu í flipanum **Dæmi um fyrirspurnir** undir **SharePoint svæði** skal velja **fá SharePoint svæði samkvæmt tengdri slóð svæðisins**.
    8. Fylltu út færibreyturnar **\{hýsilheit\}** og **\{tengda slóð þjóns\}**. Fylltu til dæmis út `<domain>.sharepoint.com` fyrir **\{hýsilheiti\}** og `sites/<siteName>` fyrir **\{tengda slóð þjóns\}**.

        > [!NOTE]
        > Fyrir sjálfgefið vefsvæði skal skilja færibreytuna **\{tengd slóð þjóns\}** eftir auða.

    9. Veldu **Keyra fyrirspurn** og vistaðu niðurstöðuna.
    10. Skilgreindu eftirfarandi fyrirspurn.

        `POST https://graph.microsoft.com/v1.0/sites/{site-id}/permissions`

        Í þessari fyrirspurn er **\{svæðiskennið\}** gildið á hnútnum **kenni** úr fyrra svari fyrirspurnar.

        Hér er meginmál beiðninnar.

        ```json
        {
            "roles": [
                "read",
                "write"
            ],
            "grantedToIdentities": [
                {
                    "application": {
                        "id": "{app-id}",
                        "displayName": "{app-name}"
                    }
                }
            ]
        }
        ```

        Í þessu meginmáli beiðninnar er **\{forritskenni\}** gildið **Auðkenni forrits (biðlara)** og **\{forritsheiti\}** er gildið **Heiti forrits**.

        ![POST fyrirspurn.](media/app-id-query.jpg)

    11. Í flipanum **Breyta heimildum** skal velja **Opna heimildasvæðið** og síðan velja **Svæði** \> **Sites.FullControl.All** \> **Samþykki**.
    12. Veldu **Keyra fyrirspurn**.

Rafræna reikningaþjónustan hefur nú aðgang að SharePoint vefsvæðinu þínu.
