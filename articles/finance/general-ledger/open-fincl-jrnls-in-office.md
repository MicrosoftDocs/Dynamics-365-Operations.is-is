---
title: Opna sniðmát fyrir fjárhagsbók í Office
description: Þessi grein lýsir vandamálum sem gætu komið upp þegar þú býrð til sérsniðnar fjárhagsbækur með því að nota Microsoft Excel sniðmát.
author: kweekley
ms.date: 05/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a29ab1cb2980ebfed6c6fa6409538bc802849156
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896348"
---
# <a name="open-financial-journal-templates-in-office"></a>Opna sniðmát fyrir fjárhagsbók í Office

[!include [banner](../includes/banner.md)]

Þessi grein lýsir vandamálum sem gætu komið upp þegar þú býrð til sérsniðnar fjárhagsbækur með því að nota Microsoft Excel sniðmát.

## <a name="symptom"></a>Einkenni

Þú bjóst til sérsniðið Excel-sniðmát fyrir fjárhagsbækur en það birtist ekki á valmyndinni **„Opna línur í Excel“**. Eða, ef það birtist það á valmyndinni, annað sniðmát er opnað en það sem þú valdir.

## <a name="resolution"></a>Lausn

Sjálfgefna virknin „Opna í Excel“ notar rótargagnagjafa (tafla) núverandi síðu til að ákvarða hvaða sniðmát eða gagnaeiningar Office birtast sem valkostir á valmyndinni **„Opna í Excel“**. Þessi virkni hentar ekki fjárhagsbókum þar sem þær nota sömu töflur (LedgerJournalTable og LedgerJournalTrans) og rótargagnagjafar margra annarra gerða færslubóka.

Í tilfellum fjárhagsbóka er „Opna línur í Excel“ virkninni ætlað að sýna sniðmát sem eru hönnuð í samhengi við færslubókina sem þú ert að vinna í, t.d. almenna dagbók eða greiðsludagbók. Til dæmis er sniðmát sem er ætlað er til notkunar með greiðsludagbók söluaðila hannað til að framfylgja aðalreikningi þínum sem lánardrottnalykill.

Ef þú vilt kynna sniðmát svo það sé tiltækt á **„Opna línur í Excel“** og valmyndinni **„Opna línur í Excel“** er auðvelt þróunarumhverfi að innleiða **LedgerIJournalExcelTemplate** viðmótið og stækka **DocuTemplateRegistrationBase** klasann. Mörg dæmi um þessa nálgun eru í kerfinu. Dæmi sem má nota til viðmiðunar er **LedgerDailyJournalExcelTemplate** viðmótið sem búið var til fyrir almenna færslubók (eða daglega færslubók).

Þegar **LedgerIJournalExcelTemplate** viðmótið er útfært fyrir sniðmátið þitt síar valmyndin **„Opna línur í Excel“** sniðmát eftir færslubókargerðinni sem þú notar og sýnir aðeins sniðmátin sem eru í boði fyrir þá færslubók. Viðmótið býður einnig upp á villuleitaraðferð sem tryggir að ekki sé hægt að opna sniðmát fyrir færslubók nema það uppfylli kröfur lyklagerðarinnar. Til dæmis geturðu tilgreint að lyklagerðin verði að vera **„Lánardrottinn“** eða **„Fjárhagur“**.

Nánari upplýsingar um þessa virkni má nálgast á [Sniðmátum bætt við valmyndina „Opna línur í Excel“](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).
