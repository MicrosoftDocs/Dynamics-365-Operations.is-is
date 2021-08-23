---
title: Power BI-efni útgjaldastýringar
description: Þetta efnisatriði lýsir því hvað er innifalið í útgjaldastýringu Power BI efnispakka.
author: panolte
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvExpenseWorkspace, ExpenseWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kfend
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 178a65c44abd0c9c068d4da1f2684a60062da595247560de4cb81d97ab7b6521
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6769899"
---
# <a name="expense-management-power-bi-content"></a>Power BI-efni útgjaldastýringar

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvað er innifalið í útgjaldastýring Power BI efnis. 

## <a name="overview"></a>Yfirlit
Tveir Power BI efnispakkar eru í boði til að nota með útgjaldastýringu í útgáfu 8.1 eða nýrri. 
- Til er persónubundið yfirlit sem er hannað fyrir starfsmenn sem senda inn kostnaðarskýrslur. 

  Yfirlitið er sniðið til að veita einstaklingum lykilupplýsingar um ósendar og sendar upphæðir, ásamt sögu og innsýn í sögu kostnaðarfærsla. Persónubundið yfirlit er ein síða sem inniheldur mikilvægustu upplýsingarnar fyrir notandann.

- Til er stjórnendayfirlit sem er hannað fyrir starfsmenn og stjórnendur viðskiptaskulda. Yfirlitið er sniðið að því að fylgjast með og tilkynna um heildarútgjöld starfsmanns. Það veitir helstu mælikvarða á kostnað, t.d. upphæðir á ósendum kostnaði, akstri og meðaltal fyrir kostnaðarskýrslu. Það notar færslugögn og veitir samtöluyfirlit yfir útgjaldastýringu þvert yfir öll fyrirtæki. Það veitir einnig sundurliðun fyrir hvern starfsmann, með möguleikanum á því að bæta við fjárhagsvíddargögnum. Efni kostnaðargreiningar stjórnanda inniheldur: 
  - Yfirlitssíðu með helstu mælikvörðum um upphæðir kostnaðar og innsýn inn í uppkast, í vinnslu og loknum kostnaðarskýrslum. 
  - Upplýsingasíða starfsmanns til að yfirfara einstakar upplýsingar um starfsmann eftir tíma, kostnaðargerð og upplýsingaflokki. 
  - Samanburðarsíða starfsmanns til að bera saman marga starfsmenn yfir tíma. 

Allar upphæðir eru sýndar í gjaldmiðli fyrirtækis. Gögn fyrir öll fyrirtæki eru sýnd, en ef þess gerist þörf er hægt að bæta við fyrirtækissíu. 

## <a name="accessing-the-power-bi-content"></a>Aðgangur að Power BI efni
Hægt er að finna Expense Admin Dashboard.pbix og Expense Personal Dashboard.pbix Power BI efni í samnýttu eignasafni í Microsoft Dynamics Lifecycle Services (LCS). Upplýsingar um hvernig á að sækja efnið og tengja það við gögn fyrirtækisins er að finna í [Power BI-efni í LCS frá Microsoft og viðskiptaaðilum þínum](/archive/blogs/dynamicsaxbi/power-bi-content-from-microsoft-and-your-partners).
Efnið er tiltækt á vinnusvæði útgjaldastýringar sem innfellt Power BI-efni. Hvaða eigandi kostnaðar sem er hefur aðgang að persónulegum útgjöldum, á meðan einungis starfsmenn og stjórnendur viðskiptaskulda hafa aðgang að efni kerfisstjóra til að skoða öll kostnaðargögn notanda.

## <a name="refreshing-the-power-bi-content"></a>Endurhleður Power BI efni
Útgjaldastýring Power BI-efnis krefst þess að TrvBiExpenseMeasurement mæling og BudgetActivityMeasure verði endurhlaðin úr einingaversluninni. 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mælikvarðar sem eru hafðir með í Power BI efni
Innihaldið inniheldur hóp af skýrslusíðum. Hver síða samanstendur af safni mælikvarða sem eru sýndir sem myndrit, reitir og töflur. Eftirfarandi tafla veitir yfirlit yfir myndrænar framsetningar í Power BI efni.

**Greiningar á persónulegum kostnaði**

| Skýrslusíða | Myndbirting                             |
|-------------|-------------------------------------------|
| Minn kostnaður | Kílómetrafjöldi                         |
|             | Kostnaðarskýrslur í vinnslu                |
|             | Nei. af ósendum kostnaði               |
|             | Persónulegur kostnaður sem þarf að greiða              |
|             | Ósend upphæð                        |
|             | Innsend upphæð                          |
|             | Upphæð sem bíður endurgreiðslu             |
|             | Kostnaðarskýrslur með upphæðum og stöðu   |
|             | Innsendar en ósamþykktar kostnaðarskýrslur  |
|             | Kostnaður eftir kostnaðargerð                     |
|             | Kostnaður eftir söluaðila                      |
|             | Kostnaður eftir meðhöndluðum kostnaði            |
|             | Kostnaður eftir verki                       |
|             | Heildarfærsluupphæð yfir tíma        |

**Kostnaðargreining stjórnenda**

| Skýrslusíða         | Myndbirting                           |           
|---------------------|-----------------------------------------|
| Kostnaðaryfirlit    | Drög að upphæð kostnaðar                   |
|                     | Fjöldinn af drögum að kostnaðarlínum           |
|                     | Drög að kostnaðarlínum                     |
|                     | Brot á reglum kostnaðarskýrslu        |
|                     | Útistandandi upphæð                      |
|                     | Innsendur en ósamþykktur kostnaður       |
|                     | Samþykktur kostnaður                       |
|                     | Heildar kostnaðarupphæð                    |
|                     | Samantekt á kostnaðarskýrslu                |
|                     | Kostnaður eftir kostnaðargerð                   |
|                     | Kostnaður eftir söluaðila                    |
|                     | Kostnaður eftir starfsfólki                   |
|                     | Kostnaður á móti verki                     |
| Samanburður starfsmanna | Upphæðir kostnaðar                         |
|                     | Upphæðir kostnaðar yfir tíma eftir starfsmanni   |
| Upplýsingar starfsmanns | Kostnaðarskýrslur eftir kostnaðargerð            |
|                     | Persónulegur kostnaður                       |
|                     | Kostnaðarskýrslur eftir upplýsingaflokki     |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]