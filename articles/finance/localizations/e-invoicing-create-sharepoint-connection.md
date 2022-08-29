---
title: Skilgreina SharePoint-tengingu
description: Þessi grein útskýrir hvernig á að stilla tengingu þannig að rafræn reikningur geti fengið aðgang að Microsoft SharePoint síða.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283988"
---
# <a name="configure-a-sharepoint-connection"></a>Skilgreina SharePoint-tengingu

[!include [banner](../includes/banner.md)]

Rafræn reikningaþjónusta getur lesið skrár frá Microsoft SharePoint möppur og hlaðið upp skrám í SharePoint. Til að tryggja að rafræn reikningur geti fengið aðgang að tilteknu SharePoint síðu, verður þú að gefa upp síðuskilríki til rafrænna reikningaþjónustunnar. Að auki, til að tryggja að skilríkin séu geymd á öruggan hátt, skaltu ekki veita þau beint. Í staðinn skaltu geyma þau í Azure lyklahólfinu og gefa upp Azure Key Vault leyndarmál.

## <a name="grant-access-to-a-sharepoint-folder"></a>Veita aðgang að a SharePoint möppu

1. Búðu til forritaskráningu í leigjandanum þar sem Regulatory Configuration Service (RCS) er uppsett.

    1. Skráðu þig inn á [Azure-gáttina](https://portal.azure.com/).
    2. Fara til **App skráningar**.
    3. Veljið **Ný skráning**.
    4. Sláðu inn nafn, svo sem **SharePoint App fyrir rafræna reikninga**, og kláraðu skráninguna
    5. Veldu nýju app skráninguna.
    6. Á **Auðkenning** flipann, virkjaðu **Leyfa flæði almennings viðskiptavina** valmöguleika.
    4. Á **Vottorð og leyndarmál** flipa, veldu **Nýtt leyndarmál viðskiptavinar** að búa til leyndarmál viðskiptavinar.
    5. Afritaðu gildi leyndarmálsins sem var búið til.

    Fylgdu þessum leiðbeiningum:

    - Ekki nota sömu forritaskráninguna fyrir mismunandi þjónustu.
    - Fylgdu [ráðleggingar um lykilorðastefnu](/microsoft-365/admin/misc/password-policy-recommendations?view=o365-worldwide).
    - Settu upp snúning lykilorða. Meðan á snúningi stendur skaltu búa til nýtt leyndarmál viðskiptavinar fyrir forritaskráninguna, uppfæra lyklahólfið og eyða síðan gamla leyndarmálinu.

2. Vistaðu **App Skráning leyndarmál** og **Auðkenni umsóknar (viðskiptavinar).** gildi sem tvö ný leyndarmál í lyklageymslunni í uppsetningu rafrænna reikningaumhverfisins þíns.
3. Bættu leyndarmálunum sem þú bjóst til við Key Vault færibreyturnar í uppsetningu rafrænna reikningaumhverfisins í RCS.
4. Í Azure gáttinni, veittu aðgang að SharePoint. Þetta skref ætti að vera lokið af leigjanda stjórnanda.

    1. Veldu forritaskráninguna sem þú bjóst til.
    2. Á **API heimildir** flipa, veldu **Bættu við heimild**.
    3. Veldu **Microsoft línurit (forritsheimildir)** \> **Síður.Valið**.
    4. Veldu **Veita samþykki stjórnanda fyrir \<user&nbsp;name\>**.
    5. Skoðaðu **Staða** reitinn til að ganga úr skugga um að heimildir séu veittar.

        ![Heimildir veittar á API heimildaflipanum.](media/configured-permissions.jpg)

    6. Opið [Graph Explorer - Microsoft Graph](https://developer.microsoft.com/graph/graph-explorer), og skráðu þig inn.
    7. Í vinstri glugganum, á **Dæmi um fyrirspurnir** flipi, undir **SharePoint Síður**, veldu **fá SharePoint síða byggt á hlutfallslegri slóð svæðisins**.
    8. Fylltu út í **\{ hýsil-nafn\}** og **\{ server-relative-path\}** breytur. Til dæmis, fylltu út`<domain>.sharepoint.com` fyrir **\{ hýsil-nafn\}** og`sites/<siteName>` fyrir **\{ server-relative-path \}**.

        > [!NOTE]
        > Fyrir sjálfgefna vefsíðu, farðu frá **\{ server-relative-path\}** færibreyta auð.

    9. Veldu **Keyra fyrirspurn**, og vistaðu niðurstöðuna.
    10. Stilltu eftirfarandi fyrirspurn.

        `POST https://graph.microsoft.com/v1.0/sites/{site-id}/permissions`

        Í þessari fyrirspurn, **\{ síða-auðkenni\}** er verðmæti **kt** hnút frá fyrra fyrirspurnarsvari.

        Hér er beiðnin.

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

        Í þessari beiðni, **\{ app-auðkenni\}** er **Auðkenni umsóknar (viðskiptavinar).** gildi, og **\{ app-nafn\}** er **Nafn umsóknar** gildi.

        ![POST fyrirspurn.](media/app-id-query.jpg)

    11. Á **Breyta heimildum** flipa, veldu **Opnaðu heimildaspjaldið**, og veldu síðan **Síður** \> **Sites.FullControl.All** \> **Samþykki**.
    12. Veldu **Keyra fyrirspurn**.

Rafræn reikningaþjónusta hefur nú aðgang að þínum SharePoint síða.
