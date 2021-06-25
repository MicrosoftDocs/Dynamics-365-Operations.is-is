---
title: Vsk-skýrsla fyrir Egyptaland
description: Þetta efnisatriði útskýrir hvernig á að skilgreina og mynda eyðublað VSK-framtals fyrir Egyptaland.
author: sndray
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: tfehr
ms.search.validFrom: 2017-06-20
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 9c776cedb65804f8cadbe324082c2abac435f906
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186615"
---
#  <a name="vat-declaration-for-egypt-eg-00002"></a>Vsk-skýrsla fyrir Egyptaland (EG-00002)

[!include[banner](../includes/banner.md)]

[!include[banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að setja upp og mynda snið VSK-framtals og sölu- og innkaupabækur fyrir lögaðila í Egyptalandi.

Eyðublað VSK-framtals fyrir Egyptaland er opinbera skjalið sem tekur saman samtals skattupphæð útskatts til greiðslu, samtals endurheimtanlega skattupphæð innskatts og tengda skuldaupphæð VSK. Eyðublaðið er notað fyrir alla skattgreiðendur og á að klára handvirkt í gegnum gátt skattyfirvalda. Yfirleitt er talað um eyðublað VSK-framtals sem útfyllingu VSK-framtals.

Eyðublað VSK-framtals í Dynamics 365 Finance inniheldur eftirfarandi skýrslur:

- VSK-framtalseyðublað númer 10 sem býður upp á sundurliðun upphæða, leiðréttingar og VSK-upphæð fyrir hvert línuatriði í framtalseyðublaði VSK eins og lýst er í reglugerðinni.
- Sölufærslubók
- Innkaupafærslubók

## <a name="prerequisites"></a>Forkröfur
Aðalaðsetur lögaðilans verður að vera í Egyptalandi.
Á vinnusvæðinu **Eiginleikastjórnun** skal virkja eftirfarandi eiginleika:

   - (Egyptaland) Tegundastigveldi fyrir Sales og skattskýrslu innkaupa.

Nánari upplýsingar um að hvernig á að virkja eiginleika er að finna í [Yfirlit eiginleikastjórnunar](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Á vinnusvæðinu **Rafræn skýrslugerð** skal flytja inn eftirfarandi snið rafrænnar skýrslugerðar úr gagnageymslunni:

- VSK-skýrsla Excel (EG)

> [!NOTE]
> Sniðið hér að ofan er byggt á **Skattskýrslulíkaninu** og notar **Líkanavörpun skattskýrslu**. Fleiri skilgreiningar verða fluttar inn sjálfkrafa.

Frekari upplýsingar um hvernig á að flytja inn skilgreiningar rafrænnar skýrslugerðar er að finna í [Hlaða niður skilgreiningum rafrænnar skýrslugerðar úr Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

## <a name="download-electronic-reporting-configurations"></a>Hlaða niður skilgreiningum rafrænnar skýrslugerðar

Innleiðing VSK-framtalseyðublaðs fyrir Egyptaland byggir á skilgreiningum rafrænnar skýrslugerðar. Frekari upplýsingar um möguleika og hugmyndir á bak við stillanlega skýrslugerð er að finna í [Rafræn skýrslugerð](../../fin-ops-core/dev-itpro/analytics/general-electronic-reporting.md).

Fyrir umhverfi framleiðslu og samþykkisprófun notanda skal skoða [Hlaða niður skilgreiningum rafrænnar skýrslugerðar úr Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

Til að búa til VSK-framtalseyðublaðið og tengdar skýrslur í egypskum lögaðila skal hlaða upp eftirfarandi skilgreiningum:

- Tax declaration model.version.70.xml eða nýrri útgáfu
- Tax declaration model mapping.version.70.120.xml eða nýrri útgáfu
- VAT Declaration Excel (EG).version.70.32 eða nýrri útgáfu

Þegar skilgreiningum rafrænnar skýrslugerðar hefur verið hlaðið niður úr Lifecycle Services (LCS) eða altæku geymslunni skal ljúka eftirfarandi skrefum.

1. Farið á vinnusvæðið **Rafræn skýrslugerð** og veljið reitinn **Skýrsluskilgreiningar**.
1. Á síðunni **Skilgreiningar**, í aðgerðarúðunni, skal velja **Skipta út** > **Hlaða úr XML-skrá**.
1. Hlaðið upp skránum í þeirri röð sem þær eru birtar hér að ofan. Þegar öllum skilgreiningum hefur verið hlaðið upp ætti skilgreiningatréð að vera til staðar í Finance.

## <a name="set-up-application-specific-parameters"></a>Setja upp færibreytur tiltekins forrits

Færibreytur tiltekins forrits gera kleift að setja skilyrði um hvernig skattfærslur verða flokkaðar og reiknaðar í hverri línu þegar skýrslan er búin til. Ákvörðunin byggir á skilgreiningunni á VSK-flokki vöru, VSK-flokki, VSK-kóða og öðrum skilyrðum sem er komið fyrir í skilgreiningu uppflettingar.

Skýrslur sölu- og innkaupabóka fyrir Egyptaland innihalda dálkasafn sem samsvara tilteknum flokkunum á færslum af gerðinni aðgerðir, afurðir og skjöl sem miðast við Egyptaland. Í stað þess að taka þessar nýju flokkanir sem ný innsláttargögn þegar færslurnar eru bókaðar munu flokkanirnar verða ákvarðaðar samkvæmt mismunandi uppflettingum sem kynntar eru í **Skilgreiningar** > **Setja upp færibreytur tiltekins forrits** > **Uppsetning** til að uppfylla kröfur VSK-skýrslna fyrir Egyptaland. 

![Síða sértækra færibreyta fyrir forrit](media/egypt-vat-declaration-setup1.png)

Þessar eftirfarandi skilgreiningar uppflettingar eru notaðar til að flokka færslurnar í skýrslum VSK-bóka útskatts og innskatts:

- **PurchaseItemTypeLookup** > Dálkur O: Tegund atriðis
- **VATRateTypeLookup** > Dálkur B: Skattgerð
- **VATRateTypeLookup** > Dálkur C: Gerð töfluatriðis
- **PurchaseOperationTypeLookup** > Dálkur A: Tegund skjals
- **CustomerTypeLookup** > Dálkur A: Gerð skjals
- **SalesOperationTypeLookup** > Dálkur N: Gerð aðgerðar
- **SalesItemTypeLookup** > Dálkur O: Tegund atriðis

Ljúkið eftirfarandi skrefum til að setja upp mismunandi uppflettingar sem notaðar eru til að mynda VSK-skýrslu og tengdar skýrslur bóka. 

1. Á vinnusvæðinu **Rafræn skýrslugerð** skal velja **Skilgreiningar** > **Uppsetning** til að setja upp reglurnar til að bera kennsl á skattfærslurnar í tengdum reitum VSK-framtalseyðublaðsins.
2. Veljið núverandi útgáfu og í flýtiflipanum **Uppflettingar** skal velja heiti uppflettingar. Til dæmis **SalesItemTypeLookup**. Þessi uppfletting auðkennir lista yfir flokkanir í VSK-bókum útskatts sem skattyfirvöld krefjast.
3. Í flýtiflipanum **Skilyrði** skal velja **Bæta við** og í nýju línunni í dálknum **Niðurstaða uppflettingar** skal velja tengda línu sem stendur fyrir flokkunina í **Dálkur O**.
4. Í dálknum **VSK-flokkur** skal velja VSK-flokkinn sem er notaður til að auðkenna flokkunina. Til dæmis **Innlendur sölureikningur**. Einnig er hægt að nota VSK-flokk vöru, skattkóða eða samsetningu trjáeiginda ef skilgreiningin er skilgreind á annan hátt. 
5. Í dálknum **Heiti** skal velja flokkun skattfærslunnar.
6. Endurtakið skref 3-5 fyrir allar tiltækar uppflettingar.
7. Veljið **Bæta við** til að taka með síðustu færslulínuna og í dálknum **Niðurstaða uppflettingar** skal velja **Á ekki við**. 
8. Í dálkunum sem eru eftir skal velja **Ekki autt**. 
9. Í reitnum **Staða** skal velja **Lokið**.
10. Veljið **Vista** og lokið síðan skjámyndinni **Sértækar færibreytur forrits**.

> [!NOTE]
> Þegar síðustu færslunni er bætt við, **Á ekki við**, er eftirfarandi regla skilgreind: Þegar VSK-flokkur, VSK-flokkur vöru, skattkóði og heiti sem notað er sem frumbreyta uppfyllir ekki neina af fyrri reglum, verða færslurnar ekki hafðar með í VSK-bók útskatts. Þótt þessi regla sé ekki notuð þegar skýrsla er búin til, þá hjálpar hún til við að koma í veg fyrir villur í myndun skýrslu þegar skilgreiningu reglu vantar.

Eftirfarandi töflur eru dæmi um tillögu að skilgreiningu fyrir útskýrðar skilgreiningar uppflettingar. 

**SalesItemTypeLookup**

| Niðurstaða uppflettingar         | Lína | VSK-flokkur    | VSK-flokkur vöru    | Skattkóði (kóði) | Nafn                  |
|-----------------------|------|--------------------|-------------------------|-----------------|-----------------------|
| Innlent              | 1    | VAT_LOCAL          | *Ekki autt*             | *Ekki autt*     | Sala                 |
| Innlent              | 2    | VAT_LOCAL          | *Ekki autt*             | *Ekki autt*     | SalesCreditNote       |
| Innlent              | 3    | VAT_FINALC         | *Ekki autt*             | *Ekki autt*     | Sala                 |
| Innlent              | 4    | VAT_FINALC         | *Ekki autt*             | *Ekki autt*     | SalesCreditNote       |
| Innlent              | 5    | VAT_PUBLIO         | *Ekki autt*             | *Ekki autt*     | Sala                 |
| Innlent              | 6    | VAT_PUBLIO         | *Ekki autt*             | *Ekki autt*     | SalesCreditNote       |
| Flytja út                | 7    | VAT_EXPORT         | *Ekki autt*             | *Ekki autt*     | Sala                 |
| Flytja út                | 8    | VAT_EXPORT         | *Ekki autt*             | *Ekki autt*     | SalesCreditNote       |
| Vél og búnaður | 9    | *Ekki autt*        | VAT_M&E                 | *Ekki autt*     | Sala                 |
| Vél og búnaður | 10   | *Ekki autt*        | VAT_M&E                 | *Ekki autt*     | SalesCreditNote       |
| Vélarhlutar        | 11   | *Ekki autt*        | VAT_PARTS               | *Ekki autt*     | Sala                 |
| Vélarhlutar        | 12   | *Ekki autt*        | VAT_PARTS               | *Ekki autt*     | SalesCreditNote       |
| Undanþágur            | 13   | VAT_EXE            | *Ekki autt*           | *Ekki autt*     | SaleExempt            |
| Undanþágur            | 14   | VAT_EXE            | *Ekki autt*           | *Ekki autt*     | SalesExemptCreditNote |
| Ekki tiltækt        | 15   | *Autt*            | *Autt*                 | VAT_ADJ         | *Ekki autt*           |
| Ekki tiltækt        | 16   | *Ekki autt*        | *Ekki autt*             | *Ekki autt*     | *Ekki autt*           |

 **SalesOperationTypeLookup**

| Niðurstaða uppflettingar  | Lína | VSK-flokkur vöru    | Skattkóði    | Nafn                  |
|----------------|------|-------------------------|-------------|-----------------------|
| Vörur          | 1    | VAT_GOODS               | *Ekki autt* | Sala                 |
| Vörur          | 2    | VAT_GOODS               | *Ekki autt* | SalesCreditNote       |
| Vörur          | 3    | VAT_GOODS               | *Ekki autt* | SaleExempt            |
| Vörur          | 4    | VAT_GOODS               | *Ekki autt* | SalesExemptCreditNote |
| Þjónustur       | 5    | VAT_SERV                | *Ekki autt* | Sala                 |
| Þjónustur       | 6    | VAT_SERV                | *Ekki autt* | SalesCreditNote       |
| Þjónustur       | 7    | VAT_SERV                | *Ekki autt* | SaleExempt            |
| Þjónustur       | 8    | VAT_SERV                | *Ekki autt* | SalesExemptCreditNote |
| Leiðréttingar    | 9    | *Autt*                 | VAT_ADJ     | Sala                 |
| Leiðréttingar    | 10   | *Autt*                 | VAT_ADJ     | SalesCreditNote       |
| Ekki tiltækt | 11   | *Ekki autt*             | *Ekki autt* | *Ekki autt*           |

**PurchaseItemTypeLookup**

| Niðurstaða uppflettingar          | Lína | VSK-flokkur vöru    | Skattkóði    | Nafn                     |
|------------------------|------|-------------------------|-------------|--------------------------|
| Vörur                  | 1    | VAT_GOODS               | *Ekki autt* | Innkaup                 |
| Vörur                  | 2    | VAT_GOODS               | *Ekki autt* | PurchaseCreditNote       |
| Þjónustur               | 3    | VAT_SERV                | *Ekki autt* | Innkaup                 |
| Þjónustur               | 4    | VAT_SERV                | *Ekki autt* | PurchaseCreditNote       |
| Vél og búnaður  | 5    | VAT_M&E                 | *Ekki autt* | Innkaup                 |
| Vél og búnaður  | 6    | VAT_M&E                 | *Ekki autt* | PurchaseCreditNote       |
| Vélarhlutar         | 7    | VAT_PARTS               | *Ekki autt* | Innkaup                 |
| Vélarhlutar         | 8    | VAT_PARTS               | *Ekki autt* | PurchaseCreditNote       |
| Undanþágur             | 9    | VAT_EXE                 | *Ekki banki*  | PurchaseExempt           |
| Undanþágur             | 10   | VAT_EXE                 | *Ekki autt* | PurchaseExemptCreditNote |
| Ekki tiltækt         | 11   | *Ekki autt*             | *Ekki autt* | *Ekki autt*              |

**PurchaseOperationTypeLookup**

| Niðurstaða uppflettingar  | Lína | VSK-flokkur  | Skattkóði    | Nafn                     |
|----------------|------|------------------|-------------|--------------------------|
| Innlent       | 1    | VAT_LOCAL        | *Ekki autt* | Innkaup                 |
| Innlent       | 2    | VAT_LOCAL        | *Ekki autt* | PurchaseCreditNote       |
| Innlent       | 3    | VAT_LOCAL        | *Ekki autt* | PurchaseExempt           |
| Innlent       | 4    | VAT_LOCAL        | *Ekki autt* | PurchaseExemptCreditNote |
| Innflutt       | 5    | VAT_IMPORT       | *Ekki autt* | Innkaup                 |
| Innflutt       | 6    | VAT_IMPORT       | *Ekki autt* | PurchaseCreditNote       |
| Innflutt       | 7    | VAT_IMPORT       | *Ekki autt* | PurchaseExempt           |
| Innflutt       | 8    | VAT_IMPORT       | *Ekki autt* | PurchaseExemptCreditNote |
| Leiðréttingar    | 9    | *Autt*          | VAT_ADJ     | PurchaseCreditNote       |
| Leiðréttingar    | 10   | *Autt*          | VAT_ADJ     | Innkaup                 |
| Ekki tiltækt | 11   | *Ekki autt*      | *Ekki autt* | *Ekki autt*              |

**CustomerTypeLookup**

|    Niðurstaða uppflettingar    | Lína | VSK-flokkur |
|---------------------|------|-----------------|
| Stofnun/fyrirtæki        |  1   | VAT_LOCAL       |
| Stofnun/fyrirtæki        |  2   | VAT_EXPORT      |
| Stofnun/fyrirtæki        |  3   | VAT_EXE         |
| Lokaneytandi      |  4   | VAT_FINALC      |
| Opinbert fyrirtæki |  5   | VAT_PUBLIO      |
| Á ekki við      |  6   | *Ekki autt*     |

**VATRateTypeLookup**

| Niðurstaða uppflettingar  | Lína | Skattkóði (kóði) |
|----------------|------|-----------------|
| GeneralGoods   | 1    | VAT_ST          |
| GeneralGoods   | 2    | VAT_RD          |
| FirstTable     | 3    | *Ekki autt*     |
| SecondTable    | 4    | *Ekki autt*     |
| Ekki tiltækt | 5    | *Ekki autt*     |


## <a name="set-up-general-ledger-parameters"></a>Setja upp færibreytur fyrir Fjárhag

Til að mynda skýrslu VSK-framtalseyðublaðs á Microsoft Excel-sniði skal skilgreina snið rafrænnar skýrslugerðar á síðunni **Færibreytur fjárhags**.

1. Farið í **Skattur** > **Uppsetning** > **Færibreytur fjárhags**.
2. Í flipanum **Virðisaukaskattur**, í hlutanum **Valkostir skatts**, í reitnum **Sniðsvörpun VSK-skýrslu**, skal velja **VSK-skýrsla Excel (EG)**. Ef reiturinn er skilinn eftir auður verður stöðluð VSK-skýrsla búin til á SSRS-sniði.
3. Veljið **Tegundastigveldið**. Þessi flokkur gerir vörukóðanum í færsluflipa erlendra viðskipta kleift að leyfa notendum að velja og flokka vörur og þjónustu. Lýsing á þessari flokkun kemur fram í skýrslum sölu- og innkaupafærslna. Þessi flokkun er valfrjáls.

![Framtalseyðublað](media/egypt-vat-declaration-setup2.png)


## <a name="generate-a-vat-return-report"></a>Búa til skýrslu VSK-skila
Ferlið til að undirbúa og senda inn VSK-skilaskýrslur fyrir tímabil er byggt á greiðslufærslum VSK-greiðslna sem voru bókaðar við uppgjörs- og bókunarvinnu söluskatts. Frekari upplýsingar um virðisaukauppgjör og skýrslugerð er að finna í [Yfirlit virðisaukaskatts](../general-ledger/indirect-taxes-overview.md).

Ljúkið eftirfarandi skrefum til að mynda skattskýrsluna.

1. Farið í **Skattur** > **Skattframtöl** > **Virðisaukaskattur** > **Tilkynna virðisaukaskatt fyrir uppgjörstímabil** eða **Gera upp og bóka virðisaukaskatt**.
2. Veljið **Jöfnunartímabil**.
3. Veljið dagsetningu frá og veljið síðan útgáfu VSK-greiðslu.
5. Veljið **Í lagi**. 
6. Sláið inn kreditupphæð frá fyrra tímabili, ef við á, eða skiljið upphæðina eftir sem núll.
7. Í reitnum **Upplýsingar skýrslu** skal velja einn af eftirfarandi tiltækum möguleikum. 
   - **VSK-bók innskatts**: Búið til skýrslu um upplýsingar um skattfærslu innkaupa.
   - **VSK-bók útskatts**: Búið til skýrslu um upplýsingar um skattfærslu sölu.
   - **VSK-skýrsla**: Búið aðeins til framtalseyðublað VSK-skýrslu.
8. Sláið inn nafn einstaklingsins sem er skráður fyrir því að úthluta eyðublaðinu.
9. Veljið tungumálið. Allar skýrslur eru þýddar á **en-us** og **ar-eg**.
  
[!INCLUDE[footer-include](../../includes/footer-banner.md)]


