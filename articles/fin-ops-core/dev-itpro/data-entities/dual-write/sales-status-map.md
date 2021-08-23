---
title: Setja upp vörpun fyrir stöðudálka sölupöntunar
description: Þetta efnisatriði útskýrir hvernig setja á upp stöðudálka sölupöntunar fyrir tvískipt skrif.
author: dasani-madipalli
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: 6eafd9b14d02dec3455b73aeee1264629331a57b8ce760b7db6f6ddbaa7406b8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741655"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-columns"></a>Setja upp vörpun fyrir stöðudálka sölupöntunar

[!include [banner](../../includes/banner.md)]

Dálkarnir sem gefa til kynna stöðu sölupöntunar eru með mismunandi tölusetningargildum í Microsoft Dynamics 365 Supply Chain Management og Dynamics 365 Sales. Viðbótaruppsetning er nauðsynleg til að varpa þessum dálkum í tvískiptum skrifum.

## <a name="columns-in-supply-chain-management"></a>dálkar í Supply Chain Management

Í Supply Chain Management endurspegla tveir dálkar stöðu sölupöntunarinnar. Dálkarnir sem þarf að varpa eru **Staða** og **Staða skjals**.

Tölusetningin **Staða** tilgreinir heildarstöðu pöntunar. Þessi staða er sýnd í pöntunarhausnum.

Tölusetningin **Staða** er með eftirfarandi gildi:

- Opin pöntun
- Afhent
- Reikningsfært
- Hætt við

Tölusetningin **Staða skjals** tilgreinir nýlegasta skjalið sem var búið til fyrir pöntunina. Til dæmis, ef pöntunin er staðfest, er þetta skjal staðfesting á sölupöntuninni. Ef sölupöntun er reikningsfærð að hluta og eftirstandandi lína er staðfest, helst staða skjalsins áfram **Reikningur** vegna þess að reikningurinn er búinn til síðar í ferlinu.

Tölusetningin **Staða skjals** er með eftirfarandi gildi:

- Staðfesting
- Tiltektarlisti
- Fylgiseðill
- Reikningur

## <a name="columns-in-sales"></a>dálkar í Sales

Í Sales sýna tveir dálkar stöðu pöntunar. Dálkarnir sem þarf að varpa eru **Staða** og **Staða úrvinnslu**.

Tölusetningin **Staða** tilgreinir heildarstöðu pöntunar. Hún eru með eftirfarandi gildi:

- Í gangi
- Sent inn
- Uppfyllt
- Reikningsfært
- Hætt við

Tölusetningin **Staða úrvinnslu** var kynnt svo að hægt sé að varpa stöðunni með nákvæmari hætti í Supply Chain Management.

Eftirfarandi tafla sýnir vörpun á **Stöðu úrvinnslu** í Supply Chain Management.

| Vinnslustaða   | Staða í Supply Chain Management | Staða skjals í Supply Chain Management |
|---------------------|-----------------------------------|--------------------------------------------|
| Í gangi              | Opin pöntun                        | Engum                                       |
| Staðfest           | Opin pöntun                        | Staðfesting                               |
| Tekið til              | Opin pöntun                        | Tínslulisti                               |
| Afhent að hluta | Opin pöntun                        | Fylgiseðill                               |
| Afhent           | Afhent                         | Fylgiseðill                               |
| Reikningsfært að hluta  | Afhent                         | Reikningur                                    |
| Reikningsfært            | Reikningsfært                          | Reikningur                                    |
| Hætt við           | Hætt við                         | Ekki tiltækt                             |

Eftirfarandi tafla sýnir vörpun á **Stöðu úrvinnslu** milli Sales og Supply Chain Management.

| Vinnslustaða   | Staða í Sales | Staða í Supply Chain Management |
|---------------------|-----------------|-----------------------------------|
| Í gangi              | Í gangi          | Opin pöntun                        |
| Staðfest           | Sent inn       | Opin pöntun                        |
| Tekið til              | Sent inn       | Opin pöntun                        |
| Afhent að hluta | Í gangi          | Opin pöntun                        |
| Reikningsfært að hluta  | Í gangi          | Opin pöntun                        |
| Reikningsfært að hluta  | Uppfyllt       | Afhent                         |
| Reikningsfært            | Reikningsfært        | Reikningsfært                          |
| Hætt við           | Hætt við       | Hætt við                         |

## <a name="setup"></a>Setja upp

Til að setja upp vörpun fyrir stöðudálka sölupöntunar þarf að virkja eigindirnar **IsSOPIntegrationEnabled** og **isIntegrationUser**.

Til að virkja eigindina **IsSOPIntegrationEnabled** skal fylgja þessum skrefum.

1. Í vafra skal fara á `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`. Skiptið út **\<test-name\>** með tengli fyrirtækisins við Sales.
2. Á síðunni sem opnast skal finna **organizationid** og gera athugasemd um gildið.

    ![Leit að organizationid.](media/sales-map-orgid.png)

3. Í Sales skal opna stjórnborð vafrans og keyra eftirfarandi forskrift. Notið gildið **organizationid** úr skrefi 2.

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on row update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![JavaScript-kóði í stjórnborði vafrans.](media/sales-map-script.png)

4. Gangið úr skugga um að **IsSOPIntegrationEnabled** sé stillt á **satt**. Notið vefslóðina úr skrefi 1 til að athuga gildið.

    ![IsSOPIntegrationEnabled stillt á satt.](media/sales-map-integration-enabled.png)

Til að virkja eigindina **erIntegrationUser** skal fylgja þessum skrefum.

1. Í Sales skal farið á **Stilling \> Sérstillingar \> Sérstilla kerfið**, velja **Notandatafla** og opna svo **Skjámynd \> Notandi**.

    ![Skjámynd notanda opnuð.](media/sales-map-user.png)

2. Í Field Explorer skal finna **Stilling samþættingarnotanda** og tvísmella á það til að bæta því við skjámyndina. Vistið breytingarnar.

    ![Stillingadálki samþættingarnotanda bætt við skjámyndina.](media/sales-map-field-explorer.png)

3. Í Sales skal farið í **Stilling \> Öryggi \> Notendur** og breyta yfirlitinu úr **Virkjaðir notendur** í **Notendur forrits**.

    ![Yfirlitinu breytt úr Virkjaðir notendur í Notendur forrits.](media/sales-map-enabled-users.png)

4. Veljið færslurnar tvær fyrir **Samþættingarnotandi tvöfaldra skrifa**.

    ![Listi yfir notendur forrits.](media/sales-map-user-mode.png)

5. Breytið gildinu á dálkinum **Stilling samþættingarnotanda** í **Já**.

    ![Gildinu breytt á stillingadálki samþættingarnotanda.](media/sales-map-user-mode-yes.png)

Sölupöntunum hefur verið varpað.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]