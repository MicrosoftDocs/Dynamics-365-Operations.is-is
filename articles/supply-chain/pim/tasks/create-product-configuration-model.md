---
title: Stofna afbrigðalíkan afurðar
description: Þessi verklýsing sýnir hvernig á að stofna afbrigðalíkan afurðar og færa inn grunnupplýsingar eins og eigindir og undiríhlutir.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0ff03c13e1d9b7a15a0237b8248c734aa879166d2db2cebeb4a98db699e3de95
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748740"
---
# <a name="create-a-product-configuration-model"></a>Stofna afbrigðalíkan afurðar

[!include [banner](../../includes/banner.md)]

Þessi verklýsing sýnir hvernig á að stofna afbrigðalíkan afurðar og færa inn grunnupplýsingar eins og eigindir og undiríhlutir. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.


## <a name="create-a-product-model"></a>Stofna framleiðslulíkan

1. Farið í **Afurðarupplýsingastjórnun \> Afurðir \> Afbrigðalíkön afurða**.
1. Veljið **Nýtt**.
1. Í reitinn **Heiti** skal slá inn gildi.
1. Í reitinn **Lýsing** skal slá inn gildi.
1. Í reitnum **Stefna leysis** skal velja valkost.
    * Leysisstefnu ákvarðar hvernig skorður í afbrigðalíkani afurðar sem byggir á skorðum eru unnar. Þetta val getur haft áhrif á afköst afbrigðalíkan afurðar.  
1. Í reitinn **Heiti** skal slá inn gildi.
    * Rótaríhlutur stendur fyrir afbrigðalíkan afurðar, en einnig er hægt að nota það í öðrum vörulíkan.  
1. Veljið **Í lagi**.
1. Veljið valkost í svæðinu **Endurnota skilgreiningar**.
    * Ef færibreytan endurnýtingu skilgreiningar er stillt á Já, mun kerfið leita að eins skilgreiningar eftir hverja stillingarlotu og nota aftur ef nákvæm samsvörun finnst.  

## <a name="add-attributes"></a>Bæta við eigindum

1. Stækka hlutann **Eigindir**.
2. Veljið **Bæta við**.
3. Í listanum skal merkja valda línu.
4. Í reitinn **Heiti** skal slá inn gildi.
5. Í reitinn **Heiti leysis** skal slá inn gildi.
    * Heiti Leysara er notaður af skorðu leysara afurðaafbrigðastillis. Hún má ekki innihalda bil eða sérstafir nema _ (undirstriki).  
6. Í reitinn **Lýsing** skal slá inn gildi.
    * Texti lýsingar birtist notandanum skilgreiningu og þar af leiðandi getur þjónað sem hjálp í að velja rétt gildi eigindar.  
7. Færa inn eða veljið gildi í svæðinu **Gerð eigindar**.
    * Gerð eigindar ákvarðar hvaða gildi eru tiltæk fyrir eigindina.  
8. Veljið gátreitinn **Taka í endurnýtingu**.
    * Þessi valkostur er aðeins tiltækur þegar valkosturinn Endurnýtingu skilgreininga er valin. Að hafa eigind með í gátreit Endurnýta þýðir að þessi eigind verður athuguð þegar kerfið leitar að nákvæm samsvörun.  

## <a name="add-subcomponents"></a>Bæta við undiríhlutir

1. Stækkaðu hlutann **Undiríhlutir**.
2. Veljið **Bæta við**.
3. Í listanum skal merkja valda línu.
4. Í reitinn **Heiti** skal slá inn gildi.
5. Í reitinn **Heiti leysis** skal slá inn gildi.
6. Í reitinn **Lýsing** skal slá inn gildi.
7. Færa inn eða veljið gildi í svæðinu **Íhlutur**.
    * Hver undirþáttagerð verður að vísa í íhlutarskilgreiningu. Þessi hönnun styður endurnýtanlegu íhluti og tryggir að þegar íhlutur hefur verið skilgreint er hægt að nota í mörg framleiðslulíkön.  
8. Veljið **Vista**.
9. Veljið **Upplýsingar um uppskriftarlínu**.
    * Upplýsingar um uppskriftalínuskjámyndina gera notandanum kleift að velja viðeigandi eiginleika fyrir undiríhlutina. Hægt er að gefa hverjum eiginleika fast gildi eða varpa honum á eigind. Að varpa á eigind leiðir til að Uppskrift línueiginleika fær mismunandi gildi eftir því hvað var valið í skilgreiningarhlutanum.  
10. Í reitinn **Vörunúmer** skal slá inn eða velja gildi.
    * Hver undirþáttagerð táknar skilgreinanleg afurðarsniðmát með skorðuskilgreiningartækni. Tilvísun er gerð með vörunúmeri.  
11. Veljið gátreitinn **Stilla**.
12. Velja skal **Já** í reitnum **Útreikningur**.
    * Stilla valkost útreiknings tryggir að afurðin verða teknar með við útreikning kostnaðar fyrir afurðina.  
13. Veljið flipann **Uppsetning**.
14. Veljið gátreitinn **Stilla**.
15. Í reitnum **Magn** slærðu inn tölu.
    * Magn svæðið ákvarðar hversu mikið þessarar afurðar verður að nota í skilgreindu vörunni.  
16. Veljið gátreitinn **Stilla**.
17. Í reitinn **Á raðir** skal slá inn númer.
18. Veljið **Í lagi**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]