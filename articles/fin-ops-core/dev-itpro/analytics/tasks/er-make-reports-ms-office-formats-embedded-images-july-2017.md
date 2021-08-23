---
title: Hanna skilgreiningar til að búa til skýrslur á Office-sniði með innfelldum myndum
description: Í þessu efni er útskýrt hvernig á að hanna skilgreiningar sem mynda rafræn skjöl á Excel- og Word-sniði sem innihalda innfelldar myndir.
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 03a514c5b616d761ef3eb6347e67e645b23eaa1794911775835e77cded4500ac
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6719346"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a>Hanna skilgreiningar til að búa til skýrslur á Office-sniði með innfelldum myndum

[!include [banner](../../includes/banner.md)]

Til að ljúka þessum skrefum í ferlinu skal fyrst ljúka við ferlið „Rafræn skýrslugerð Stofna skilgreiningarveitu og merkja hana sem virka.“ Ferlið útskýrir hvernig á að hanna grunnstillingar fyrir rafræna skýrslugerð til að mynda ívafnar myndir í Microsoft Excel eða Word skjali sem inniheldur ívafnar myndir. Í þessu ferli mun notandi stofna nauðsynlega grunnstillingu rafrænnar skýrslugerðar fyrir sýnifyrirtæki, Litware, Inc. Hægt er að ljúka þessum skrefum með USMF-gagnamengi. Þetta ferli er hugsað fyrir þá notendur sem hefur verið úthlutað hlutverkum Kerfisstjóra eða Þróunaraðila rafrænnar skýrslugerðar. Áður en hafist er handa skal sækja og vista eftirfarandi skrár: 

| lýsing                                          | Skrárnafn                   |
|------------------------------------------------------|-----------------------------|
| Skilgreining á gagnalíkani í ER                          | [Model for cheques.xml](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| ER Sníða skilgreiningu                              | [Cheques printing format.xml](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| Mynd af merki fyrirtækis                                   | [Company logo.png](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| Mynd af undirskrift                                      | [Signature image.png](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| Önnur mynd af undirskrift                          | [Signature image 2.png](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| Microsoft Word-sniðmát fyrir prentun greiðsluávísana  | [Cheque template Word.docx](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |

## <a name="verify-prerequisites"></a>Staðfesta forkröfur  
 1. Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.  
 2. Vertu viss um að skilgreiningarveitan fyrir sýnifyrirtækið, Litware, Inc., sé tiltæk og merkt Virk. Ef þú sérð skilgreiningarveituna ekki, skal klára skrefin í ferlinu „Stofna skilgreiningarveitu og merkja hana sem virka”.   
 3. Smelltu á Grunnstillingar skýrslugerðar  
 
## <a name="add-a-new-er-model-configuration"></a>Bæta við nýrri grunnstillingu líkans í Rafræn skýrslugerð  
 1. Í stað þess að búa til nýtt líkan er hægt að hlaða upp líkanstillingarskránn rafrænnar skýrslugerðar (Model for cheques.xml) sem var vituð áður. Þessi skrá inniheldur sýnigögn gagnalíkans fyrir greiðslu ávísana og vörpun gagnalíkans í gagnalíka Dynamics 365 for Operations.   
 2. Á Útgáfur flýtiflipa skal smella á Exchange.   
 3. Smellt er á Hlaða úr XML-skrá.  
 4. Smellið á Fletta og veljið Model for cheques.xml.   
 5. Smellið á „Í lagi“.  
 6. Hlaðið líka verður notað sem gagnaveita fyrir upplýsingar til að búa til skjöl sem innihalda myndir í Excel og Word.  

## <a name="add-a-new-er-format-configuration"></a>Bæta við nýrri grunnstillingu sniðs í Rafræn skýrslugerð  
 1. Í stað þess að búa til nýtt snið er hægt að hlaða upp líkanastillingaskrá rafrænnar skýrslugerðar (Cheques printing format.xml) sem var vistuð áður. Þessi skrá inniheldur sýniútlit sniðsins til að prenta ávísanir með forstillingarsniði og vörpun þessa sniðs í „Model for cheques” gagnalíkan.   
 2. Smellt er á Skipta út.  
 3. Smellt er á Hlaða úr XML-skrá.  
 4. Flettið og veljið Ávísanir prentsnið format.xml skrá.   
 5. Smellið á „Í lagi“.  
 6. Í trénu skal víkka út „Líkan fyrir ávísanir“.  
 7. Í trénu skal velja „Líkan fyrir ávísanir\Ávísanir prentsnið“.  
 8. Hlaðið snið verður notað til að búa til skjöl sem innihalda myndir í Excel og Word.   

## <a name="configure-er-user-parameters"></a>Skilgreina færibreytur notanda rafrænnar skýrslugerðar  
 1. Í Aðgerðarrúðunni er smellt á skilgreiningar.  
 2. Smelltu á Færibreytur notanda  
 3. Veljið Já í svæðinu Stillingar keyrslu.  
  Kveikið á „Keyrsludrög” fánann til að hefja drög að útgáfu af völdu sniði í stað þess sem lokið er.  
 4. Smellið á „Í lagi“.  

## <a name="configure-cash--bank-management-parameters"></a>Grunnstilla færibreytur reiðufjár- og bankastjórnunar  
 1. Farið í Reiðufjár- og bankastjórnun > Bankareikningar > Bankareikningar.  
 2. Nota flýtiafmörkun til að sía í reitnum bankareikningur með gildið „USMF OPER“.  
 3. Í aðgerðasvæðinu er smellt á setja upp.  
 4. Smella skal á athuga.  
 5. Víkka út hlutann Uppsetning.  
 6. Smellið á „Breyta“.  
 7. Velja Já í reitnum Lógó fyrirtækis.  
 8. Prenta merki fyrirtækis.  
 9. Smellt er á breyta.  
 10. Smellið á Fletta og veljið skrána sem var sótt áður Company logo.png.   
 11. Smellið á „Vista“.  
 12. Lokið síðunni.  
 13. Víkkið út hlutann Undirskrift.  
 14. Velja skal Já í svæðinu Prenta fyrstu undirskrift.  
 15. Smellt er á breyta.  
 16. Smellið á Fletta og veljið skrána sem var sótt áður Signature image.png.   
 17. Útvíkka hluta Eintaka.  
 18. Í reitnum Vatnsmerki skal velja valkost.  
 19. Velja skal Já í Almennan rafræna skýrslugerð svæði.  
 20. Veljið Veldu stillingarnar „Ávísanir prentsnið“.  
 21. Nú verður snið rafrænnar skýrslugerðar notað fyrir prentun ávísana.  
 22. Smellt er á Hengja við.  
 23. Smellið á „Nýtt“.  
 24. Smella á Skrá  
 25. Smellið á Fletta og veljið skrána sem var sótt áður Signature image 2.png.   
 26. Lokið síðunni.  
 27. Lokið síðunni.  
 28. Lokið síðunni.  
 29. Fara í Reiðufjár- og bankastjórnun > Uppsetning > Færibreytur reiðufjár- og bankastjórnunar.  
 30. Velja skal Já í Leyfa stofnun fyrirframkvittana fyrir óvirka bankareikninga: reitinn.  
 31. Smellið á „Vista“.  
 32. Lokið síðunni.  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
