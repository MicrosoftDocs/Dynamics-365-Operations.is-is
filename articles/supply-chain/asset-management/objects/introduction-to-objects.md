---
title: Kynning á eignum
description: Í þessari grein er að finna yfirlit yfir eiginleika eigna í Eignastýringu.
author: johanhoffmann
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage, EntAssetTimeline, EntAssetObjectTableLookup, EntAssetObjectTableParent, EntAssetObjectOverview, EntAssetObjectImage, EntAssetObjectTable, EntAssetLifecycleStateLog, EntAssetObjectWorkOrderActive, EntAssetObjectAttribute
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "2214"
- intro-internal
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d8498d6099112cea2c57a6387e7596adb5bcd84e
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016015"
---
# <a name="introduction-to-assets"></a>Kynning á eignum

[!include [banner](../../includes/banner.md)]

 

Í þessari grein er að finna yfirlit yfir eiginleika eigna í Eignastýringu. *Eign* er hvers konar búnaður, svo sem vél eða vélahlutur, sem krefst viðhalds, þjónustu eða viðgerða.

Eign er sjálfkrafa uppfærð með tengdum upplýsingum. Til dæmis gætu þessar tengdar upplýsingar snúist um nýjar eða uppfærðar verkbeiðnir. Þú getur búið til eignir með því að nota annaðhvort valmyndaratriðið **Allar eignir** eða valmyndaratriðið **Eignir í bið**. Þessi grein útskýrir hvernig á að búa til eignir með því að nota **Allar eignir** valmyndaatriðið. Fyrir upplýsingar um hvernig á að búa til eignir með því að nota valmyndaratriðið **Eignir í bið**, sjá [Stofna eignir byggðar á innkaupapöntunum](../objects/create-objects-based-on-purchase-orders.md).

## <a name="all-assets"></a>Allar eignir

Veldu **Eignastýring** \> **Eignir** \> **Allar eignir**. Listasíðan **Allar eignir** sýnir allar eignir og sumar upplýsingar sem tengjast þeim. Til að skoða eingöngu virkar eignir velurðu **Virkar eignir**. Til að skoða eignir sem eru uppsettar á þeim virkum staðsetningum sem þú tengist sem viðhaldsstarfsmaður skaltu velja **Mínar virku eignir**. (Þessi tengsl eru sett upp á síðunni **Starfskraftar**. Sjá frekari upplýsingar [Viðhaldsstarfsmenn og starfsmannahópar](../setup-for-objects/workers-and-worker-groups.md).)

Í hnitalínuyfirlitinu **Allar eignir** velurðu tengil í dálkinum **Eign** til að skoða upplýsingar um valinn skrá. Til að breyta skránni skaltu velja hnappinn **Breyta**. Í smáatriðinu eru ítarlegar upplýsingar sem tengjast eigninni. Glugginn **Tengdar upplýsingar** til hægri inniheldur viðbótarupplýsingar sem tengjast eigninni. Stækkaðu rúðuna til að sýna tengdar upplýsingar fyrir valda eign.

Hnapparnir á aðgerðarglugganum eru skipulagðir á flipa. Eftirfarandi tafla lýsir stuttlega hnöppunum sem tengjast eignastýringu.

| Heiti hnapps          | Lýsing                                                                                                                                                       |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Breyta                 | Breyta valinni eign.                                                                                                                                         |
| Nýjar                  | Búa til nýja eign.                                                                                                                                                |
| Eyða               | Eyða valinni eign.                                                                                                                                       |
| Færa eign           | Færa eignir í aðra eignaskipan, eða á annan stað í sömu eignaskipan.                                                                                         |
| Skipta út eign        | Skiptu út einni undireign í eignastigveldi með annarri eign.                                                                                                  |
| Settu upp eign        | Setja upp eign á virkri staðsetningu.                                                                                                                          |
| Afrita eign           | Afritaðu eignastigveldi yfir í aðra eign.                                                                                                                          |
| Beiðnir             | Opnaðu listasíðuna **Virkar eignir** þar sem þú getur skoðað viðhaldsbeiðnir sem hafa verið stofnaðar fyrir valda virka eign.                                                                         |
| Viðburðarferill        | Skoða yfirlit yfir hinar ýmsu skráningar sem gerðar hafa verið á eigninni.                                                                                                         |
| Uppskrift eignar            | Skoða lista yfir alla hluti (varahluti og aðra hluti) sem eru notaðir á eign.                                                                                  |
| Verkbeiðnir          | Opnaðu listasíðuna **Virkar verkbeiðnir** þar sem þú getur skoðað verkbeiðnir fyrir eignina.                                                                                        |
| Gátlisti            | Skoða yfirlit yfir viðhaldsgátlista og mælingar sem hafa verið skráðar á eignina.                                                                                                 |
| Niðurtími vegna viðhalds | Búðu til eða skoðaðu skráningar niðurtíma vegna viðhalds á eigninni.                                                                                                       |
| Verkfærslur | Skoða allar bókaðar færslur sem tengjast verkbeiðnum sem hafa verið stofnaðar fyrir eignina.                                                                                       |
| Eignamælingar       | Búðu til eða skoðaðu eignamælingar á eigninni.                                                                                                               |
| Viðhaldsáætlun | Opnaðu listasíðuna **Opna viðhaldsáætlun** þar sem þú getur skoðað viðhaldsáætlanir, viðhaldsbeiðnir og viðhaldsumferðir sem tengjast eigninni og hafa stöðu **Stofnað**. |
| Uppfæra eignastöðu   | Uppfæra líftímastöðu eignar. Þú getur valið margar eignir á listasíðunni **Allar eignir** og uppfærðu síðan líftímastöðu eigna fyrir alla á sama tíma.              |
| Kladdi líftímastöðu  | Opnaðu kladdaskrá sem sýnir líftímastöður valinnar eignar.                                                                                                                 |
| Eignaskjöl      | Skoða lista yfir skjölin sem hengd eru við völdu eignina. Þessi skjöl eru sett upp í **Eignastýring** \> **Uppsetning** \> **Eignaskjöl**.                 |
| Eiginleikar           | Stofnaðu eða skoðaðu eignaeigindirnar.                                                                                                                             |
| Mynd                | Velja skal mynd fyrir eignina.                                                                                                                                   |
| Yfireignir        | Skoða sögu yfireigna fyrir valda eign.                                                                                                                |
| Virkar staðsetningar | Skoða sögu virkra stasðetninga fyrir valda eign.                                                                                                          |
| Ástandsmat | Skráðu ástandsmatsmælingar á eigninni.                                                                                                         |
| Bilanir               | Opnaðu listasíðuna **Eignabilanir** þar sem þú getur skoðað bilanir sem hafa verið skráðar á eignina.                                                                                             |
| Kostnaðarstýring         | Berðu saman kostnaðaráætlun og raunkostnað eignarinnar.                                                                                                              |
| Klukkustundastjórnun         | Berðu saman spátíma og rauntíma eignarinnar.                                                                                                              |
| Afkastavísar (KPI) eignar           | Reiknaðu og skoðaðu lykilárangur (KPI) fyrir eignina.                                                                                              |
| Starfsgerðir            | Skoða yfirlit yfir núverandi sjálfgefnar starfstegundir fyrir eignina.                                                                                                            |
| Gerðir mikilvægis    | Skoðaðu eða uppfærðu mikilvægi eigna.                                                                                                                              |
| Varahlutir          | Skoðaðu lista yfir viðurkennda og aðra varahluti sem hægt er að nota á eignina.                                                                               |
| Notkun eignar    | Prentaðu skýrslu sem sýnir neytendaskráningar á eigninni.                                                                                                |
| Bilun eignar          | Prentaðu skýrslu sem sýnir bilanaskráningar á eigninni.                                                                                                      |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]